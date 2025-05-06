# lodestone-labs.github.io
Brochure page

Used [this post from Steven
Westmoreland](https://stevenwestmoreland.com/2021/01/using-tailwind-css-with-jekyll.html)
to set up Tailwind CSS with Jekyll.

# Pictures 

Responsive image tags are created with [Jekyll Picture Tag](https://rbuchberger.github.io/jekyll_picture_tag). 

Required dependencies (available in [Homebrew](https://brew.sh/)):
- libvips
- libpng
- libwebp: this has webp in brew, but may need to use a custom libwebp tap like this https://github.com/skyzyx/homebrew-webp 
- libjpeg
- libheif

`brew install libvips`

These will also need to be installed on any build environments that are used. 
