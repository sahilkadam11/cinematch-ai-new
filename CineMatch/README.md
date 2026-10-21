# 🎬 CineMatch — Content-Based Movie Recommendation System

A lightweight **AI & Data Science mini project** that recommends similar movies using **weighted content vectors and cosine similarity**. Entirely client-side: **no backend, API key, database, or npm installation** required.

## Features
- 32 curated movies, including international and Indian films
- Instant personalized recommendations (top 6 similar titles)
- Search by movie, actor, or director; genre filters and sorting
- Relative similarity scores and explanations showing shared features
- Responsive, dark-themed interface; completely offline-compatible

## How it works
Each movie has genres, theme keywords, director, and main cast. These become tagged tokens such as `genre_sci_fi` and `director_christopher_nolan`. Token weights use `(1 + ln((N + 1) / (document_frequency + 1)))` multiplied by category importance (genre 3, keyword 2, director 1.8, actor 1.3). Cosine similarity ranks movies by closeness. This **does not use an LLM, external recommender API, or neural network**; it is a classical information retrieval recommendation algorithm.

## Run locally
1. Download/extract this folder, open it in VS Code.
2. Double-click `index.html` (or use VS Code Live Server).
3. Search for a movie, click its card and see recommendations.

## Push to GitHub (new empty repository)
```bash
git init
git add .
git commit -m "Initial commit: CineMatch movie recommendation system"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/cinematch-movie-recommender.git
git push -u origin main
```
Create the GitHub repository **without** initializing a README to avoid non-fast-forward errors. If a README already exists remotely, use `git pull --rebase origin main` before pushing, resolving any conflicts.

## Deploy — GitHub Pages
In your repo, **Settings → Pages → Build and deployment → Deploy from a branch → main / (root) → Save**. Your website will appear at `https://YOUR_USERNAME.github.io/cinematch-movie-recommender/` after publishing.

## Files
- `index.html`: website markup
- `style.css`: visuals and responsive design
- `movies.js`: curated movie metadata
- `app.js`: TF-IDF-style vectors, cosine similarity, filters, and recommendations
- `README.md`: explanation and setup

## Limitations and future scope
Small subjective dataset, no viewing history or collaborative filtering, similarity scores are not probabilities or model accuracy. Enhance by importing a larger licensed dataset, evaluating Precision@K, and including user feedback.

**Project type:** AI & DS / Recommendation System | **App domain:** Entertainment | **Technical domain:** Content-based filtering, NLP-style metadata features, cosine similarity
