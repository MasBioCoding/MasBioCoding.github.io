---
layout: post
title:  "Visualising a full leaf"
date:   2023-12-08 10:00:00 +0100
categories: images
---

# Visualising a full leaf

Have you ever looked at a leaf and wondered about it's cellular structures?
Have you ever been teased into this feeling of not fully understanding a plant?
Most animals run away, giving you pleanty reason not to know them intimately. But plants can't hide,
yet still they must peak your curiosity. Have you ever sat in front of a leaf and strained your eyes to see inside?
With a microscope, you might gain insight, but you lose perspective. Peering into the binoculars, the sense of scale disappears.
After an initial wonder, a new wave of curiosity arises, and the only answer would surely be to increase the magnification.
Deeper still lies the mystery.

This can go on and on and every time we gain something, but we also leave behind the world we knew. And looking back at the full leaf,
we feel only more wonder, but no satisfaction. In this project I am trying to marry the world we know, to the world too small to see.
I want you to have acces to the leaf in it's entirety without distinction from it's cellular composition.
Image stitching and focus stacking allow for this. I have created a single large image composed of hundreds of photos.
This allows you to zoom in to any part of the leaf and see it's cells, while at the same time keeping the perspective of the leaf
as a whole. Zoom in to see details.

![top](/images/full_leaf/plantbovenkantq4_Panorama-1.jpg)
![bottom](/images/full_leaf/plantonderkantq4_Panorama-1.jpg)

Notice the interesting puzzle piece like cuticle. In reality this covers the whole outside of the leaf, but it is so transparent that the focus stacking algorithm has trouble recognising it.
Also notice on the bottom side of the leaf, the second image, the many stomata in between the puzzle pieces.

# Focus stacking

Focus stacking is taking many photographs at different focal lengths to create a single image that is sharp everywhere.

 <img src="/images/full_leaf/stackincomplete1.jpg" alt="stackincomplete1.jpg" width="360"/>
 <img src="/images/full_leaf/stackincomplete2.jpg" alt="stackincomplete2.jpg" width="360"/>

![stacked](/images/full_leaf/stackcomplete.jpg)

# Image stitching

Image stitching is taking many photographs that overlap, so that a software can stitch them together into a bigger image. The stacked image we created in the previous section can be stitched with another stacked image like this

![untstiched1](/images/full_leaf/stitchincomplete2.jpg)

Notice the two area's slightly overlap. The bottom of this second image correspond to the top of the first image. Software can identify the overlapping features into a full image. I have manually taken hundreds of photographs of a very small young leaf, maybe 4 mm in diameter. The focus stacks are about 20 images each and then the stitches are 20 images for the top of leaf 1, and 11 for the bottom of leaf 2. The original png files are about 150 MB  for the final images, however don't worry. I have compressed them to about 5 MB each. The other photos are each less than a megabyte to this page won't eat up data.

# Thoughts for future work

There are pieces I am happy with, like the bottom side of the second image, but mostly I think the focus stacking proces did a bad job of picking the parts that are important. I want to get the outermost layers of cells, the cuticle, and their interesting puzzle-piece-like organisation. The transparency of the leaf cells makes this very hard to automate. A deeper focus exposes the more inner cells from the mesophyll, but warped by the refractions through the cuticle and epidermal layer, the final result is an incomprehensible mess when you zoom in. This proces already took 4 hours in total to do both leaves, blending by hand would increase that perhaps 10 fold, simply not worth it.
I think my next attempt will be with top lighting, hopefully decreasing the transparency and increasing reflections from the waxy cuticle, that way the focus stacking algorithm will know more easily what I want.
Alternatively I could do shallower stacks, and more stitches. Focus only on the cuticle in the middle of the objective, and take images at more locations.
Maybe a combination of these both.
I focus stacked from the most deep towards the most shallow focus, I guess the other way around the algorithm first encounters the in-focus cuticle, perhaps this matters too.

Additionally there are live stitching programs these days. These programs only require a video input and will automatically output a large stitched image. Perhaps this is the most efficient approach
