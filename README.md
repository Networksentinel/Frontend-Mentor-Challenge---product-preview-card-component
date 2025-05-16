# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![](./public/images/project%20screenshot.png)

### Links

- [Solution URL](https://your-solution-url.com)
- [Live Site](https://networksentinel.github.io/Frontend-Mentor-Challenge---product-preview-card-component/)

## My process

### Built with

- Semantic HTML5 markup
- Sass/SCSS - modular approach, variables + mixins
- Flexbox
- Mobile-first workflow
- [Vite](https://vite.dev/) - Build tool

### What I learned

This wasn’t just a simple `clamp()` fix — the design needed the component to start small on phones, get bigger by tablet size, then shrink a bit, and finally grow again on bigger screens. 

**It was kind of tricky, but I made it work by mixing `@media` queries with `clamp()`. The layout feels smooth and responsive, and it really matches the Figma design closely.**
Here is an example:

```scss
.card {
    width: 93.33vw;
    overflow: hidden;
    
    margin-top: 21.3333vw;
    margin-bottom: 45.8666vw;

    display: flex;
    flex-direction: column;
    align-items: center;

    border-radius: $space-100;

    @media (min-width: $breakpoint-tablet) {
        width: clamp(21.875rem, 78.125vw, 37.5rem);
        margin: clamp(5rem, 37.3046875vw, 17.90625rem) 0;
        flex-direction: row;       
}
}
```

### Continued development

In future projects I need to commit more often in Git, and be more intentional with it. Like, really think about what each change is doing to the layout or visuals, and pick a commit message/label that fits.