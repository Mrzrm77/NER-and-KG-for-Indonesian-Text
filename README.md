# Named Entity Recognition and Knowledge Graph from Indonesian Text

Introduction
---
This project focuses on developing a system to extract Named Entities (NER) and construct a Knowledge Graph (KG) from Indonesian text, specifically from Wayang stories. The primary goal is to identify and categorize entities such as characters, deities, places, and heirlooms, and to extract relationships between them.

Key Features
---
- Data Loading & Preprocessing: Loads and cleans text data from .txt files, including text normalization and punctuation removal.
- Named Entity Recognition (NER): Trains two spaCy models (one with a blank id model and another with a multilingual xx_ent_wiki_sm model) to identify custom entities.
- NER Model Evaluation: Evaluates model performance using metrics such as Precision, Recall, F1-score, and Confusion Matrix.
- Knowledge Graph Extraction: Utilizes the Google Gemini API to extract relationships (specifically family, allied, or enemy relationships) between detected entities.
- Knowledge Graph Visualization: Visualizes entity relationships in an interactive graph using the pyvis library.
- Entity Similarity Analysis: Calculates and visualizes cosine similarity between entities using word embeddings from a spaCy model.

Methodology
---
- Data Loading: Loads Wayang stories from different text files.
- Text Preprocessing: Applies cleaning functions to remove punctuation, normalize spaces, and convert text to lowercase.
- Entity Definition: Defines a list of custom entities and their categories (TOKOH, DEWA, TEMPAT, PUSAKA).
- NER Model Training: Initializes and trains NER pipelines on the annotated data, using both a blank id model and the xx_ent_wiki_sm model as a base.
- Relationship Extraction: After entity detection, the Gemini API is called to identify relationships between entities based on the text context.
- KG Construction & Visualization: The extracted relationships are used to build and visualize a Knowledge Graph, allowing for interactive exploration.
- Entity Similarity: Word embeddings are obtained for unique entities, and cosine similarity is calculated to measure semantic closeness.
Technologies Used
- Python: The primary programming language.
- spaCy: For Named Entity Recognition (NER) and natural language processing.
- Google Gemini API: For Knowledge Graph relationship extraction.
- pyvis: For interactive Knowledge Graph visualization.
- scikit-learn: For NER model evaluation metrics and cosine similarity.
- Matplotlib & Seaborn: For data visualization and plotting evaluation metrics.

Installation and Usage Requirements
---
- Google Colab (recommended environment)
- Google Gemini API Key (configured in Colab secrets or environment variables)

Steps
---
- Open Notebook: Open the .ipynb notebook in Google Colab.
- Install Dependencies: Run the cells that install spacy, pyvis, etc.
- Configure Gemini API Key: Ensure your Gemini API key is correctly configured (e.g., via userdata.get('GOOGLE_API_KEY')).
- Run All Cells: Execute all cells in order to load data, train NER models, extract and visualize the Knowledge Graph, and analyze entity similarity.

Results and Insights
---
- The NER models demonstrate strong performance in detecting custom entities.
- The generated Knowledge Graph provides a structured representation of relationships within the Wayang stories.
- Interactive visualizations facilitate exploration of relationships between entities.
- Cosine similarity analysis can uncover semantic closeness between entities that might not be immediately apparent in the KG.
