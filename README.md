# NLP Project: Extracting Top Informative Sentences

## Project Overview
This project utilizes Natural Language Processing (NLP) techniques to extract the most informative sentences from a given set of text data. By leveraging multiple NLP models and algorithms, it ranks sentences based on their importance using various scoring mechanisms such as TF-IDF, BERT embeddings, TextRank, keyword extraction, and Named Entity Recognition (NER).

## Features
- **Text Preprocessing:** Tokenization, lemmatization, stopword removal using SpaCy.
- **TF-IDF Scoring:** Assigns scores based on word frequency importance.
- **BERT-based Sentence Embeddings:** Uses `sentence-transformers` to compute similarity scores.
- **TextRank Algorithm:** Uses `networkx` to rank sentences based on similarity.
- **Keyword Extraction:** Utilizes `yake` for importance-based scoring.
- **Named Entity Recognition (NER):** Assigns scores based on the presence of named entities.
- **Sentence Ranking & Selection:** Combines all scoring methods to rank and extract top sentences.
- **Visualization:** Displays a bar chart of top-ranked sentences.

## Technologies Used
- Python
- NLP Libraries: `spaCy`, `nltk`, `sentence-transformers`, `yake`
- Machine Learning: `scikit-learn`
- Graph Algorithms: `networkx`
- Data Visualization: `matplotlib`

## Installation
Run the following command to install all dependencies:
```sh
!pip install numpy pandas nltk scikit-learn sentence-transformers networkx matplotlib spacy yake
!python -m spacy download en_core_web_sm
```

## How to Use
1. **Prepare the Input:** Provide a list of sentences.
2. **Set Parameters:** Modify `num_total_sentences` and `num_top_sentences` as needed.
3. **Run the Script:** The program will process the sentences and return the most informative ones.
4. **Visualize Results:** A bar chart will be generated showing sentence importance scores.

## Example Usage
```python
num_total_sentences = 100  # Total number of sentences
num_top_sentences = 10  # Number of top-ranked sentences to extract
sentences = [
    "Artificial intelligence is transforming industries worldwide.",
    "Climate change is a global challenge requiring urgent action.",
    ...
]

ranked_sentences = extract_top_sentences(sentences, num_top_sentences)
top_sentences = [sent for _, sent in ranked_sentences[:num_top_sentences]]

for i, sentence in enumerate(top_sentences, 1):
    print(f"{i}. {sentence}")
```

## Output Example
```
Top 10 Informative Sentences:
1. Artificial intelligence is transforming industries worldwide.
2. Climate change is a global challenge requiring urgent action.
...
```

## Contributing
If you'd like to contribute, feel free to fork the repository and submit a pull request.

## License
This project is open-source and available under the MIT License.

