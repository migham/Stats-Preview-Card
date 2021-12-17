# Frontent Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://github.com/migham/Stats-Preview-Card/blob/master/screenshots/Screenshot%202021-12-16%20at%2020-46-05%20Stats%20Preview%20Cards.png).

![Design preview for the Stats preview card component coding challenge](./screenshots/desktop.png)

## Table of contents

- [Frontent Mentor - Stats preview card component solution](#frontent-mentor---stats-preview-card-component-solution)
	- [Table of contents](#table-of-contents)
	- [Overview](#overview)
		- [Screenshot](#screenshot)
			- [Desktop version](#desktop-version)
			- [Mobile version](#mobile-version)
		- [Links](#links)
	- [My Process](#my-process)
		- [Built with](#built-with)
		- [What I learned](#what-i-learned)
		- [Useful resources](#useful-resources)

## Overview

### Screenshot

#### Desktop version
![Desktop version](./screenshots/desktop.png)

#### Mobile version
![Mobile version](screenshots/mobile.png)

### Links
* Solution URL: [Github repository](https://github.com/migham/Stats-Preview-Card)
* Live Site URL: [Github Page](https://migham.github.io/Stats-Preview-Card/)

## My Process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

It was very useful for me to go deeper into flexbox, to be able to change the flow-direction through media query and in turn go from display: flex to display: block in the body to align the elements.

For some strange reason, I had to use linear-gradient to be able to add a translucent color to the image, instead of simply using the shorthand background, which did not allow me to add color [as explained here](https://stackoverflow.com/questions/903659/why-cant-i-use-background-image-and-color-together) where it is used:
```css
background-color: green; /*i replaced it with an alpha layer */
background-image: url(images/shadow.gif);
background-position: right;
background-repeat: no-repeat;
```

but I had to opt for the following solution

```css
:root{
	...
	--accent-t: hsla(277, 75%, 30%, 0.6);
	...
}

.image-header{
	...
	background-image:linear-gradient(
		var(--accent-t), 
		var(--accent-t)), 
		url(./images/image-header-desktop.jpg);
	...
}

```

If someone can explain why, I would be very grateful!

### Useful resources

- [The peculiar magic of flexbox and auto margins](https://css-tricks.com/the-peculiar-magic-of-flexbox-and-auto-margins/): Helped me better understand element centering using flexbox.
- [CSS para oscurecer o colorear una imagen](https://comolademo.es/css-oscurecer-colorear-imagen/) This was the solution I ended up using to add a filter.

---
Thanks for readme!