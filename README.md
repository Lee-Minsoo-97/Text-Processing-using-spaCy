# Text-Processing-using-spaCy

# LAB Assignment 1 - README

This Jupyter Notebook focuses on applying **SpaCy**, a powerful natural language processing (NLP) library, to analyze and process textual data. Below is an overview of its structure and main features.

## Key Details
- **Author**: Minsoo Lee  
- **Date**: January 22, 2025  
- **Total Cells**: 36  
  - **Code Cells**: 25  
  - **Markdown Cells**: 11  
- **Purpose**:  
  The notebook demonstrates how to use SpaCy to preprocess and analyze a dataset of restaurant reviews, focusing on sentiment analysis and text processing.

## Main Features

### 1. Library Setup
- The notebook sets up **SpaCy** and loads the `en_core_web_lg` pre-trained language model.  
- Example code:
    ```python
    !pip install spacy==3.5.4
    import spacy
    nlp = spacy.load("en_core_web_lg")
    ```

### 2. Data Import and Overview
- Loads a dataset of restaurant reviews from a `.csv` file.  
- Initial data exploration includes displaying the first few rows and basic data analysis.

### 3. Data Selection
- Filters specific sentiment data, such as 1-star and 5-star reviews, for focused analysis.

### 4. Text Processing with SpaCy
- Implements SpaCy's core features:
  - Tokenization and segmentation
  - Named Entity Recognition (NER)
  - Text vectorization using pre-trained embeddings
- Example code:
    ```python
    doc = nlp("This is a 1-star review.")
    for token in doc:
        print(token.text, token.pos_, token.dep_)
    ```

### 5. Insights and Applications
- Demonstrates preprocessing of unstructured text data for tasks like sentiment analysis and feature extraction.

## Example Markdown and Code Insights

### Markdown Snippets
- Includes detailed instructions, such as:
  - *"Apply necessary text processing techniques on the selected reviews"*
  - *"1. Segmentation/Tokenization"*

### Code Snippets
- Example snippets include:
    - **Loading and exploring data**:
        ```python
        df = pd.read_csv(data_path)
        print(df.head())
        ```
    - **Filtering specific reviews**:
        ```python
        one_star_reviews = df[df['stars'] == 1]
        print("1 STAR REVIEW")
        ```

## Summary
This notebook provides a practical guide to leveraging SpaCy for NLP tasks using a real-world dataset. It is ideal for those interested in exploring SpaCy's capabilities for preprocessing and analyzing text data to derive meaningful insights.
