# Delete duplicate images from specified directories

**This tool allows the user to search specified directories for duplicate or near duplicate images and delete them.**

The tool is built on [SentenceTransformers](https://www.sbert.net/) which is a Python framework for sentence, text and image vector space embeddings. By computing the embeddings of unseen images and by taking the distance between them, the framework is able to approximate the distance between pairwise sets of images and hence identify duplicates or near duplicates. SentenceTransformers itself is a package built from the work discussed in the paper [Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks (Reimers & Gurevych, EMNLP 2019)](https://arxiv.org/pdf/1908.10084.pdf).

<img src="https://github.com/cadams012/Delete-Duplicate-Images/blob/main/demo.PNG" width="800">

**How to use this tool**

- Run all cells down to the user specifications section.
- Specify either:
    - One directory: The pairwise similarity between all images in the directory will be computed. Once an image is matched, it will not be revisited by the algorithm again.
    - Two directories: The pairwise similarity between images in the first directory will be computed against those in the second directory. Once an image in the first directory is matched to images in the second directory, these matched images will not be revisited by the algorithm again.
    - **Warning: If entering two directories, ensure that there are no duplicates within either directory by running the tool on single directories first.**
- Adjust the similarity threshold provided if desired. This is a hyperparameter that is set by default to 0.92 which was an empirically chosen value.
- Run the remaining cells to open the tool, and follow the instructions to navigate through duplicates ("Previous/Next") and to delete highlighted duplicates ("Delete & Continue").
- **Warning: The tool does not have functionality to recover images accidentally deleted by the user, so please be careful.**

## Future Improvements

- Clustering similar images together using density based clustering techniques (e.g. DBSCAN) rather than iteratively looping through images and identifying later images which are similar.
- Reworking the Matplotlib buttons as an issue in Matplotlib thought to be introduced in v3.3.1 has slowed down the operation of the event handling features of the buttons.

## Further Reading

This project was inspired by a [demonstration workbook](https://github.com/UKPLab/sentence-transformers/blob/master/examples/applications/image-search/Image_Duplicates.ipynb) of an open source project based on Sentence Transformers that demonstrates the fundamentals of image duplicate identification from embeddings.
