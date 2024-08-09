# Word Embedding Demo

This repository contains a Jupyter Notebook that demonstrates how to load and use pre-trained word embeddings using the Google News dataset. The word embeddings are leveraged to analyze the semantic relationships between words using the `gensim` library.

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Data](#data)
- [Contributing](#contributing)

## Overview

Word embeddings are a type of word representation that allows words to be represented as vectors in a continuous vector space. This demo notebook showcases how to:
- Download and prepare the Google News word embeddings.
- Load these embeddings using the `gensim` library.
- Perform basic operations with these embeddings, such as finding similar words, vector arithmetic, and more.

## Installation

To run this notebook locally, you'll need to have Python installed, along with the necessary packages. Follow the steps below to set up your environment:

1. Clone this repository:
    ```sh
    git clone https://github.com/yourusername/word-embedding-demo.git
    cd word-embedding-demo
    ```

2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

3. (Optional) Download the Google News word embeddings:
    - The notebook includes commands to download the embeddings directly, but you can also download them manually from [Google's archive](https://code.google.com/archive/p/word2vec/) or [Google Drive link](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM).

## Usage

Once the dependencies are installed, you can open and run the notebook:

1. Start Jupyter Notebook:
    ```sh
    jupyter notebook
    ```

2. Open the `Word_Embedding(Demo).ipynb` notebook.

3. Follow the steps in the notebook to download the Google News word embeddings, load them, and perform various word embedding operations.

### Key Features Demonstrated:
- **Downloading the Google News Word2Vec Model**: The notebook includes commands to download and unzip the necessary files.
- **Loading Pre-trained Word Embeddings**: Using `gensim` to load the Word2Vec model.
- **Exploring Word Relationships**: Examples of finding similar words, vector arithmetic (e.g., `king - man + woman ≈ queen`), and more.

## Dependencies

The following Python packages are required to run the notebook:
- `gensim`
- `wget` (if you choose to download files directly via the notebook)
- `gzip` (for unzipping the downloaded files)

These can be installed via pip:
```sh
pip install gensim wget
```

## Data

The notebook uses the **Google News Word2Vec model**, which consists of 300-dimensional vectors for 3 million words and phrases. This model is large (~1.5GB), so ensure you have sufficient disk space and bandwidth.

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request with your improvements or bug fixes. If you're unsure about your changes, feel free to open an issue for discussion.
