# Delete Duplicate Images

**This tool allows the user to search specified directories for duplicate or near duplicate images and delete them.**

The tool is built on SentenceTransformers which a Python framework that allows the user to embed images and text into the same vector space. The framework is able to identify similar images through the proximity of their embeddings and so identify duplicates and near duplicates. SentenceTransformers itself is a package built from the work discussed in the paper _Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks (Reimers & Gurevych, EMNLP 2019)_.

**How to use this tool**

- Paste directories
  - One directory: The pairwise similarity between all images in the directory will be computed.
  - Two directories: All images in the first directory will be pairwise compared to all images in the second directory .
  - **Warning: If entering two directories, ensure that there are no duplicates within either directory either manually or by running the tool on single directories first.**
- Adjust the similarity threshold provided if necessary to pull a list of all duplicate images onto the screen.
- Select which images you would like to delete, and press "Execute". 
- **Warning: The tool does not have functionality to recover images accidentally deleted by the user, so please be careful.**

## Further Reading

This project was inspired by several open source projects which are cited below:

- [Duplicate Image Demo] - .ipynb file demonstrating the usage of a Sentence Transformer
- [Streamlit Demo] - .py file demonstrating how to build an app in Streamlit

## License

MIT

**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
   [Duplicate Image Demo]: <https://github.com/UKPLab/sentence-transformers/blob/master/examples/applications/image-search/Image_Duplicates.ipynb>
   [Streamlit Demo]: <https://github.com/streamlit/demo-self-driving/blob/a3ea599ff44f9b0f1f0613490f2e49382c5fd0e2/streamlit_app.py#L200>