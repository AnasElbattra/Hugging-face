# NLP News Understanding Project
<img src="https://raw.githubusercontent.com/News-Understanding/News-App/main/assets/images/logo.jpg" alt="Logo" width="200"/>

## Project Overview
The purpose of this project is to understand news articles through various NLP tasks, including topic classification, fake vs real classification, bias classification, sentiment analysis, and summarization. The goal is to enable users to quickly assess the relevance and trustworthiness of news articles.

### Fake vs Real Classification
We collected data from Hugging Face and Kaggle, using three datasets to fine-tune the T5-small model. The accuracy ranges from 87% to 97% across different datasets (see Figure 1 for comparison). The model effectively distinguishes between fake and real news.

### Bias Classification
Data for bias classification is sourced from AllSides News and MediaBiasFactCheck. A mix of these datasets is created after careful cleaning to remove duplicates. The DistilBERT model is fine-tuned, achieving accuracy scores of 75% and 94% on separate datasets (see Figure 2).

### Sentiment Analysis
To handle news about various topics, Gemini Pro and GPT-4 are used for sentiment labeling. Data is fine-tuned on models such as XLNet, DistilBERT, and RoBERTa Large. RoBERTa Large yields the highest accuracy in sentiment analysis (see Figure 3).

### Topic Classification
Data for topic classification is gathered from Kaggle and Hugging Face. K-train is utilized for rapid fine-tuning, testing different classification methods. DistilBERT achieves the highest accuracy among the tested models.

### Summarization
Pegasus, BART Large, T5-Small, and T5-Base are employed for summarization. Evaluation is done manually and using Bert-score. BART and T5-Base outperform others in terms of word count and overall information extraction.

## Deployment
### Backend (Flask API)
We utilize Flask to create an API that integrates all fine-tuned models for classification and summarization. Preprocessing is adapted for each model, and the API returns a list of classifications (e.g., [Fake - L-Biased - Negative - Tech]). Ngrok is used to host the API online.

[Backend Repo](backend_repo_link)

### App
A user-friendly news app is developed, allowing users to check or browse news articles with pre-labeled classifications. The simple UI provides options to classify or summarize articles, connecting to the backend API.

[App Repo](https://github.com/News-Understanding/News-App#news-understanding-app)

## Video Demo
A video demo is provided to demonstrate the reliability of the models. Data generated from ChatGPT, labeled, and tested on the app is showcased.

[Link to Video Demo](video_demo_link)


Feel free to explore the repositories and video demo for a detailed understanding of the project. Contributions and feedback are welcome!