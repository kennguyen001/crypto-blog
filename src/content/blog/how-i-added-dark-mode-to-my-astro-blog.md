---
title: "How I Added Dark Mode to My Astro Blog (and Fought a Few Bugs Along the Way)"
description: "A story about how I added dark mode to my Astro blog, the unexpected bugs I ran into, and how I fixed them."
pubDate: 'Sept 17, 2025'
---

---

One of the first things I wanted on my new Astro blog was a dark theme. I mean, every serious dev blog needs one, right? I thought it’d be a quick add-on, slap on a toggle, flip a few colors, done. Spoiler: it wasn’t that simple. Here’s how it went down.

## Tailwind Setup: The First Roadblock

I started by trying to add Tailwind. Astro makes it easy *in theory*, but my setup wasn’t playing nice. At first I didn’t even have a `tailwind.config.mjs`. Then when I did get Tailwind running, my `@tailwind` directives in `global.css` were throwing unknown rule errors.

It turned out I was missing **autoprefixer** and the right PostCSS plugin. A couple of installs later:

```bash
npm install -D tailwindcss @tailwindcss/postcss autoprefixer
```

And finally, Tailwind was alive. Small win ✌️

## The Toggle That Cried Null

With Tailwind ready, I made a `ThemeToggle.astro` component: a button with a sun and moon icon. Click it, and it switches the theme.

That’s when TypeScript decided to remind me that DOM elements can be `null`. My code was yelling at me:

```ts
'sun' is possibly 'null'
'moon' is possibly 'null'
```

Really? I could *see* the sun and moon right there.

I ended up fixing it by asserting with `!` (non-null assertion operator) and adding some safety checks. Not elegant, but it worked.

## The Icon Saga

My first icons were SVGs. The moon looked fine, but the sun? At small sizes it looked… weird. Too many rays, not enough sun.

So I thought: why not just use PNGs? I dropped in `moon-icon.png` and `sun-icon.png` and changed `<svg>` to `<img>`.

Boom. Error:

```
Type 'ImageMetadata' is not assignable to type 'string'
```

Turns out Astro doesn’t give you a string when you import an image, it gives you an object. Classic.

The trick was using `.src`:

```astro
<img src={sunIcon.src} alt="Sun icon" />
```

Lesson learned: Astro images are fancy.

## The “Reset on Page Change” Problem

Okay, I had the toggle working. I could switch to dark mode. But the moment I clicked into another page, the blog reset back to light mode.

That was infuriating.

The problem was that I wasn’t remembering the user’s preference anywhere. So I added `localStorage.theme = 'dark'` or `'light'` in the toggle, and then a tiny script in the `<head>` (`ThemeInit.astro`) that runs before anything renders.

That script checks localStorage and system settings, then slaps on `class="dark"` to `<html>` if needed. Problem solved. Dark mode now *sticks*.

## Wrestling With Global Styles

At this point, things were “working” — but ugly. My blog still had Bear Blog’s original CSS baked in, with hard-coded colors. Light mode looked fine, dark mode looked like I’d forgotten to pay my CSS bill.

So I went through `global.css` and added `.dark` overrides:

```css
code {
  background-color: rgb(var(--gray-light));
}
.dark code {
  background-color: rgb(55, 65, 81);
  color: #facc15; /* yellow for contrast */
}
```

I also switched headings and text colors to Tailwind classes. Finally, things looked consistent.

## Final Thoughts

What I thought would be a 15-minute task ended up being a full mini-project. Along the way I:

* Broke Tailwind.
* Fought TypeScript about `null`.
* Got schooled by Astro’s image imports.
* And finally, had to wrangle global CSS into something dark-mode friendly.

But now it works: dark mode toggle, persistent theme, clean text contrast. Honestly, it feels good to click that little moon and watch the blog flip into hacker mode.

Next time I won’t underestimate “just add dark mode.” It’s never just dark mode.