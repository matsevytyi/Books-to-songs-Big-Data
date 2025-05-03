# Books-to-songs-Big-Data

Our system follows the best pratices and combines two recommendation approaches: collaborative and content-based filtering

## Collaborative filtering

## Content-based filtering

<img width="918" alt="Знімок екрана 2025-05-03 о 23 02 07" src="https://github.com/user-attachments/assets/bba98926-999f-4d5d-9517-a0e81afc52fc" />


Workflow for content-based filtering
1. When user want to pick a song for particular book, we pick the book name
2. Select the row from the dataset if it exists and pick the necessary features (i.e. title, genre)
3. If the book does not exit, we proceed just with the title
4. Embed it into a vector using language encoder
5. Obtain top_N results in FAISS
6. Map then to the song names

TODO:
1. For existing records (both for songs and books) in dataset we compute vector embeddings and store them in golden layer
2. Then we push them to FAISS for quick vector search
3. Save golden layer
4. Save faiss

5. working end-to-end code is already in `small_scale_content_based_filtering.ipynb`, but you need to modify the tables and fields names up to your use case (I created only general approach)
