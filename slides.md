---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/KdeqA3aTnBY/1600x900
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
---

# Behavior Driven Development (BDD)

With Gerkin

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 p-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<a href="https://github.com/localgod/bbd_presentation" target="_blank" alt="GitHub"
  class="abs-br m-6 text-xl icon-btn opacity-50 !border-none !hover:text-white">
  <carbon-logo-github />
</a>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# BDD ehh?

- <uim-rocket class="tytter" /> Behaviour-driven Development (BDD) is an agile methodology, that has roots in Test Driven Development (TDD) and Domain Driven Design (DDD)

<v-clicks>

- It builds on the idea, that all requirements should be accompanied by an acceptance test criteria
- And in fact, could both be the same
- And while we are at it, they can be automated.

</v-clicks>
<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
.tytter {
  display:inline;
}
</style>

---
layout: image-left
image: https://source.unsplash.com/3ROwc3JSjCk/1600x900
---

# Never heard of it...

- Actually based on the ideas introduced in 1997 (by a bank)

<v-clicks>

- Then called Feature-driven development (FDD)
- There where not really any tools for it then
- But it introduced ideas that sparked many of the agile methodologies and tools used today 

</v-clicks>


---
layout: image-left
image: https://source.unsplash.com/Gej8FOFLlHg/1600x900
---

# Code

Kiss Gherkin...

<!-- https://sli.dev/guide/syntax.html#line-highlighting -->

```gherkin
    Background: Navigate to page
        Given I am on page one
        When I click the “page 2” button
        Then I see “page 2”

    Scenario Outline: Make button go away
        Given <BUTTON> button exists
        When I click the <BUTTON> button
        Then I see the <BUTTON> button disappear

        Examples:
            | BUTTON |
            | first  |
            | second |
            | third  |
```

<arrow v-click="3" x1="400" y1="420" x2="230" y2="330" color="#564" width="3" arrowSize="1" />

---
layout: image-right
image: https://source.unsplash.com/XzuJuyYLjmE/1600x900
---

# What is Gherkin?

- Domain Specific Language
- Business Readable
- Created especially fordescribing behaviour
- Originally created in the ruby community
- The first parser was called Cucumber

---
layout: default
---

# Why should I care?

- Document features in legacy systems
- Regression testing
- Live, verified product requirement specification

<img src="https://www.nowsecure.com/wp-content/uploads/2017/05/NIST-relative-cost-to-fix-a-flaw.png" alt="drawing" width="400"/>

---
preload: false
---

# Animations

Animations are powered by [@vueuse/motion](https://motion.vueuse.org/).

```html
<div
  v-motion
  :initial="{ x: -80 }"
  :enter="{ x: 0 }">
  Slidev
</div>
```

<div class="w-60 relative mt-6">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-square.png"
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-circle.png"
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-triangle.png"
    />
  </div>

  <div 
    class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Slidev
  </div>
</div>

<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x:35, y: 40, opacity: 0}"
  :enter="{ y: 0, opacity: 1, transition: { delay: 3500 } }">

[Learn More](https://sli.dev/guide/animations.html#motion)

</div>

---

# LaTeX

LaTeX is supported out-of-box powered by [KaTeX](https://katex.org/).

<br>

Inline $\sqrt{3x-1}+(1+x)^2$

Block
$$
\begin{array}{c}

\nabla \times \vec{\mathbf{B}} -\, \frac1c\, \frac{\partial\vec{\mathbf{E}}}{\partial t} &
= \frac{4\pi}{c}\vec{\mathbf{j}}    \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\

\nabla \times \vec{\mathbf{E}}\, +\, \frac1c\, \frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\

\nabla \cdot \vec{\mathbf{B}} & = 0

\end{array}
$$

<br>

[Learn more](https://sli.dev/guide/syntax#latex)

---

# Diagrams

You can create diagrams / graphs from textual descriptions, directly in your Markdown.

<div class="grid grid-cols-2 gap-4 pt-4 -mb-6">

```mermaid {scale: 2.0}
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Create            :done,    des1, 2014-01-06,2014-01-08
Tweak              :active,  des2, 2014-01-09, 3d
Trim               :         des3, after des2, 5d
Release               :         des4, after des3, 5d
```

</div>

[Learn More](https://sli.dev/guide/syntax.html#diagrams)


---
layout: center
class: text-center
---

# Learn More

[Documentations](https://sli.dev) / [GitHub Repo](https://github.com/slidevjs/slidev)
