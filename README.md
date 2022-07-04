# Delete duplicate images from specified directories

**This tool allows the user to search specified directories for duplicate or near duplicate images and delete them.**

The tool is built on [SentenceTransformers](https://www.sbert.net/) which is a Python framework for sentence, text and image vector space embeddings. By computing the embeddings of unseen images and by taking the distance between them, the framework is able to approximate the distance between pairwise sets of images and hence identify duplicates or near duplicates. SentenceTransformers itself is a package built from the work discussed in the paper [Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks (Reimers & Gurevych, EMNLP 2019)](https://arxiv.org/pdf/1908.10084.pdf).

**How to use this tool**

- Paste directories
  - One directory: The pairwise similarity between all images in the directory will be computed.
  - Two directories: All images in the first directory will be pairwise compared to all images in the second directory .
  - **Warning: If entering two directories, ensure that there are no duplicates within either directory either manually or by running the tool on single directories first.**
- Adjust the similarity threshold provided if necessary to pull a list of all duplicate images onto the screen.
- Select which images you would like to delete, and press "Execute". 
- **Warning: The tool does not have functionality to recover images accidentally deleted by the user, so please be careful.**

## Further Reading

This project was inspired by a [demonstration workbook](https://github.com/UKPLab/sentence-transformers/blob/master/examples/applications/image-search/Image_Duplicates.ipynb) of an open source project based on Sentence Transformers that demonstrates the fundamentals of image duplicate identification from embeddings.
