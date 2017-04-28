+++
weight = 1
title = "Tissue Classification"
date = "2015-10-10T13:07:31+02:00"
tags = ["project", "digital pathology", "classification", "machine learning", "image analysis", "pattern recognition"]
categories = []
banner = "img/projects/tissue-classification.png"
+++

Medical image analysis has a long history, and recent years have included
several groundbreaking studies in histopathology. Below is a broad overview of
the steps required to quantify and analyze medical imaging, along with our
group's work in developing novel methods and experimental models.

<!--more-->

# Multi-Scale Framework Development

<img src="../../img/projects/image_processing_card.png" alt="Image Processing" class="img-responsive" />

We often deal with very high-resolution images that contain large amounts of
variance and noise. We are interested in developing frameworks that can deal
with whole-slide images on the order of 5-10 GB in size, identifying important
information at a variety of scales (sample, tissue, region, cell, and
intra-cell) using fast and robust methods, and standardizing images with respect
to lighting, stain intensity, and noise.

# Finding Biologically Important Structures

<img src="../../img/projects/object_segmentation_card.png" class="img-responsive" alt="" />

Object segmentation is a major topic in image analysis. Segmentation can be done
in a low-level manner driven by image pixels and homogeneity constraints, or at
a higher level by integrating domain knowledge to identify relevant areas and
eliminate unnecessary ones. In biomedical imaging, both approaches have their
uses in identifying important biological constructs such as tissue regions,
glands, cells, and sub-cellular components.

# Quantifying Biological Domain Knowledge

<img src="../../img/projects/feature_extraction_card.png" alt="Feature Extraction" class="img-responsive" />

Feature design and extraction is a complex process that involves two phases:
First, we must identify the (qualitative) characteristics of the images and
segmented structures that are necessary to identify the target classes, which
could be disease presence, cancer severity, patient outcome, etc. Second, we
need to ensure that we design feature operators that reliably and robustly
quantify those characteristics. Features should be independent from one another
(that is, each feature should add new information to the dataset) and should
capture intuitive biological processes.

# Viewing and Operating on Quantitative Data

Once the features are extracted for each object of interest (image, patient,
nucleus, etc.) we can analyze them prior to building a fully-fledged predictive
model. For example, we can identify feature groups that are highly correlated,
indicating that we might be extracting redundant information from the system. We
can perform "feature selection", which determines the feature's ability to
encode information about the target classes -- this serves as a nice sanity
check that our feature extraction is in fact yielding useful information.
Finally, we can look at the feature values themselves; this topic is covered in
great detail in our visualization projects.
