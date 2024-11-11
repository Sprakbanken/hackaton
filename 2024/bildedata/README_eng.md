# Hackathon image data

[Here](simple-search.ipynb) is an example notebook that shows how you can load the image dataset and search for images based on SigLIP embedding vectors.
The dataset is quite large (15 GiB) so contact Marie for a copy.
You can, alternatively, take inspiration from our image search application: https://dh.nb.no/bildesok/.

## Om datasettet

The dataset consists of 363061 images with SigLIP embedding vectors from 16711 Norwegian books published before the year 1900 that are in the public domain
The SigLIP embedding vectors are obtained with the `google/siglip-base-patch16-256-multilingual` model.

In addition to images, we have the following metadata from the books (where it was available).

 * access (streng)
 * authors (streng)
 * title (streng)
 * publisher (streng)
 * published_year (år)
 * tags (liste med strenger)
 * language (streng)
 * document_type (streng)
 * udc (streng)
 * license (streng)
 * page_urn (streng)
 * image_url (streng)
 * urn (streng)
 * file_name (streng)
 * public_domain (streng)
 * genres (streng)
 * issn (streng)
 * dewey (streng)
 * original_title (streng)
 * isbn (streng)

We have used outputs from the digitization pipeline at the National Library to detect the images.
Specifically, we have extracted the parts of each page that have been classified as graphical elements.
Consequently, there are some misclassifications and some images contain e.g. tables or blank pages.
