# Crowdsourced-Product-Recommender-System-using-Text-Analytics

## Overview
This project implements the core building blocks of a **crowdsourced recommender system** using unstructured text data from product reviews. Given a set of user-specified product attributes, the system recommends the top 3 products that best match user preferences.

The project focuses on comparing traditional **Bag-of-Words models** with **word embeddings** to evaluate which approach provides better recommendation quality in a real-world text analytics setting.

---

## Dataset
- **Source:** Beer reviews scraped from BeerAdvocate (Top-rated beers)
- **Size:** ~8,000–10,000 reviews across ~250 products
- **Schema:**
  - `product_name`
  - `product_review`
  - `user_rating`

Reviews without textual content were excluded during preprocessing.

---

## Methodology

### Data Collection
- Scraped reviews for top-rated products
- Handled pagination and filtering of empty reviews
- Created a clean review-level dataset

### Attribute-Based Recommendations
- Identified key product attributes using:
  - Word frequency analysis
  - Lift / co-occurrence analysis
- Simulated a user specifying **three preferred attributes**
- Built recommendations using:
  - Bag-of-Words representation
  - Cosine similarity
  - Sentiment analysis weighting
- Produced:
  - Top 3 recommendations
  - 20 additional contenders for comparison

### Word Embeddings vs Bag-of-Words
- Replaced BoW with **pretrained SpaCy word embeddings**
- Compared recommendation outcomes
- Analyzed which method performed better and why

### Custom Word Embeddings
- Trained **custom embeddings** using review data (SpaCy / Gensim)
- Evaluated changes in top-3 recommendations
- Compared pretrained vs domain-specific embeddings

### Ratings-Only Baseline
- Generated recommendations using only average user ratings
- Compared results against attribute-based recommendations
- Analyzed suitability for personalized user preferences

### Product-to-Product Similarity
- Selected a subset of products
- Identified the most similar product using text similarity
- Explained similarity logic and competitive positioning

---

## Key Concepts & Tools
- Natural Language Processing (NLP)
- Bag-of-Words & TF representations
- Cosine similarity
- Sentiment analysis
- Word embeddings (SpaCy, Gensim)
- Custom embedding training
- Python, Pandas, NumPy, Scikit-learn

---

## Results & Insights
- Attribute-based recommendations better captured **user intent** than ratings alone
- Bag-of-Words outperformed embeddings when attributes were explicitly defined
- Custom embeddings improved semantic relevance in domain-specific contexts
- Highlighted trade-offs between interpretability and semantic richness

---
