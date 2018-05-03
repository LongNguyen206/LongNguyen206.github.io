# My portfolio website ![code quality](https://img.shields.io/badge/code-5%2F5-brightgreen.svg) ![responsiveness](https://img.shields.io/badge/responsiveness-excellent-brightgreen.svg) ![jquery](https://img.shields.io/badge/jQuery%20used-1-blue.svg)

> *This website was created by **Long Nguyen** for the Gentech portfolio project*

### Visit me at [longnguyen206.github.io](https://longnguyen206.github.io)


## Project goals
> Keep it simple!

Learning from my previous assignment, the website was planned to be simple yet complete in time. I did not use **Bootstrap** or any other frameworks and limited the use of jQuery to one single script -  [smooth scrolling](https://css-tricks.com/snippets/jquery/smooth-scrolling/).

The main takeaway for me was to learn how to make my websites **responsive** on any device.

## Design

The design process included:

* Googling other people's portfolio websites
* Selecting top 3 good-but-simple-looking pages
* Dissecting their HTML and CSS via browser's 'Inspect' tool to see how things work

To draw the wireframe, I simply used pen and paper as I found this method easier. As you can see, the final design is slightly different from the initial plan
![wireframe](https://github.com/LongNguyen206/LongNguyen206.github.io/blob/master/wireframe.jpg)

As the motto was to keep things simple, the website is split into 6 simple, page-wide, horizontal sections:

* Hero section
* About me
* My education
* My stack
* Portfolio
* Footer

The navigation is done through scrolling and there is no navigation bar. This was made intentionally as the sections are pretty short right now. The navbar is something to be considered in the future when the website will have more content.

The choice of fonts and colors are the result of many trial and errors (but mostly googling). 

The icons are scaled upon hovering via

```
img:hover {
    transform: scale(1.1);
}
```

And a 'transition' property is added to the icon element to ease the animation: 

```
img {
    transition: transform .2s;
}
```

## Encountered difficulties
### Hero section
The hero section was the most enjoyable part to create as the layout is quite simple. The background image is planned to be replaced with something more 'tech-related' in the future. There is actually a gray semi-transparent layer over the photo to make the text more readable:

```
.home-hero:before { # the following properties go before the '.home-hero' element
    ...             # you have to include a bunch of other properties also
    background-image: linear-gradient(90deg, rgba(49, 61, 65, 0.6), rgba(49, 61, 65, 0.6))
}
```

All the logos and text in the section is responsive to the width of the browser/device.

### 'About me' section

The section is split into 2 equal horizontal halves at 48% width each.
 
Although this section looks simple, the issue lied with the text alignment on small devices. When viewed on phones, the text should be aligned to the center as opposed to the default right-side alignment.

### 'Portfolio' section

The button animation is simply the colors and paddings changing when hovered

```
button:hover {
    padding: 1.2rem 4.0rem; # only side padding is increased at the hover to give the 'enlarge' effect
    color: yellow; # colors are changed
    background-color: black;
    border: 2px solid black; 
}
```
### Footer

Another aesthetic problem I got was the ugly outline around clickables when clicked. I managed to get rid of it by using

```
a:active {
    outline:0;
}
```

## Responsiveness

All the images and texts scale up and down with the browser's width. Much of the responsiveness is achieved automatically via **'viewport' meta tag**:

```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

However **@media queries** were also used to account for specific elements. The 3 screen widths that were considered are: 350 pixels (most phones), 550 pixels (tablets), 750 pixels and 1000 pixels.

## Intended audience

Anyone who cares, mostly my Gentech comrades.

## Usability heuristics

The website tried to follow most of the [usability heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) and is at least consistent with the following:

* Consistency and standards
* Error prevention
* Flexibility and efficiency of use
* Aesthetic and minimalist design
* Help and documentation (this README)

## Media used

* Most logos came from Google images. I specifically looked for logos with transparent backgrounds. Where the background was not transparent, I used [GIMP](https://www.gimp.org/) for Ubuntu to remove the background

* The personal logo was made in [Canva](https://www.canva.com/)

* The social media icons come form [Fontawesome](https://fontawesome.com/)

* The project's GIF was recorded with [Peek](https://www.omgubuntu.co.uk/2018/03/peek-snap-app-discontinued) for Ubuntu

* Hero background photo made by me
