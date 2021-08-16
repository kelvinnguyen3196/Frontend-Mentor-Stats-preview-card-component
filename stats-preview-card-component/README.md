# Frontend Mentor - Stats preview card component solution

This is my solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshots](#screenshots)
- [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshots

![Desktop version](images/desktop-screenshot.png)
*Desktop version*
![Mobile version](images/mobile-screenshot.png)
*Mobile version*

## My process

I started off by adding the given values from style-guide.md to the :root pseudo-element in my style.css. I then added the universal styles to the HTML elements such as font family, background color, and text color. Working on the mobile version first I grouped the elements together to make it easier to add CSS Flexbox later. Using positioning I was able to position the main card in the center of the page. I used CSS Flexbox to align elements inside other each of the group that I made. The image color overlay took a bit of trial an error with the filter functions.
### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

I found a really neat HTML tag that allows you to choose which image to display based on the user's device size.

```html
<picture>
    <!-- Mobile -->
    <source srcset="images/image-header-mobile.jpg" media="(max-width: 600px)">
    <img src="images/image-header-mobile.jpg" alt="Office colleagues laughing at something off screen">
</picture>
```
I ended up using the mobile image for both because I found that it fit better even when the user had a larger device, but I wanted to keep the HTML picture element so I could remember how useful it was.
```css
.right .overlay {
    position: absolute;
    background-color: var(--accent);
    inset: 0;
    opacity: 0.5;
    filter: brightness(0.2) saturate(7);
}
```
Using Kevin Powell's tips from the video linked below, I learned about how useful position: absolute combined with inset: 0 could be. It was very interesting how it behaved and I will definitely beusing this again in the future.

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

Some things that I could work on would be learning how to make the overlay more like the preview image. While the purple overlay that I created looked similar, I am not completely satisfied with it.

Another element that I am not completely satisfied with is how the image on the desktop version is not perfectly half of the text portion. I wanted to the image and text portion to be the exact same size, but I was a little too deep in my code when I found out it was not complete perfect.

### Useful resources

- [Kevin Powell - Best (and worst) ways to center WITHOUT flex or grid](https://youtu.be/87YMCtsBoCM) - This helped me with the color overlay. I really liked the way Kevin Powell used these CSS properties together in the video at 10:15
- [Firefox Developer Tool](https://developer.mozilla.org/en-US/docs/Tools) - This was the first time that I had downloaded Firefox to use developer tools and it was really useful! It was helpful how you can select the element from the page and developer tools will show you which CSS properties are being applied along with how large the element is due to its size, padding, and margin. I wish that I had downloaded this earlier.
```css
.inner-box {
    position: absolute;
    inset: 0;
    margin: auto;

    /* declare height and width here */
}
```

The usage of inset: 0 to allow the .inner-box element to "live" inside the containing element and margin: auto to center the .inner-box element is really clever.

## Author

- Frontend Mentor - [@kelvinnguyen3196](https://www.frontendmentor.io/profile/kelvinnguyen3196)
