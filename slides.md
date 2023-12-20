---
theme: apple-basic
class: text-center
highlighter: shikiji
transition: slide-left
title: Modern CSS
mdc: true
---

# Modern CSS

Stop doing things the hard (old) way

<!-- A lot of you are probably just starting your career or still learning. You probably find your CSS solutions on some 7yr+ old stackoverflow post.  -->

---

# Agenda

<toc></toc>

---

# Kaleb Ercanbrack

https://twitch0125.github.io/

- JS Dev for 4 years
- Design nerd

<v-click>

Not a CSS Expert

</v-click>

<!-- I love everything around Javascript and especially the frontend. I'm not dis-interested in backend, but I always tie it back to how it benefits the browser (and thus the user). I also really like UX design/research and I'll be bringing up some design terminology. I love the idea of making people's lives easier even if its just a small interaction on a website. I also believe the user's browser is their own tool/extension of themselves so we should allow them to use it how they'd please. <br>
Please call me out on anything that seems wrong or when I'm being dumb. I would love for this to be an open discussion. -->

---

# Credits

Go to these people/sites and you'll get 99.9% of what I'm gonna talk about.

- Every Layout https://every-layout.dev/
- Utopia https://utopia.fyi/
- Cube CSS https://cube.fyi/
- SmollCSS https://smolcss.dev/
- Kevin Powell https://www.youtube.com/@KevinPowell
- Andy Bell https://twitter.com/belldotbz

---

# What is CSS?

<v-clicks>

Cascading Style Sheets.

Text instructions you download to tell your browser how to render things.

_flexible_ and **resilient**.

F#&*%ing hard.

</v-clicks>

<!-- CSS may be the hardest part of the web to use effectively. There's a lot of nice hammers out there though (css in js anyone?) -->

---

# Flexibility

A lot of the time you don't know the devices your users will be using.

You don't know how they're using their browser.

- Default OpenDyslexic Font, Reader Mode, split-screen, picture in picture mode,
  on a TV, in the car, on a limited network, zoomed in/out, Multiple tabs open,
  using a screen reader, keyboard only navigation, eye-tracking software.

Could even be a robot.

<v-click>

## We **NEED** to get out of the way

</v-click>

<!-- A person's livlihood could be made on a browser. They spend all day interacting with a specific website, and everyone will be using it differently. In the prisons they have tablets with education systems that are all offline websites. This isn't strictly CSS related either.

Generally if we get the responsivenss down then the app is fairly usable. -->

---
layout: center
---

# Be the browser's mentor, not its micromanager.

https://buildexcellentwebsit.es/
![QR code for buildexcellentwebsit.es](/buildexcellentwebsites.png)

<!-- This will demo flexibility. Everyone is gonna have a slightly different phone. Reiterate the flexibility slide.

Think of it as automating decisions for you. -->

---
layout: center
---

# My example

https://coffee-app.pages.dev/
![QR code for my coffee app website](/coffeeapp.png)

<!-- point out the flexibility of the sidebars. Point out the awkwardsness, but thats okay because its worth a little funkiness for an incredibly flexible experience IMO.

There are no breakpoints anywhere in the CSS. The most annoying part of tailwind was having a bunch of sm: md: etc-->

---

# Recent CSS improvements

css nesting,`:has()`, color-mix()

```css
ul {
  li {
    color: var(--list-text-color, green);
    &[data-error] {
      color: var(--list-text-color-error, red);
    }
  }
  &:has(li[data-error]) {
    background-color: color-mix(in srgb, var(--list-text-color-error, red), #000);
  }
}
```

Do you even need SASS anymore???

<!-- you can copy/paste that into the browser and it'll work. VSCode might freak out though. -->

---

# Code time!

1. Utilities and Design Tokens are handled by UnoCSS
2. Templating handled by Vue and Nuxt
