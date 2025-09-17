# Multimodal Review Summarizer
This project provides an AI-powered approach to summarizing product reviews using multimodal LLMs to analyze product reviews by extracting valuable insights from both text and images. It utilizes image captioning, sentiment analysis, clustering, and text summarization techniques for effective review aggregation.

## Data Sources
The data for this project was obtained from the [Amazon Reviews'23](https://amazon-reviews-2023.github.io/) dataset. It is a large-scale **Amazon Reviews** dataset, collected in **2023** by [McAuley Lab](https://cseweb.ucsd.edu/~jmcauley/), and it includes rich features such as:

1. **User Reviews** (ratings, text, helpfulness votes, etc.);
2. **Item Metadata** (descriptions, price, raw image, etc.);
3. **Links** (user-item / bought together graphs).

**Home and Kitchen** category datasets were selected for the analysis, which contains 23.2 millions users, 3.7 millions items, 67.4 millions ratings, and 3.1 billions tokens in user reviews.

Images were collected using urls provided in the dataset.

- Reviews & Images collected via APIs and datasets, and uploaded to MongoDB server as amazon_23 database with meta and reviews collections.
- Data Cleaning & Processing performed using Pandas & MongoDB.
- Embeddings for clustering computed via SentenceTransformer.

## Code Description

* **Notebooks:**
	* `1_data_collection.ipynb`: This notebook performs data collection and preprocessing.
	* `2_image_captioning.ipynb`: This notebook handles image captioning using BLIP.
	* `3_review_summarization.ipynb`: This notebook summarizes reviews using LLMs.

## Dependencies
The project requires the following Python libraries:
- MongoDB, PyTorch, Transformers, TextBlob, KMeans
- BLIP for image captioning
- Ollama and LLama for LLM-based review summarization
- Matplotlib and Seaborn for visualization

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
