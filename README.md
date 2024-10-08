# -Mental-Health-Condition-Monitoring-from-Social-Media

## Project Title: Mental Health Condition Monitoring from Social Media.
![image](https://www.economist.com/cdn-cgi/image/width=1424,quality=80,format=auto/content-assets/images/20240427_STD002.jpg)





## Introduction

In recent years, there has been growing recognition of the importance of mental health and well-being. However, identifying and addressing mental health conditions in a timely manner remains a significant challenge. Traditional methods of monitoring mental health, such as clinical assessments and surveys, often suffer from limitations such as high cost, stigma, and delays in data collection and analysis.Mental health conditions, including depression, anxiety, and suicidal ideation, affect millions of individuals worldwide. Social media platforms have emerged as a valuable source of data for monitoring and understanding mental health trends and behaviours.
This project aims to leverage natural language processing (NLP) techniques to analyze social media posts, particularly tweets from Twitter, to detect signs of mental health conditions and identify individuals at risk of suicidal ideation. By harnessing the power of social media data, we seek to provide early interventions and support for those in distress.

## Objectives

1) Machine Learning Models for Linguistic Markers: Develop machine learning models capable of detecting linguistic markers and patterns indicative of mental health conditions, such as depression and suicidal ideation, within social media posts.

2) Actionable Alerts for Timely Interventions: Provide actionable alerts generated by the system to mental health professionals, crisis intervention teams, and social media platform moderators. These alerts facilitate timely interventions and support for individuals identified as being at risk, thereby potentially preventing self-harm or suicide attempts.
These objectives outline a comprehensive approach aimed at leveraging machine learning and real-time monitoring technologies to address mental health challenges on social media platforms effectively.

## Dataset:
<img width="727" alt="image" src="https://github.com/user-attachments/assets/19700136-7cde-49aa-8a07-291abee4118d">

Kaggle link - https://www.kaggle.com/datasets/nikhileswarkomati/suicide-watch

### Dataset Details

The dataset utilized in this analysis originates from Kaggle and comprises posts from the "SuicideWatch" and "depression" subreddits on Reddit, acquired through the Pushshift API.
Specifically, posts from "SuicideWatch" were collected from December 16, 2008 (the subreddit's inception) to January 2, 2021.

Posts from the "depression" subreddit were gathered from January 1, 2009, to January 2, 2021.

Categorized labeling assigns posts from "SuicideWatch" as suicide-related, while those from the "depression" subreddit are marked as pertaining to depression.

Additionally, non-suicidal posts are drawn from the "teenagers" subreddit.

Initially, the dataset featured labels solely for suicide and non-suicide posts.

Subsequent iterations, such as version V13, expanded the labeling scheme to encompass depression and normal conversations among teenagers.

Supplementary documentation, in the form of a notebook, illustrates the methodology for obtaining Reddit posts via the PushShift API.

## AI Models Used

Model Description
Summary:Long short-term memory (LSTM) is a type of recurrent neural network (RNN)
aimed at dealing with the vanishing gradient problem present in traditional RNNs. Its relative
insensitivity to gap length is its advantage over other RNNs, hidden Markov models and other
sequence learning methods. It aims to provide a short-term memory for RNN that can last
thousands of timesteps, thus "long short-term memory". It is applicable to classification,
processing and predicting data based on time series, such as in handwriting, speech recognition,
machine translation, speech activity detection,robot control video games,and healthcare.
CNN is a deep learning model commonly used for image recognition tasks, but it can also be
applied to sequential data such as text through the use of 1D convolutions.
Usage in Project: LSTM and CNN was adapted for text classification to capture local patterns
and features within social media posts. It learned to detect specific linguistic patterns associated
with suicidal ideation, aiding in the detection process.
These models, along with K-Fold Cross-Validation, collectively formed the core components of
the project's machine learning pipeline. They were instrumental in developing a comprehensive
system for detecting linguistic markers and patterns associated with mental health conditions in
social media posts, ultimately contributing to the goal of early intervention and support for
at-risk individuals


## Classification Results
<img width="538" alt="image" src="https://github.com/user-attachments/assets/ba8577ec-e615-4e3a-91bb-bea8a23be594">

1. Training without cross validation
Training with Bidirectional Long Short-Term Memory (CNN-BiLSTM) represents a powerful
approach in natural language processing (NLP) tasks, particularly for tasks involving sequential
data like text. This hybrid architecture combines the strengths of Convolutional Neural Networks
(CNNs) and Bidirectional Long Short-Term Memory (BiLSTM) networks to capture both local
and global dependencies within the input sequences. CNNs excel at extracting local features and
patterns, while BiLSTMs are adept at modeling long-range dependencies and capturing
contextual information. By integrating these two architectures, CNN-BiLSTM models can
effectively capture hierarchical representations of text data, enabling them to learn intricate
patterns and nuances present in the input sequences. During training, the model undergoes
iterative optimization processes, where the weights of the CNN and BiLSTM layers are updated
through backpropagation, minimizing the loss function and enhancing the model's ability to
make accurate predictions. Through this training process, CNN-BiLSTM models can achieve
state-of-the-art performance in various NLP tasks, including text classification, sentiment
analysis, and language translation.

<img width="564" alt="image" src="https://github.com/user-attachments/assets/d47a1d04-cd68-4499-bcc6-a511607f7a93">

2) Training with K-fold cross validation
Optimizer Used: Adamax is an optimization algorithm commonly used in deep learning models.
It is a variant of the Adam optimizer, which is well-suited for training neural networks with large
datasets and high-dimensional parameter spaces. Adamax adapts the learning rate during
training, allowing for efficient convergence and improved performance.
Key Features of Adamax: Adamax dynamically adjusts the learning rate for each parameter
based on the magnitude of past gradients and exponentially decaying averages of past squared
gradients.Efficient Parameter Updates: Adamax efficiently updates model parameters, especially
in high-dimensional spaces, by maintaining separate learning rates for each parameter.Stability:
Adamax offers improved stability during training compared to traditional stochastic gradient
descent (SGD), leading to faster convergence and better generalization.Robustness: Adamax is
robust to noisy gradients and sparse data, making it suitable for a wide range of deep learning
tasks. In the k-fold method, the Adamax optimizer is used to optimize the model's parameters
during each training iteration across different folds of the dataset. This helps in achieving optimal
performance and generalization across the entire dataset while mitigating overfitting.
<img width="739" alt="image" src="https://github.com/user-attachments/assets/d7ad8555-6545-4b41-990d-c0e568e62c44">
<img width="655" alt="image" src="https://github.com/user-attachments/assets/cd99d8c4-9ddf-4b94-94ea-12d915107a92">


## Results
<img width="634" alt="image" src="https://github.com/user-attachments/assets/95495147-9c69-4348-b5ec-4507476e46ae">


## Future Scope and Limitations
Future Scope:
Multi-platform Integration: Extend analysis to multiple social media platforms.
Multimodal Analysis: Incorporate diverse data types like images and audio.
Real-time Intervention: Implement immediate support mechanisms.
Longitudinal Analysis: Track changes in mental health states over time.
User Engagement Monitoring: Identify individuals at risk of social isolation.

Limitations:
Data Bias: Risk of biased training data.
Privacy Concerns: Need for stringent data protection measures.
Algorithmic Accuracy: Models may produce false results.
Generalization Challenges: Performance variation across demographics.
Ethical Considerations: Stigmatization and consent concerns must be addressed.


## Conclusion

In conclusion, our project represents a significant stride towards harnessing the power of machine learning and deep learning techniques for early detection and intervention in mental health crises through analysis of social media content. By leveraging models such as Convolutional Neural Networks (CNN) and employing K-fold cross validation, we have developed a robust system capable of identifying linguistic markers and patterns associated with mental health conditions, including depression and suicidal ideation.
Through the integration of these models into a scalable, real-time monitoring system for social media platforms like Twitter, we have paved the way for proactive identification of individuals at risk of self-harm or suicide. Our project not only offers actionable alerts to mental health professionals, crisis intervention teams, and platform moderators but also underscores the ethical imperative of responsible AI-driven interventions in mental health. As we continue to refine and expand upon our methodologies and technologies, we remain steadfast in our commitment to leveraging cutting-edge advancements in machine learning for the betterment of society. Together, we can strive towards a future where early detection, timely intervention, and compassionate support are the cornerstones of mental health care in the digital age.


## REFERENCES
Aldhyani THH, Alsubari SN, Alshebami AS, Alkahtani H, Ahmed ZAT. Detecting and Analyzing Suicidal Ideation on Social Media Using Deep Learning and Machine Learning Models. Int J Environ Res Public Health. 2022 Oct 3;19(19):12635. doi: 10.3390/ijerph191912635. PMID: 36231935; PMCID: PMC9565132.
https://www.kaggle.com/datasets/nikhileswarkomati/suicide-watch


## Authors/Contributors


- [Resham Hansdah](https://github.com/Resham0007)
- [Sonali Kishan](https://github.com/sonalikishan)
- [Subham Beura](https://github.com/Subham-Beura/Subham-Beura)
