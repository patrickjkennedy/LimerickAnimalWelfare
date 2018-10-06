# COMP30680 Web Application Development 
## Assignment 1: HTML and CSS

For my submission, I decided to take a charity with a mission that resonates with me and improve the design of their existing website. [Limerick Animal Welfare](http://www.limerickanimalwelfare.ie/) are a no-kill animal shelter, located approximately 30 miles from Limerick City. In addition to their animal rescue, they promote the humane treatment of animals throughout society.

In my submission, I've endeavoured to separate content and styling by using appropriate, valid HTML and CSS. In particular the assignment requested the use of the following.

### Links to both my own pages and external webpages

My navigation bar (e.g. index.html, lines 16-27) includes links to both my own pages, as well as external sites such as Facebook, Instagram and Google Maps. I also include a link to my Donate page in my landing page banner (index.html, line 33), as well as external links in my Contact page (contact.html, lines 51-58)

### A navigation bar

My navigation bar is positioned on the top of each page's layout. What differs is that I created an `active` class to highlight which page is being displayed. You can find an example of my `<nav>` element in my index page (index.html, lines 16-27).

### A least one table

I've included a table on the Donation page (donate.html, lines 36-65) listing what your money goes toward funding.

### At least one list (ordered or unordered)

My site includes two unordered lists:
1. The navigation bar is an unordered list that has been formatted with CSS.
2. The *Useful Links* section of my Contact page (contact.html, lines 53-57) is an unordered list of image links.

### At least one local or embedded video

There is an embedded Youtube video on my About page (about.html, line 36).

### At least four CSS3 and four HTML5 elements

My HTML5 specific elements include
1. A `<nav>` element (index.html, line 16)
2. A `<section>` element (index.html , line 37)
3. A `<header>` element that includes the introductory content for that page (contact.html, line 29)
4. A `<footer>` element (index.html, line 49)

My external stylesheet, styles.css, includes numerous CSS selectors and CSS properties. Some elements introduced in CSS3 are

1. `border-radius` is used to produce the rounded corners on my cards and on the 'Donate' button on the index (styles.css, line 102).

2. `opacity` is used to make the banner description tag-line more visually interesting (styles.css, line 96).

3. `box-shadow` is used to create shadows around elements (styles.css, line 192).

4. `transition` is used to change the background colour and text colour of my large Donate button (styles.css, line 105).

### Make use of the CSS positional properties (e.g. position, float)

I use the CSS positional property `float: left` in creating my navigation bar. I also make use of it again when changing the layout of the navbar on smaller screens (< 600px) (styles.css, line 72).

```
@media screen and (max-width: 600px){
  nav > ul li {
    float: none;
  }
  .social-li {
    float: none;
  }
}
```
### Make use of both inline and block elements

There are several examples of explicitly declaring elements' `display` properties in my external stylesheet. For instance:
1. `nav li > a` is set to `display:block`.
2. My Contact page consists of two inline-block elements wrapped in an enclosing `div` element. This allows me to set the height and width of these elements while displaying them in-line on larger screens.
3. I use inline `span` elements for adding emphasis to copy (e.g. about.html, line 40)

## Additional Features of HTML and CSS

In going beyond the parts of HTML and CSS described in class, I wanted to further explore two important aspects of modern design for the web, responsive design and accessibility.

## Responsive Design

To make my website more responsive, I created new styling for devices with widths less than 600px (e.g. smartphone devices). I switch to smaller versions of my banner images which display better, and added some opaque background to texts to make them more readable. I also switch to a vertical navigation bar on smaller displays.

## Accessibility

I was curious to see how my website might be viewed by blind or low-vision users. According to the World Health Organization, [an estimated 253 million people live with vision impairment](http://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment). As developers, we should make every effort to design equitable digital spaces. To test my site, I used the inbuilt VoiceOver programme on macOS Mojave. After an initial scan through of my page (by using the read page command - `Control + Option + A`), I made the following adjustments.

1. Added `alt` attributes to my images.
2. For background images, I added `aria-label` to my `<header>` tags.
3. Added `title` attributes to my social links. This gives a way to describe non-text links.
4. Added a `<span>` tag to my footer with the text 'love' and then hid that using CSS. This allows the screenreader to not lose the meaning of the sentence for blind or low-vision users.
5. Added hidden `<h2>` tags that describe content contained within `<section>` tags. These overly verbose headings are hidden from sighted users.

To recreate my screen-reader test on macOS:

1. Enable "VoiceOver" from "System Preferences/Accessibility".
2. To start VoiceOver hold `Command + F5`.
3. With my site open, hold `Control + Option + A` for VoiceOver to begin reading the page.

## Attribution

Code samples and content (such as copy) from external sources are referenced as such as comments in the HTML and CSS. The images are from Pexels, [and are free for personal and commercial purposes](https://www.pexels.com/photo-license/). The home and heart images from index.html are from [Nucleo's free pack](https://nucleoapp.com/).
