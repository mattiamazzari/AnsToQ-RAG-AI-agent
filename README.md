# FaqSense: E-commerce FAQ Chatbot System

## Overview

This project is designed to create a Retrieval-Augmented Generation (RAG) system that interacts directly with users by retrieving relevant information from a pre-existing FAQ dataset. The system is intended for use in e-commerce environments where users frequently have questions about products, shipping, returns, and other common topics. Instead of making users search through an FAQ page, the system provides direct answers through a chat interface.

## Dataset

The FAQ data used in this project is sourced from the [Ecommerce-FAQ-Chatbot-Dataset](https://www.kaggle.com/datasets/saadmakhdoom/ecommerce-faq-chatbot-dataset) on Kaggle. This dataset contains a list of JSON objects, each representing a frequently asked question along with its corresponding answer.

## How It Works

1. **Embedding the FAQ Data**:
   - The system converts the answers from the FAQ dataset into embeddings. These embeddings are stored in a vector store.
   - Optionally, the questions can be concatenated with the answers before converting them into embeddings. This approach is useful if the questions provide additional context that might enhance the retrieval performance.

2. **User Interaction**:
   - When a user asks a question via the chat interface, the system converts the query into an embedding.
   - The system then compares this query embedding with the embeddings stored in the vector store to find the most relevant answer.

3. **Response Generation**:
   - The system retrieves the best-matched answer and presents it directly to the user in a conversational format.
   - This process provides users with quick and accurate answers without the need to navigate through an FAQ page.

## When No FAQ Page Exists

If the e-commerce site does not have an existing FAQ page, the system can perform web scraping to gather FAQ data directly from the website. This involves extracting question-answer pairs from the website's FAQ section, which are then processed into embeddings and stored in the vector store, just like the pre-existing dataset.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/ecommerce-faq-chatbot.git
2. Import the notebook in Google Colab.

## Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue if you find any bugs or have suggestions for improvements.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.
