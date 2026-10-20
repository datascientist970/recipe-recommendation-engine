# Recipe Recommendation Engine

> A semantic recipe search engine that understands what you're craving — not just what you're typing.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-Web%20App-092E20?logo=django&logoColor=white)
![Sentence Transformers](https://img.shields.io/badge/Sentence%20Transformers-Embeddings-blue)
![Cosine Similarity](https://img.shields.io/badge/Ranking-Cosine%20Similarity-green)

## Overview

Most recipe sites only match keywords: type "chicken" and you get every title containing the word. The Recipe Recommendation Engine instead uses **semantic search** — your natural-language query ("quick vegetarian dinner", "chocolate dessert for a party") is converted into an embedding and compared against pre-computed recipe embeddings, so results are ranked by *meaning*, not by exact words.

The system returns the 10 most relevant recipes, each with a full detail page: ingredients, step-by-step instructions and an image.

## Key Features

- **Semantic search** — describe a craving, a mood, an occasion or dietary need in plain language
- **Smart recommendations** — top-10 recipes ranked by cosine similarity to the query embedding
- **Complete recipe details** — ingredients, detailed cooking instructions and images on every result
- **Fast search** — recipe embeddings are pre-computed, so queries are answered by vector comparison rather than re-processing the dataset
- **Clean interface** — a simple, intuitive search UI with AJAX-driven dynamic results

## How It Works

1. **Query processing** — the user's query is cleaned and converted into a numerical embedding with a Sentence Transformers model.
2. **Similarity matching** — the query embedding is compared with thousands of pre-computed recipe embeddings.
3. **Ranking** — recipes are sorted by cosine similarity to the query.
4. **Results** — the top 10 recipes are displayed with titles and images; each links to a full detail page.

## Tech Stack

- **Backend:** Django (Python)
- **Machine Learning:** Sentence Transformers (text embeddings)
- **Ranking:** Cosine similarity
- **Frontend:** HTML templates with AJAX for dynamic search
- **Data Processing:** Python-based preprocessing and embedding generation

## Project Structure

```text
recipe-recommendation-engine/
└── README.md   # Project documentation (design & system description)
```

> Note: this repository currently publishes the project's design and system documentation. The application follows a standard Django layout — a Django project with a search view that embeds the query, ranks recipes by cosine similarity against pre-computed embeddings, and renders result/detail templates via AJAX.

## Getting Started

For a standard Django deployment of this design:

```bash
git clone https://github.com/datascientist970/recipe-recommendation-engine.git
cd recipe-recommendation-engine
pip install django sentence-transformers pandas numpy scikit-learn
python manage.py runserver
```

Then open `http://127.0.0.1:8000/` and search in natural language.

## Usage

Try queries such as:

- *"quick vegetarian dinner"*
- *"chocolate dessert for parties"*
- *"healthy breakfast with eggs"*

Select any result to view its ingredients and step-by-step cooking instructions.

## Who Is It For?

- **Home cooks** discovering recipes from available ingredients or cravings
- **Meal planners** matching dietary requirements or time constraints
- **Cooking learners** exploring dishes by desired outcome, mood or occasion

## Author

**Muhammad Dawood** — AI & Data Science Engineer
GitHub: https://github.com/datascientist970 · Mardan, Pakistan
LinkedIn: https://www.linkedin.com/in/dawood406/
