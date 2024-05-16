# NLP Summarization of Privacy Policies
## Project Overview
This project aims to develop an efficient method for summarizing privacy policy documents using NLP (Natural Language Processing) abstractive text summarization models. Privacy policies are often lengthy and complex, making it difficult for users to quickly understand the key points. By summarizing these documents, we aim to provide users with concise and comprehensible summaries.
I have implemented three different models for this task:
•	BART (Bidirectional and Auto-Regressive Transformers)
•	T5 (Text-To-Text Transfer Transformer)
•	BERT (Bidirectional Encoder Representations from Transformers) in an encoder-decoder configuration
## Dataset
The dataset comprises various privacy policies collected from multiple sources. The dataset was preprocessed and split into three subsets to facilitate training, validation, and testing of the models. The split ratios are as follows:
•	Training Set: 80% of the dataset
•	Validation Set: 10% of the dataset
•	Test Set: 10% of the dataset
## Models Implemented
1.	BART Model:
•	BART is a denoising autoencoder for pretraining sequence-to-sequence models. It is particularly effective for tasks like text generation, translation, and summarization.
2.	T5 Transformer Model:
•	T5 treats all NLP tasks as text-to-text tasks. It is highly versatile and has shown excellent performance on a wide range of tasks, including summarization.
3.	BERT Model:
•	BERT is designed to understand the context of words in a sentence. For this project, BERT is configured in an encoder-decoder setup to perform the summarization task.
## Training and Evaluation
All models were trained using the Google Colab environment to leverage its computational resources. After training, the models were saved to Google Drive for easy access and deployment.
Each model was used to generate summaries for a set of texts. These summaries were then evaluated using the ROUGE metrics, which compare the overlap of n-grams between the generated summary and a reference summary. The ROUGE scores were averaged to provide a comprehensive performance comparison.
## Results
The evaluation results indicated that the T5 Transformer model outperformed the other models. Below are the visualized results of the average precision, recall, and F-measure scores:
Average Precision Scores
<img width="1018" alt="Screenshot 2024-05-14 at 9 47 11 AM" src="https://github.com/RohithJ11/NLP_Privacy_Policies/assets/165297272/b3a39e79-103d-4e67-8765-ad79514a8447">

•	T5: Exhibits the highest precision across all ROUGE types, indicating that its generated summaries closely match the reference summaries in terms of relevant content.
•	BERT: Performs moderately well, particularly in ROUGE-1, showing that it captures many relevant unigrams.
•	BART: Has the lowest precision scores among the three models, suggesting its summaries are less concise compared to the reference summaries.

Average Recall Scores
•	BERT: Leads in recall scores, especially in ROUGE-1 and ROUGE-L, indicating it captures a broader range of relevant content from the original texts.
•	BART: Follows closely with strong performance in ROUGE-2 and ROUGE-L, showing it captures relevant bigrams and long sequences well.
•	T5: Has the lowest recall scores, despite its high precision, suggesting it generates more concise but slightly less comprehensive summaries.

Average F-measure Scores
•	T5: Scores highest on the F-measure, balancing precision and recall effectively, making it the best performer overall.
•	BART and BERT: Have similar F-measure scores, with BART slightly ahead in ROUGE-L, indicating a balanced but slightly less effective performance compared to T5.
#Conclusion
Based on the average ROUGE scores, the T5 Transformer model is the most effective for summarizing privacy policies among the models tested in this project. Its balance of precision and recall makes it particularly suitable for generating concise and accurate summaries.



