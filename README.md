Conditionnal Responsive Lightbox
================================

This is a conditionnal lightbox that is and extension of Brad Frost's article <a href="http://bradfrostweb.com/blog/post/conditional-lightbox/">Conditional Lightbox</a> and <a href="http://codepen.io/bradfrost/full/tfCAp">codepen demo </a>

You can <a href="http://inpixelitrust.fr/demos/conditionnal-responsive-lightbox/">see a demo online.</a>

It is based on media queries detections so that smaller devices that support media queries won't open the lightbox (read the article for further explanation)

1. We check if there is a media queries support, using the CSS part   @media all and (min-width: 1em) and (max-width: 45em) and adding a "mqsupport" to the body. For browsers like old IEs that don't support media queries, we just open the lightbox, assuming they've a fixed width container (instead of max-width)
2. If the viewport size is bigger than 45em, we use @media all and (min-width: 45em) to add the "widescreen" content to the body
3. using JS, we will display or not the lightbox depending on mq support and screen size.

The script automatically finds all the links that link to a .png, .jpg or .gif file, and add the class that the lightbox needs.

We could also use the e.preventDefault(); to make the image not be opened in the browser for smaller screens

The lightbox is placed given to the user scroll.

Warning : This is a pretty messed up technique. Seriously. Chrome sends back widescreen and Firefox sends back "widescreen" (yes with the double quotes) as value of var size. This forces use to make two tests. So use it at your own risks :) 

