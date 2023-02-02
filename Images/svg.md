# SVG - Scalable Vector Graphics

SVG images are a scalable image format, which means they will scale and keep the same qaulity without increasing file size.

Common uses:

1. Icons
2. Graphs/Charts
3. Large, simple images
4. Patterned Backgrounds
5. Applying effects to other elements via SVG filters

Not good for:

1. complicated, detailed images

### Creating SVGs

Typically, you wouldn't create SVGs directly from XML, but rather something like Figma or Adobe Illustrator. However, downloading an existing SVG and tweaking small things in XML is more common.

### Embedding SVGs

Two ways: Linked or Inline

#### Linked

Samea s linking any other image format. use `<img>` or similar or in CSS using `background-image: url(./my-image.svg)`. The CSS method allows it to scale, but the image contents are not available on the webpage. This is the simple option.

#### Inline

Paste the contents of the SVG directly into the webpage's code. Allows thee contents to be reachable by CSS/Javascript. However, this can make your code harder to read, make the webpage less cacheable, and may delay loading. Some of these things can be avoided with React and other tools.

## XML - Extensible Markup Language

SVG images are defined using XML. It's syntax is similar to HTML and is used for APIs, RSS, spreadsheets and more. IT's interoperable with HTML - copy paste into a webpage!

This allows the images to be human readable (you can't read a binary jpeg file).

## Making SVGs

use free editors like Inkscape, or the paid Affinity Designer.
