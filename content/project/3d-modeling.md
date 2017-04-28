+++
weight = 3
title = "3D Modeling"
date = "2015-10-10T13:07:31+02:00"
tags = ["project", "digital pathology", "classification", "machine learning", "image analysis", "pattern recognition"]
categories = []
banner = "img/projects/3d-modeling.png"
+++

Biology exists in a three-dimensional spatial world, but too often we are
restricted to a 2D view of nature through microscopy sections. To facilitate
understanding of both normal and disease states, we are interested in building
and analyzing 3D models of biological structures.

<!--more-->

# Source Data

Our data comes from a variety of sources, representing the multi-center
collaborations our lab is engaged in. For example, in our work on oral cavity
cancer architecture, we obtain serial stacks of 2D histology from tumor
resections at the Erie County Medical Center. Meanwhile, data for modeling
microvessel connections between the vagina and the bladder are obtained through
the generous Anatomical Donor Program here at the University at Buffalo.
Finally, high-resolution computed tomography (CT) scans of cadavers are obtained
at the Center for Translation and Clinical Research, which are used to further
our understanding of human anatomy through segmentation and analysis of organ
structures _in situ_.

# 3D Visualization

3D data exists as either point clouds (a collection of vertices in 3D space) or
as a mesh (a set of triangular or polygonal shapes with edges, faces, and
orientation in space). For easy visualization of these objects, we can use
open-source tools like [MeshLab](http://www.meshlab.net/) to quickly calculate
useful statistics like surface area, volume, and curvature. For more detailed
analysis, we can use custom-written code in Python to run feature analysis and
extract useful data from each object.

# From Data to Diagnosis

By operating in 3D, we can observe relationships between structure that are
difficult or impossible to achieve with a series or sampling of 2D sections. In
oral cavity cancer, for example, we need to know if two tumor regions are
separate or connected, and how far apart they are in real space. In a single 2D
slice, we may have a misleading view of the structure, which will lead us to
think the tumor regions are further apart -- and that the tumor is more
aggressive -- than it actually is. Moreover, we may find that we can identify
more diagnostically useful features in 3D than in 2D, leading to a new
understanding of how tumors grow and migrate through living tissue.
