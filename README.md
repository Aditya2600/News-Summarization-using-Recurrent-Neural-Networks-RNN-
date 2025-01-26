# Inshorts News Summarization using LSTM

## Introduction
Inshorts is a news app started in 2013 that delivers news summaries in less than 60 words. This business use case demonstrates how to build a news summarization model using Recurrent Neural Networks (RNN).

## Objective
We aim to develop a model that takes news articles of 40-60 words as input and generates a summary of less than 30 words.

## Steps to Implement

### 1. Data Collection
- Collect a dataset of news articles and their respective summaries.
- Ensure the dataset includes news articles between 40-60 words and their respective summaries of less than 30 words.

### 2. Data Preprocessing
- Clean and tokenize the text data.
- Remove stopwords, punctuations, and irrelevant characters.
- Convert text into sequences using tokenization.
- Split the dataset into training and testing sets.

### 3. Model Architecture
We will use an Encoder-Decoder architecture with LSTM.

#### Encoder
- Input: Sequence of words from the news article.
- Layer: LSTM to encode the input into a context vector.

#### Decoder
- Input: Context vector from the encoder.
- Layer: LSTM to generate the summarized text.

### 4. Training
- Use the training data to train the model.
- Loss function: Categorical Crossentropy.
- Optimizer: Adam or RMSprop.

### 5. Evaluation
The model's performance is evaluated using metrics like ROUGE. Below are some sample results from the evaluation:

| Actual Summary | Predicted Summary | ROUGE Precision | ROUGE Recall | ROUGE F1 |
|----------------|-------------------|-----------------|--------------|----------|
| start deepika denies starring as amrita in bhansali s film end | start deepika to play in biopic on padmavati row report end | 0.363636 | 0.363636 | 0.363636 |
| start shahid takes care of ishaan me on being single mom end | start my son taimur is a dream to be a on my burkha end | 0.285714 | 0.333333 | 0.307692 |
| start pilot dies on board airways plane mid air end | start pilot flyers to fly plane with emergency landing end | 0.400000 | 0.400000 | 0.400000 |
| start celebrations begin at ram nath kovind s village end | start pm modi to be called by a dictator in uk end | 0.166667 | 0.200000 | 0.181818 |
| start guest their heads in protest in mp end | start women wear skirts in protest against end | 0.500000 | 0.444444 | 0.470588 |
| start can t tolerate weinstein like behaviour in hollywood end | start i don t know how to be used to stop facing end | 0.266667 | 0.400000 | 0.320000 |
| start gujarat poll panel orders probe in contract end | start ec orders removal of using fake news online end | 0.250000 | 0.272727 | 0.260870 |
| start facebook suspends canadian firm amid data breach end | start facebook suspends facebook over fake news end | 0.600000 | 0.600000 | 0.600000 |
| start iraq s first non arab president passes away end | start iraq s 1st state citizen to be held in end | 0.333333 | 0.400000 | 0.363636 |
| start us scientists propose new organ in human body end | start scientists propose new type of human system end | 0.666667 | 0.600000 | 0.631579 |

### 6. Deployment
- Deploy the trained model in a backend server or integrate it into a mobile app for real-time news summarization.

## Results
- The model successfully summarizes news articles of 100 words to under 15 words.
- Performance metrics:

  - ROUGE: Varies as shown above.

## Future Enhancements
- Experiment with transformers like BERT or T5 for improved accuracy.
- Incorporate multilingual summarization support.

## Repository Structure
```
├── data
│   ├── raw_data.csv
│   ├── processed_data.csv
├── models
│   ├── news_summarization_model.h5
├── src
│   ├── train.py
│   ├── preprocess.py
│   ├── inference.py
├── README.md
```

---

For more details, refer to the [GitHub Repository](https://github.com/Aditya2600/News-Summarization-using-Recurrent-Neural-Networks-RNN).
