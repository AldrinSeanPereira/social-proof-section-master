# Frontend Mentor - Social proof section solution

This is a solution to the [Social proof section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-proof-section-6e0qTv_bA). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout for the section depending on their device's screen size

### Screenshot

![screenshot of desktop version](/images/social-proof-section-master.png)

### Links

- Solution URL: [link](https://github.com/AldrinSeanPereira/social-proof-section-master)
- Live Site URL: [link](https://chipper-jelly-335c32.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

This project surprised me in areas I never expected 
- Creating the stars for the reviews
- Learning about **Developer Tools** which is extremely helpful for CSS Grid layout
- using CSS Grid for the layouts especially for the ratings and testimonies

The code for the stars is just insanely interesting
```html
<div class="ratings__stars" style="--rating: 5;" aria-label="Rating of this product is 5 out of 5."></div>
```

```css
.ratings__stars {
    --percent: calc(var(--rating) / 5 * 100%);

    display: inline-block;
    font-size: var(--star-size);
    font-family: Times;
    /* make sure ★ appears correctly */
    line-height: 1;

    display: flex;
    justify-content: center;
    align-items: center;

    margin-bottom: var(--space-5px);
}

.ratings__stars::before {
    content: '★★★★★';
    letter-spacing: var(--star-spacing);
    background: linear-gradient(90deg,
            var(--star-background) var(--percent),
            var(--star-color) var(--percent));
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
```

The code for background images was also a new learning point

```css

background-color: var(--color-White);
    background-image: url(images/bg-pattern-top-mobile.svg),
        url(images/bg-pattern-bottom-mobile.svg);
    background-repeat: no-repeat, no-repeat;
    background-position: top center, bottom center;

```

CSS Grid code was posiible only because I used the Developer tools to see what line had what number and had to use trial-and-error to set a good positioning value

### Useful resources

- For the stars:
  - [Article link](https://css-tricks.com/five-methods-for-five-star-ratings/) - This helped me learn what strategies were possible. I finally went with using Unicode characters in pseudo-elements.
- Background images:
  - [How to use multiple background images](https://www.w3schools.com/cssref/pr_background-image.php)
  - [To understand how to position background images](https://www.w3schools.com/cssref/pr_background-position.php)
  - [How to control background image repeating](https://www.w3schools.com/cssref/pr_background-repeat.php)

- CSS Grid reference:
  - [Dave Gray video](https://www.youtube.com/watch?v=EaWj2AWI5Es) - start here. ***Especially important to learn how to use Developer Tools***
  - [Kevin Powell video](https://youtu.be/rg7Fvvl3taU?si=-5Q8rMqYVUc1aXx-) - to gain more context and understanding

## Author

- GitHub - [@AldrinSeanPereira](https://github.com/AldrinSeanPereira)
- Frontend Mentor - [@AldrinSeanPereira](https://www.frontendmentor.io/profile/AldrinSeanPereira)
- LinkedIn - [@yourusername](https://www.linkedin.com/in/aldrinseanpereira)

## Acknowledgments

I sincerely thank frontend mentor for this project and for the platform they have provided for learning.