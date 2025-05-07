# Books-to-songs-Big-Data

This is a recommendation system that selects music for books based on emotions from reviews. Our system follows the best pratices and combines two recommendation approaches: collaborative and content-based filtering.

## Collaborative filtering

<img width="918" alt="Image" src="https://github.com/user-attachments/assets/dd45172d-b5da-484f-8fa4-d9798b21a776" />

#### Input data:
- user_id, book_id 
- parameters top_n_users, top_n_songs

#### Process:
- search for similar users → collect and rank songs

#### Output data:
- a list of recommended songs for a particular user and book

## Content-based filtering

<img width="918" alt="Знімок екрана 2025-05-03 о 23 02 07" src="https://github.com/user-attachments/assets/bba98926-999f-4d5d-9517-a0e81afc52fc" />

#### Input data:
- a vector of the target book
- a set of song vectors (FAISS)
- parameter top_n

#### Process:
- L2-normalisation of the vectors
- search for k nearest neighbours
- ranking

#### Output data:
- list of recommended songs for a specific book
