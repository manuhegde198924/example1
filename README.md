# example1

HOSTED LINK OF PROJECT:https://manuhegde198924.github.io/example1/
HTML PARTCSS PART AND MEDIA QUEIRIES
https://github.com/manuhegde198924/example1/issues/1





 
Media Types in CSS: There are many types of media types which are listed below:

    all: It is used for all media devices
    print: It is used for printer.
    screen: It is used for computer screens, smartphones, etc.
    speech: It is used for screen readers that read the screen aloud.

Features of Media query: There are many features of media query which are listed below:

    color: The number of bits per color component for the output device.
    grid: Checks whether the device is grid or bitmap.
    height: The viewport height.
    aspect ratio: The ratio between width and height of the viewport.
    color-index: The number of colors the device can display.
    max-resolution: The maximum resolution of the device using dpi and dpcm.
    monochrome: The number of bits per color on a monochrome device.
    scan: The scanning of output devices.
    update: How quickly can the output device modify.
    width: The viewport width.
Responsive design is an approach to web design that makes your web content adapt to the different screen and window sizes of a variety of devices.

For example, your content might be separated into different columns on desktop screens, because they are wide enough to accommodate that design.

If you separate your content into multiple columns on a mobile device, it will be hard for users to read and interact with.

Responsive design makes it possible to deliver multiple, separate layouts of your content and design to different devices depending on screen size.

The difference between responsive design and adaptive design is that responsive design adapts the rendering of a single page version. In contrast, adaptive design delivers multiple completely different versions of the same page.
If you’re new to web design, development, or blogging, you might wonder why responsive design matters in the first place.

The answer is simple. It’s no longer enough to design for a single device. Mobile web traffic has overtaken desktop and now makes up the majority of website traffic, accounting for more than 51%.
Mobile, tablet, desktop market share
Mobile, tablet, desktop market share

When over half of your potential visitors are using a mobile device to browse the internet, you can’t just serve them a page designed for desktop. It would be hard to read and use, and lead to bad user experience.

But that’s not all. Users on mobile devices also make up the majority of search engine visits.
Mobile search traffic
Mobile search traffic

Finally, over the last few years, mobile has become one of the most important advertising channels. Even in a post-pandemic market, mobile ad spending is growing 4.8% to $91.52 billion.

Whether you choose to advertise on social media or use an organic approach like YouTube SEO, the vast majority of your traffic will come from mobile users.

If your landing pages aren’t optimized for mobile and easy to use, you won’t be able to maximize the ROI of your marketing efforts. Bad conversion rates will lead to fewer leads and wasted ad spend.
What is The Viewport?

The viewport is the user's visible area of a web page.

The viewport varies with the device, and will be smaller on a mobile phone than on a computer screen.

Before tablets and mobile phones, web pages were designed only for computer screens, and it was common for web pages to have a static design and a fixed size.

Then, when we started surfing the internet using tablets and mobile phones, fixed size web pages were too large to fit the viewport. To fix this, browsers on those devices scaled down the entire web page to fit the screen.

This was not perfect!! But a quick fix.
Setting The Viewport

HTML5 introduced a method to let web designers take control over the viewport, through the <meta> tag.

You should include the following <meta> viewport element in all your web pages:
<meta name="viewport" content="width=device-width, initial-scale=1.0">

This gives the browser instructions on how to control the page's dimensions and scaling.

The width=device-width part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).

The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.

Here is an example of a web page without the viewport meta tag, and the same web page with the viewport meta tag:



Without the viewport meta tag



With the viewport meta tag

Tip: If you are browsing this page with a phone or a tablet, you can click on the two links above to see the difference.
Size Content to The Viewport

Users are used to scroll websites vertically on both desktop and mobile devices - but not horizontally!

So, if the user is forced to scroll horizontally, or zoom out, to see the whole web page it results in a poor user experience.

Some additional rules to follow:

1. Do NOT use large fixed width elements - For example, if an image is displayed at a width wider than the viewport it can cause the viewport to scroll horizontally. Remember to adjust this content to fit within the width of the viewport.

2. Do NOT let the content rely on a particular viewport width to render well - Since screen dimensions and width in CSS pixels vary widely between devices, content should not rely on a particular viewport width to render well.

3. Use CSS media queries to apply different styling for small and large screens - Setting large absolute CSS widths for page elements will cause the element to be too wide for the viewport on a smaller device. Instead, consider using relative width values, such as width: 100%. Also, be careful of using large absolute positioning values. It may cause the element to fall outside the viewport on small devices.

The Building Blocks of Responsive Web Design:

The foundation of responsive design is the combination of HTML and CSS, two languages that control the content and layout of a page in any given web browser.
html vs css
HTML vs CSS (Image source: codingdojo.com)

HTML mainly controls the structure, elements, and content of a webpage. For example, to add an image to a website, you have to use HTML code like this:

<img src="image.gif" alt="image" class=”full-width-img”>

You can set a “class” or “id” that you can later target with CSS code.

You could also control primary attributes such as height and width within your HTML, but this is no longer considered best practice.

Instead, CSS is used to edit the design and layout of the elements you include on a page with HTML. CSS code can be included in a <style> section of a HTML document, or as a separate stylesheet file.

For example, we could edit the width of all HTML images at the element level like this:

img {
width: 100%;
}

Or we could target the specific class “full-width-img” by adding a period in front.

.full-width-img {
width: 100%;
}
Responsive Web Design - Images

Resize the browser window to see how the image scales to fit the page.
Using The width Property

If the width property is set to a percentage and the height property is set to "auto", the image will be responsive and scale up and down:
Example
img {
  width: 100%;
  height: auto;
}

Notice that in the example above, the image can be scaled up to be larger than its original size. A better solution, in many cases, will be to use the max-width property instead.
Using The max-width Property

If the max-width property is set to 100%, the image will scale down if it has to, but never scale up to be larger than its original size:
Example
img {
  max-width: 100%;
  height: auto;
}
Add an Image to The Example Web Page
Example
img {
  width: 100%;
  height: auto;
}
Background Images

Background images can also respond to resizing and scaling.

Here we will show three different methods:

1. If the background-size property is set to "contain", the background image will scale, and try to fit the content area. However, the image will keep its aspect ratio (the proportional relationship between the image's width and height):

Here is the CSS code:
Example
div {
  width: 100%;
  height: 400px;
  background-image: url('img_flowers.jpg');
  background-repeat: no-repeat;
  background-size: contain;
  border: 1px solid red;
}

2. If the background-size property is set to "100% 100%", the background image will stretch to cover the entire content area:

Here is the CSS code:
Example
div {
  width: 100%;
  height: 400px;
  background-image: url('img_flowers.jpg');
  background-size: 100% 100%;
  border: 1px solid red;
}

3. If the background-size property is set to "cover", the background image will scale to cover the entire content area. Notice that the "cover" value keeps the aspect ratio, and some part of the background image may be clipped:

Here is the CSS code:
Example
div {
  width: 100%;
  height: 400px;
  background-image: url('img_flowers.jpg');
  background-size: cover;
  border: 1px solid red;
}
Different Images for Different Devices

A large image can be perfect on a big computer screen, but useless on a small device. Why load a large image when you have to scale it down anyway? To reduce the load, or for any other reasons, you can use media queries to display different images on different devices.

Here is one large image and one smaller image that will be displayed on different devices:
Example
/* For width smaller than 400px: */
body {
  background-image: url('img_smallflower.jpg');
}

/* For width 400px and larger: */
@media only screen and (min-width: 400px) {
  body {
    background-image: url('img_flowers.jpg');
  }
}

The Media query in CSS is used to create a responsive web design. It means that the view of a web page differs from system to system based on screen or media types. The breakpoint specifies for what device-width size, the content is just starting to break or deform.

Media queries can be used to check many things:

    width and height of the viewport
    width and height of the device
    Orientation
    Resolution

A media query consist of a media type that can contain one or more expression which can be either true or false. The result of the query is true if the specified media matches the type of device the document is displayed on. If the media query is true then a style sheet is applied.

Syntax:

@media not | only mediatype and (expression) {
    // Code content
}

Example: This example illustrates the CSS media query with the different device-width for making it responsive.

<!DOCTYPE html>
<html>
 
<head>
    <title>CSS media query</title>
    <style>
        body {
            text-align: center;
        }
 
        .gfg {
            font-size: 40px;
            font-weight: bold;
            color: green;
        }
 
        @media screen and (max-width:800px) {
            body {
                text-align: center;
                background-color: green;
            }
 
            .gfg {
                font-size: 30px;
                font-weight: bold;
                color: white;
            }
 
            .geeks {
                color: white;
            }
        }
 
        @media screen and (max-width:500px) {
            body {
                text-align: center;
                background-color: blue;
            }
        }
    </style>
</head>
 
<body>
    <div class="gfg">
        GeeksforGeeks
    </div>
    <div class="geeks">
        A computer science portal for geeks
    </div>
</body>
 
</html>

Output: From the output, we can see that if the max-width of the screen is reduced to 800px then the background color changes to green & if the max-width of the screen is reduced to 500px then the background color will turn to blue. For the desktop size width, the background color will be white.

Media Types in CSS: There are many types of media types which are listed below:

    all: It is used for all media devices
    print: It is used for printer.
    screen: It is used for computer screens, smartphones, etc.
    speech: It is used for screen readers that read the screen aloud.

Features of Media query: There are many features of media query which are listed below:

    color: The number of bits per color component for the output device.
    grid: Checks whether the device is grid or bitmap.
    height: The viewport height.
    aspect ratio: The ratio between width and height of the viewport.
    color-index: The number of colors the device can display.
    max-resolution: The maximum resolution of the device using dpi and dpcm.
    monochrome: The number of bits per color on a monochrome device.
    scan: The scanning of output devices.
    update: How quickly can the output device modify.
    width: The viewport width.
You can use the media query min-device-width, instead of min-width, which checks the device width, instead of the browser width. Then the image will not change when you resize the browser window:
Example
/* For devices smaller than 400px: */
body {
  background-image: url('img_smallflower.jpg');
}

/* For devices 400px and larger: */
@media only screen and (min-device-width: 400px) {
  body {
    background-image: url('img_flowers.jpg');
  }
}
The HTML <picture> Element

The HTML <picture> element gives web developers more flexibility in specifying image resources.

The most common use of the <picture> element will be for images used in responsive designs. Instead of having one image that is scaled up or down based on the viewport width, multiple images can be designed to more nicely fill the browser viewport.

The <picture> element works similar to the <video> and <audio> elements. You set up different sources, and the first source that fits the preferences is the one being used:
Example
<picture>
  <source srcset="img_smallflower.jpg" media="(max-width: 400px)">
  <source srcset="img_flowers.jpg">
  <img src="img_flowers.jpg" alt="Flowers">
</picture>

The srcset attribute is required, and defines the source of the image.

The media attribute is optional, and accepts the media queries you find in CSS @media rule.

You should also define an <img> element for browsers that do not support the <picture> element.

You can also control the design beyond just height, width, and color. Using CSS like this is how you make a design responsive when you combine it with a technique called media query.
Media Queries

A media query is a fundamental part of CSS3 that lets you render content to adapt to different factors like screen size or resolution.
media queries - responsive web design
Media queries for desktop, tablet, smartphone

It works in a similar way to an “if clause” in some programming languages, basically checking if a screen’s viewport is wide enough or too wide before executing the appropriate code.

@media screen and (min-width: 780px) {
.full-width-img {
margin: auto;
width: 90%;
}

If the screen is at least 780 pixels wide, “full-width-img” class images will take up 90% of the screen and be automatically centered by equally wide margins.
Fluid Layouts

A fluid layout is an essential part of modern responsive design. In the good old days, you would set a static value for every HTML element, like 600 pixels.

A fluid layout relies instead on dynamic values like a percentage of the viewport width.
fluid layout - responsive web design
Example of fluid layout

This approach will dynamically increase or decrease the different container element sizes based on the size of the screen.
Flexbox Layout

While a percentage-based layout is fluid, many designers and web developers felt it was not dynamic or flexible enough. Flexbox is a CSS module designed as a more efficient way to lay out multiple elements, even when the size of the contents inside the container is unknown.

A flex container expands items to fill available free space or shrinks them to prevent overflow. These flex containers have a number of unique properties, like justify-content, that you can’t edit with a regular HTML element.
flexbox justify
Flexbox container

It’s a complicated topic, so if you want to use it in your design, you should read CSS Tricks’ flexbox guide.
Responsive Images

The most basic iteration of responsive images follows the same concept as a fluid layout, using a dynamic unit to control the width or height. The sample CSS code we covered earlier already accomplishes this:

img {
width: 100%;
}

The % unit approximates to a single percentage of the width or height of the viewport and makes sure the image remains in proportion to the screen.

The problem with this approach is that every user has to download the full-sized image, even on mobile.

To serve different versions scaled for different devices, you need to use the HTML srcset attribute in your img tags, to specify more than one image size to choose from.

<img srcset="large-img.jpg 1024w,
middle-img.jpg 640w,
small-img.jpg  320w"
src="small.jpg"
/>

WordPress automatically uses this functionality for images included in posts or pages.
Speed

When you’re attempting to create a responsive design for your website, the loading speed should be a top priority.

Pages that load in 2 seconds have an average 9% bounce rate, while pages that take 5 seconds lead to a 38% bounce rate.

Your approach to responsiveness must not block or delay your page’s first render any more than it needs to.

There are several ways you could make your pages faster. Optimizing your images, implementing caching, minification, using a more efficient CSS layout, avoiding render-blocking JS, and improving your critical rendering path are all great ideas you should consider.

Kinsta customers have access to a quick and easy way to accomplish this by using the code minification feature that is built right into the MyKinsta dashboard, allowing customers to enable automatic CSS and JavaScript minification with a simple click.

You could also try to implement Google AMP for your mobile pages, but in our Google AMP case study, our mobile leads dropped by a whopping 59%.
Common Responsive Breakpoints

To work with media queries, you need to decide on the “responsive breakpoints” or screen size breakpoints. A breakpoint is the width of the screen where you use a media query to implement new CSS styles.
Common screen sizes

    Mobile: 360 x 640
    Mobile: 375 x 667
    Mobile: 360 x 720
    iPhone X: 375 x 812
    Pixel 2: 411 x 731
    Tablet: 768 x 1024
    Laptop: 1366 x 768
    High-res laptop or desktop: 1920 x 1080

If you choose a mobile-first approach to design, with a single column and smaller font sizes as the basis, you don’t need to include mobile breakpoints — unless you want to optimize the design for specific models.
mobile first - responsive web design
Mobile-first design (Image source: silocreativo.com)

So you can create a basic responsive design with just two breakpoints, one for tablets and one for laptops and desktop computers.
What is a Media Query?

Media query is a CSS technique introduced in CSS3.

It uses the @media rule to include a block of CSS properties only if a certain condition is true.
Example

If the browser window is 600px or smaller, the background color will be lightblue:
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
Add a Breakpoint

Earlier in this tutorial we made a web page with rows and columns, and it was responsive, but it did not look good on a small screen.

Media queries can help with that. We can add a breakpoint where certain parts of the design will behave differently on each side of the breakpoint.

Desktop

Phone

Use a media query to add a breakpoint at 768px:
Example

When the screen (browser window) gets smaller than 768px, each column should have a width of 100%:
/* For desktop: */
.col-1 {width: 8.33%;}
.col-2 {width: 16.66%;}
.col-3 {width: 25%;}
.col-4 {width: 33.33%;}
.col-5 {width: 41.66%;}
.col-6 {width: 50%;}
.col-7 {width: 58.33%;}
.col-8 {width: 66.66%;}
.col-9 {width: 75%;}
.col-10 {width: 83.33%;}
.col-11 {width: 91.66%;}
.col-12 {width: 100%;}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  [class*="col-"] {
    width: 100%;
  }
}
ADVERTISEMENT
Always Design for Mobile First

Mobile First means designing for mobile before designing for desktop or any other device (This will make the page display faster on smaller devices).

This means that we must make some changes in our CSS.

Instead of changing styles when the width gets smaller than 768px, we should change the design when the width gets larger than 768px. This will make our design Mobile First:
Example
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
  .col-1 {width: 8.33%;}
  .col-2 {width: 16.66%;}
  .col-3 {width: 25%;}
  .col-4 {width: 33.33%;}
  .col-5 {width: 41.66%;}
  .col-6 {width: 50%;}
  .col-7 {width: 58.33%;}
  .col-8 {width: 66.66%;}
  .col-9 {width: 75%;}
  .col-10 {width: 83.33%;}
  .col-11 {width: 91.66%;}
  .col-12 {width: 100%;}
}
Another Breakpoint

You can add as many breakpoints as you like.

We will also insert a breakpoint between tablets and mobile phones.

Desktop

Tablet

Phone

We do this by adding one more media query (at 600px), and a set of new classes for devices larger than 600px (but smaller than 768px):
Example

Note that the two sets of classes are almost identical, the only difference is the name (col- and col-s-):
/* For mobile phones: */
[class*="col-"] {
  width: 100%;
}

@media only screen and (min-width: 600px) {
  /* For tablets: */
  .col-s-1 {width: 8.33%;}
  .col-s-2 {width: 16.66%;}
  .col-s-3 {width: 25%;}
  .col-s-4 {width: 33.33%;}
  .col-s-5 {width: 41.66%;}
  .col-s-6 {width: 50%;}
  .col-s-7 {width: 58.33%;}
  .col-s-8 {width: 66.66%;}
  .col-s-9 {width: 75%;}
  .col-s-10 {width: 83.33%;}
  .col-s-11 {width: 91.66%;}
  .col-s-12 {width: 100%;}
}

@media only screen and (min-width: 768px) {
  /* For desktop: */
  .col-1 {width: 8.33%;}
  .col-2 {width: 16.66%;}
  .col-3 {width: 25%;}
  .col-4 {width: 33.33%;}
  .col-5 {width: 41.66%;}
  .col-6 {width: 50%;}
  .col-7 {width: 58.33%;}
  .col-8 {width: 66.66%;}
  .col-9 {width: 75%;}
  .col-10 {width: 83.33%;}
  .col-11 {width: 91.66%;}
  .col-12 {width: 100%;}
}

It might seem odd that we have two sets of identical classes, but it gives us the opportunity in HTML, to decide what will happen with the columns at each breakpoint:
HTML Example

For desktop:

The first and the third section will both span 3 columns each. The middle section will span 6 columns.

For tablets:

The first section will span 3 columns, the second will span 9, and the third section will be displayed below the first two sections, and it will span 12 columns:
<div class="row">
  <div class="col-3 col-s-3">...</div>
  <div class="col-6 col-s-9">...</div>
  <div class="col-3 col-s-12">...</div>
</div>
Typical Device Breakpoints

There are tons of screens and devices with different heights and widths, so it is hard to create an exact breakpoint for each device. To keep things simple you could target five groups:
Example
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...}
Orientation: Portrait / Landscape

Media queries can also be used to change layout of a page depending on the orientation of the browser.

You can have a set of CSS properties that will only apply when the browser window is wider than its height, a so called "Landscape" orientation:
Example

The web page will have a lightblue background if the orientation is in landscape mode:
@media only screen and (orientation: landscape) {
  body {
    background-color: lightblue;
  }
}
Hide Elements With Media Queries

Another common use of media queries, is to hide elements on different screen sizes:
I will be hidden on small screens.
Example
/* If the screen size is 600px wide or less, hide the element */
@media only screen and (max-width: 600px) {
  div.example {
    display: none;
  }
}
Change Font Size With Media Queries

You can also use media queries to change the font size of an element on different screen sizes:
Variable Font Size.
Example
/* If the screen size is 601px or more, set the font-size of <div> to 80px */
@media only screen and (min-width: 601px) {
  div.example {
    font-size: 80px;
  }
}

/* If the screen size is 600px or less, set the font-size of <div> to 30px */
@media only screen and (max-width: 600px) {
  div.example {
    font-size: 30px;
  }
}
CSS @media Reference

For a full overview of all the media types and features/expressions, please look at the @media rule in our CSS reference.




