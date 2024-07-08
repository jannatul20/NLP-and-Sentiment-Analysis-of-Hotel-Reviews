# NLP-and-Sentiment-Analysis-of-Hotel-Reviews
### Objective
In the hospitality industry, understanding guest sentiment is crucial for improving customer satisfaction and driving business growth. This study explores the use of Natural Language Processing (NLP) and sentiment analysis techniques to analyze hotel reviews. We will compare the performance of two popular models, Vader and BERT, in capturing the sentiment expressed by guests. The goal is to identify which model delivers the most accurate assessment of sentiment in hotel reviews.

### Dataset
The dataset features hotel reviews scraped from TripAdvisor for 10 different cities. (Dubai, Beijing, Long, New York City, New Delhi, San Francisco, Shanghai, Montreal, Las Vegas, Chicago) each city containing a varying number of hotels where each hotel has text. The text fields featured within the dataset are date, review title and full review as shown in Fig 1. It contains approximately 259 000 reviews. For this project the focus was on 5 of the 10 cities London, Dubai, Delhi, Shanghai and New York. 

### Step-by-Step Procedure
-	Familiarize myself with different NLP techniques. [2,3,5] Mostly I learned details of the concepts of tokenizer, autotokenizer and how to perform TF-IDF (Term Frequency - Inverse Document Frequency) in week 1. [7,8] 
-	In week 1, I familiarized myself with various NLP techniques, including the concepts of tokenizer, autotokenizer, and performing TF-IDF. Specifically, I delved into the details of these techniques and gained a good understanding of them. 
-	In the next week, I also learned about Vader and Bert pretrained models and the concept of a pipeline. [9,10] I was able to implement these models and their pipelines effectively.
-	Moving on to the next week, I successfully implemented TF-IDF (Term Frequency - Inverse Document Frequency) on Dataset-1 and generated a list of the most relevant words for five cities.
-	In the following 2 weeks I have learned and implemented Vader (Valence Aware Dictionary and Sentiment Reasoner) sentiment analysis. I used this technique to analyze the reviews of four hotels in Dataset-1 and achieved satisfactory results.
-	After studying the Bert (Bidirectional Encoder Representations from Transformers) pre-trained model, I attempted to apply it to hotel reviews from Delhi. However, I encountered several challenges along the way. First, I discovered that the Bert model cannot accept input if the reviews exceed 256 tokens, and it does not work with non-English characters or languages other than English. Although most of the reviews in the dataset were in English, there were a few rows with reviews containing unfamiliar characters such as (? or !). Devanshi and I worked together to address this issue, I had to perform data cleaning again and remove those rows. In addition, I added a 'try except' loop to ignore rows with reviews that exceeded 256 words. Finally, I faced the challenge of requiring a GPU to run Bert, which was a new concept for me. I ended up paying for Colab Pro to use GPU and TPU to run the Bert model on the datasets of four cities (Dubai, Delhi, Shanghai, London), and obtained some useful results.
-	However, another challenge was that these datasets did not contain a rating column, so I could not compare the sentiments obtained from Bert and Vader with the original ratings.

### Sentiment Analysis with Vader and Bert
#### Vader
In order to implement the VADER sentiment analysis, the transformer and TensorFlow 
were installed, followed by importing the pipeline and downloading the VADER sentiment 
model. Then the VADER model was run on the entire dataset 1 to obtain the sentiments 
expressed in the dataset
#### Bert
- Bert is a pre-trained deep learning model which is developed by Google. This model is used 
for natural language processing (NLP) tasks, e.g., sentiment analysis. Hugging Face provides 
the platform for Bert and the Hugging Face transformers library contains lots of pre-trained 
BERT models.
[9] 
- In a Google Collab notebook, the "cardiffnlp/twitter-roberta-base-sentiment" model was 
imported after importing AutoTokenizer. [10] Next, a dictionary was created to store 
sentiments. Finally, a try-except loop was implemented within a ‘for loop’ to ignore longer 
reviews

### Insights from Vader and Bert Model
Bert model outperforms the Vader model in capturing sentiment. The Vader model tends to label a significant portion of sentiments as neutral, while the Bert model is more effective in distinguishing between different types of sentiments. 
![Screenshot_8-7-2024_144835_](https://github.com/jannatul20/NLP-and-Sentiment-Analysis-of-Hotel-Reviews/assets/113473117/0e37c10e-127b-445c-990f-3fa24ae67960)

As a result, when applied to the same dataset for each city, the Bert model detects more positive or negative sentiment compared to the Vader model. This suggests that the Bert model is a more reliable tool for sentiment analysis in this context. 
![Screenshot_8-7-2024_15646_](https://github.com/jannatul20/NLP-and-Sentiment-Analysis-of-Hotel-Reviews/assets/113473117/67d27290-b22c-4ef5-adf7-be6751d212ce)

### Comparison of Sentiment with Vader vs Bert for Shanghai

![shanghai-vader](https://github.com/jannatul20/NLP-and-Sentiment-Analysis-of-Hotel-Reviews/assets/113473117/5d54075c-1181-4663-b56b-3618eb09dbab)
![shanghai-bert](https://github.com/jannatul20/NLP-and-Sentiment-Analysis-of-Hotel-Reviews/assets/113473117/adb03fcf-4a10-4cd1-880f-442d1f21038d)


#### Collaborator:
- Jannatul Naeema
- Devanshi P
