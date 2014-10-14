SimpleGallery
=============
Author: Joseph Bozarth,
Date Created: 10-13-2014

A clean, easy to use, straight forward jQuery gallery.

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/.


Overview
------------------
When I was doing some work on my personal website I thought it would be nice to have some gallery type functionality. So I went looking but I could not find anything that was not overly complex for what I needed. I just wanted to display some pictures to go with my build posts, not sell anything grab attention with flashy graphics.

You can see a live demo on my site gallery: http://bozarthprime.github.io/gallery.html


Implementation
------------------
Include jQuery, jQuery UI, SimpleGallery.js, and SimpleGallery.css


Usage
------------------
The idea is that you will have a class that will denote your galleries (I will use '.gallery' in my example) and you just call SimpleGallery() on that class on document ready. All objects with that class will become galleries. You can do this with multiple classes with different settings if you wish.

Example:
```
<script>
	$(document).ready(function() {
		$('.gallery').SimpleGallery();
	});
</script>

<div class='gallery'>
	<img src='img1.jpg' comment='Picture annotation example 1' />
	<img src='img2.jpg' />
	<img src='img3.jpg' comment='Picture annotation example 2' />
	<img src='img4.png' />
</div>
```

Example with options:
```
<script>
	$(document).ready(function() {
		$('.gallery').SimpleGallery({
			nextImage: "/images/right_arrow.gif", 
			prevImage: "/images/left_arrow.gif",
			closeImage: "/images/x.gif"
		});
	});
</script>

<div class='gallery'>
	<img src='img5.jpg' />
	<img src='img6.jpg' />
</div>
```

The comment attribute on the image is how you leave annotations for images.

Options
------------------
* height: The maximum height a gallery can be, if it would be over this it will scroll (default: 500)
* width: The width of the gallery (default: 100)
* heightIsPercent: If the height is px or percent (default: false)
* widthIsPercent: If the width is px or percent (default: true)
* nextImage: Path to an image for the next image button (default: text reading 'Next')
* prevImage: Path to an image for the previous image button (default: text reading 'Prev.')
* closeImage: Path to an image for the close button (default: capital 'X' in consolas font)
