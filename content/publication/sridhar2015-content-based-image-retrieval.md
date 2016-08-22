+++
abstract = "Content-based image retrieval (CBIR) systems allow for retrieval of images from within a database that are similar in visual content to a query image. This is useful for digital pathology, where text-based descriptors alone might be inadequate to accurately describe image content. By representing images via a set of quantitative image descriptors, the similarity between a query image with respect to archived, annotated images in a database can be computed and the most similar images retrieved. Recently, non-linear dimensionality reduction methods have become popular for embedding high-dimensional data into a reduced-dimensional space while preserving local object adjacencies, thereby allowing for object similarity to be determined more accurately in the reduced-dimensional space. However, most dimensionality reduction methods implicitly assume, in computing the reduced-dimensional representation, that all features are equally important. In this paper we present boosted spectral embedding(BoSE), which utilizes a boosted distance metric to selectively weight individual features (based on training data) to subsequently map the data into a reduced-dimensional space. BoSE is evaluated against spectral embedding (SE) (which employs equal feature weighting) in the context of CBIR of digitized prostate and breast cancer histopathology images. The following datasets, which were comprised of a total of 154 hematoxylin and eosin stained histopathology images, were used: (1) Prostate cancer histopathology (benign vs. malignant), (2) estrogen receptor (ER) + breast cancer histopathology (low vs. high grade), and (3) HER2+ breast cancer histopathology (low vs. high levels of lymphocytic infiltration). We plotted and calculated the area under precision-recall curves (AUPRC) and calculated classification accuracy using the Random Forest classifier. BoSE outperformed SE both in terms of CBIR-based (area under the precision-recall curve) and classifier-based (classification accuracy) on average across all of the dimensions tested for all three datasets: (1) Prostate cancer histopathology (AUPRC: BoSE = 0.79, SE = 0.63; Accuracy: BoSE = 0.93, SE = 0.80), (2) ER + breast cancer histopathology (AUPRC: BoSE = 0.79, SE = 0.68; Accuracy: BoSE = 0.96, SE = 0.96), and (3) HER2+ breast cancer histopathology (AUPRC: BoSE = 0.54, SE = 0.44; Accuracy: BoSE = 0.93, SE = 0.91). Our results suggest that BoSE could serve as an important tool for CBIR and classification of high-dimensional biomedical data."
abstract_short = ""
authors = ["A Sridhar", "S Doyle", "A Madabhushi"]
date = "2015-06-29"
image = ""
image_preview = ""
math = true
publication = "In *Journal of Pathology Informatics*."
publication_short = "J. Pathol. Inform."
selected = false
title = "Content-Based Image Retrieval of Digitized Histopathology in Boosted Spectrally Embedded Spaces"
url_code = ""
url_dataset = ""
url_pdf = ""
url_project = ""
url_slides = ""
url_video = ""

+++
