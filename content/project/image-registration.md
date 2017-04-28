+++
weight = 2
title = "Image Registration"
date = "2017-01-01"
tags = ["project", "digital pathology", "classification", "machine learning", "image analysis", "pattern recognition"]
categories = []
banner = "img/projects/image-registration.png"
+++

If we want to do 3D modeling, we first need to know how to translate 2D sections
into 3D objects. For this, we use image registration to align sections of tissue
into the same coordinate plane.

<!--more-->

# Registration vs. Native 3D Microscopy

Microscopy gives us a view of biology on the scale of microns. A typical
brightfield microscopy section at 40x optical magnification is digitized at
about 0.25 microns per pixel (mpp). For comparison, a cell nucleus is on the
order of 10 microns in diameter.

While some types of microscopy are inherently 3D (confocal microscopy, for
example), these techniques are often expensive, require specialized preparation,
and are limited in their ability to visualize "deep" tissue sections. Further,
the majority of clinically-available samples are not prepared with 3D microscopy
in mind: they are non-specifically stained (e.g. with hematoxylin and eosin) and
intended for use in brightfield settings.

# Macro-scale Structure from Micro-scale Data

We can combine the benefits of 2D microscopy (high resolution) with those of 3D
microscopy (realistic biological structure) by obtaining multiple serial
sections of tissue. This is done by sequentially cutting a block of tissue,
fixing each slice on a glass slide, and staining for the structures of interest.
These slides are then scanned at a typical working resolution (between 0.25 -
0.5 microns per pixel) to yield a large set of data for each tissue sample.

These images are in _sequence_, but not yet in _alignment_. To line up our
sequence of images, we must register them so they can be stacked together to
reconstruct the underlying 3D architecture. That process of figuring out how to
transform image A so that it aligns with image B is the goal of registration
methods.

# Improving Existing Registration Techniques

There are many methods for performing registration; interested readers are
encouraged to check out [Fiji](www.fiji.sc), a package of ImageJ that contains
popular registration methods. In our lab, we are interested in expanding the
ability of these algorithms to tackle the following problems:

1. ***Large images***: Whole Slide Imaging (WSI) leads to tissue images that can
   measure several gigabytes of space (corresponding to images of dimension
   100,000 x 100,000 and larger). Efficient registration of these images would
   mean that we can create stacks covering a wider area of biological tissue.
2. ***Deep stacks***: Tissue sections can average around 6 microns of thickness.
   This means that serial sectioning a block of tissue that is 1 centimeter deep
   may result in up to 10,000 sections! If the registration algorithm cannot
   handle errors across several images, then those errors may become magnified
   across such a large space.
3. ***Missing / Noisy Data***: As any lab technician will tell you, getting
   10,000 perfect slides is impossible. Tissue tearing, inconsistencies in
   staining, and lost sections are a reality that must be handled at the
   registration side. The algorithm must be robust to these changes; also, it
   must be able to interpolate between sections that are lost.

We aim to build on existing methods to create a robust set of techniques that
are driven by the data itself: by understanding the scale of the data and
structures of interest, it should be possible to tune the parameters of these
methods to yield accurate registered stacks that reflect the underlying volume.
