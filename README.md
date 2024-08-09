# Word Embedding Demo

Welcome to the Word Embedding Demo repository! This project showcases the use of pre-trained word embeddings to explore semantic relationships between words using the powerful `gensim` library and the widely recognized Google News Word2Vec model.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Quickstart](#quickstart)
- [Installation](#installation)
- [Usage Guide](#usage-guide)
- [Understanding Word Embeddings](#understanding-word-embeddings)
- [Dataset Information](#dataset-information)
- [Dependencies](#dependencies)
- [Project Structure](#project-structure)
- [Contributing](#contributing)

## Introduction

Word embeddings are a popular representation method in Natural Language Processing (NLP), where words are mapped to vectors of real numbers in a continuous vector space. These vectors capture semantic meanings, enabling machines to understand and process human language more effectively.

This notebook demonstrates how to:
- Download the Google News Word2Vec model.
- Load and utilize the pre-trained word embeddings.
- Perform various word vector operations to explore word similarities, analogies, and more.

## Features

- **Seamless Model Download:** Automatic downloading and extraction of the Google News Word2Vec model.
- **Efficient Word Vector Loading:** Use `gensim` to load large-scale pre-trained word vectors.
- **Semantic Exploration:** Analyze and visualize word similarities, perform vector arithmetic, and discover interesting word analogies.
- **Extensibility:** Easily extend the notebook to include additional NLP tasks or integrate other word embedding models.

## Quickstart

If you’re eager to dive in, follow these steps to get the project up and running:

1. Clone the repository and navigate to the project directory:
    ```sh
    git clone https://github.com/yourusername/word-embedding-demo.git
    cd word-embedding-demo
    ```

2. Install the necessary Python packages:
    ```sh
    pip install -r requirements.txt
    ```

3. Start Jupyter Notebook and open the provided notebook:
    ```sh
    jupyter notebook
    ```

4. Run the notebook `Word_Embedding(Demo).ipynb` to see the word embeddings in action.

## Installation

### Prerequisites

Before you begin, ensure that you have the following installed:
- Python 3.7 or higher
- Jupyter Notebook

### Setting Up the Environment

1. **Clone the Repository:**
    ```sh
    git clone https://github.com/yourusername/word-embedding-demo.git
    ```

2. **Navigate to the Project Directory:**
    ```sh
    cd word-embedding-demo
    ```

3. **Install Dependencies:**
    Install all required Python packages using the following command:
    ```sh
    pip install -r requirements.txt
    ```

4. **(Optional) Download Word2Vec Model:**
    While the notebook provides commands to download the Word2Vec model, you can also manually download it from [Google Drive](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM) or [Google's Archive](https://code.google.com/archive/p/word2vec/).

## Usage Guide

### Running the Notebook

To run the notebook:

1. Launch Jupyter Notebook:
    ```sh
    jupyter notebook
    ```

2. Open the file `Word_Embedding(Demo).ipynb`.

3. Execute the cells sequentially to:
    - Download and extract the Google News Word2Vec model.
    - Load the model into memory using `gensim`.
    - Explore various operations on word vectors, such as finding similar words, performing vector arithmetic, and understanding word analogies.

### Example Operations

- **Finding Similar Words:**
    Identify words that are semantically similar to a given word.
    ```python
    model.most_similar('king')
    ```

- **Vector Arithmetic:**
    Perform operations like `king - man + woman ≈ queen`.
    ```python
    result = model.most_similar(positive=['king', 'woman'], negative=['man'])
    ```

- **Word Analogies:**
    Explore interesting word relationships and analogies.
    ```python
    model.most_similar(positive=['Paris', 'Germany'], negative=['France'])
    ```

## Understanding Word Embeddings

Word embeddings are a crucial part of modern NLP, representing words as dense vectors in a high-dimensional space. These vectors are trained on large corpora, capturing syntactic and semantic word relationships.

- **Semantic Relationships:** Words with similar meanings are located near each other in the vector space.
- **Vector Arithmetic:** The direction and distance between word vectors encode analogies and relationships.

For instance, the famous analogy "king is to queen as man is to woman" can be represented as:
\[ \text{king} - \text{man} + \text{woman} \approx \text{queen} \]

## Dataset Information

The Google News Word2Vec model consists of 300-dimensional vectors for approximately 3 million words and phrases. This model was trained on part of the Google News dataset (about 100 billion words).

- **Model Size:** ~1.5GB
- **Dimensions:** 300
- **Source:** [Google's Word2Vec project](https://code.google.com/archive/p/word2vec/)

## Dependencies

This project relies on the following Python packages:

- `gensim`: For loading and working with Word2Vec models.
- `wget`: For downloading files from the web directly within the notebook.
- `gzip`: For decompressing `.gz` files.

Install all dependencies using:
```sh
pip install -r requirements.txt
```

## Project Structure

```
word-embedding-demo/
│
├── Word_Embedding(Demo).ipynb  # Jupyter Notebook demonstrating word embeddings
├── requirements.txt            # List of Python dependencies
└── README.md                   # This readme file
```

## Contributing

Contributions are welcome! Whether you’re fixing bugs, adding new features, or improving documentation, your help is appreciated. 

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

For significant changes, please open an issue first to discuss what you would like to change.
