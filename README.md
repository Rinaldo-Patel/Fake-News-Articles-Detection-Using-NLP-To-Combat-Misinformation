# Fake-News-Articles-Detection-Using-NLP-To-Combat-Misinformation

# Description of Business Problem
The spread of fake news and misinformation through digital media platforms has become a major societal challenge. Misleading or false information influences public opinion, undermines democratic processes, and can even endanger lives during crises (e.g., pandemics or elections). Current content moderation systems on social media often struggle to detect and flag fake news effectively and in real-time. This project aims to utilize natural language processing to develop a machine learning classifier that can accurately detect fake news articles based on their textual content. The ultimate goal is to assist media platforms, fact-checking organizations, and the general public in distinguishing between credible and deceptive news content, enabling proactive content moderation, and reducing the spread of misinformation.

# Objective
This project aims to build and evaluate a binary classification model for a text-only dataset that labels the articles as real or fake. To create a model that acts as a supportive tool for decision makers, such as fact-checkers, content moderators, and news platforms, to determine the legitimacy of the content.

# Dataset and Source of Data
This project uses the WELFake Dataset, an open-source dataset curated to support the development of robust fake news detection models.
Source: https://zenodo.org/records/4561253
The dataset contains 72,134 labeled news articles compiled from four popular datasets to ensure diversity and minimize overfitting. Each entry includes: title, headline of the article, text: full article body, label: 1 for fake, 0 for real. The article's text has an average word count of 550 words. This mildly unbalanced dataset supports both traditional ML and deep NLP approaches.

# Motivation 
With the dawn of a new age of social media platforms, online news publications, and platforms, rapid circulation of misinformation has become a huge issue. This overwhelms the various content editors and platforms by manually sifting through humungous volumes of content under extremely tight constraints. Manual reviews not only take time but are also susceptible to errors. There's a serious requirement for automated models that flag high-risk fake articles for human review while minimizing false alarms. My motivation is to provide actionable evidence on the model combinations that deliver the best efficiency, accuracy, stability, and balance for text-only fake-news screening. This project touches upon the main concepts of Natural Language Processing, covering both unsupervised and supervised machine learning, thus giving a good idea of the practical applications of their combination. 

# Business Relevance
Tackling misinformation is a huge task for many people. It will help personnel in the newsroom, fact-checkers, to prioritize high-risk articles and save time. For platforms to ensure the best service for their audiences. For advertisers, ensuring brand safety would prevent their ads from being placed next to deceptive or misleading content. Automation will lead to time & resource savings with 24/7 coverage. It can instantaneously flag content at any time, which would be critical during a global crisis or unforeseen black swan events. Provides a clean, organized experience for the users reading these articles as they would get cleaner feeds, leading to minimal complaints and reducing the churn of viewers. It enhances the engagement of users on the platform, protecting the reputation. The same model can be used for other use cases, such as clickbait and spam detection.

# Limitations 
a) The Entire dataset could not be run for all the vectorizers, embeddings, and Machine learning models due to resource and cost constraints. 
b) Hyperparameter tuning could not be performed for all the models due to the dataset size and resource constraints
c) Down-sampling & balance - Trained on a 44k balanced subset of. This may result in a reduction in topical diversity and alter real-world base rates.
d) Dataset noise - WELFake aggregates prior datasets. Thus, labels may be imperfect. Models can learn to fit noisy annotations, inflating apparent performance.


# Conclusion
This project was initiated to identify a practical, high-accuracy approach to text-heavy fake-news detection, which delivered the result that sparse features alongside dimensionality reduction prove to be the best way to classify articles as fake or not fake. Across 196 experiments, BoW/TF-IDF paired with tree ensembles and neural networks consistently outperformed all the other models. There was proper in-domain generalization and gave results without overfitting. The rigorous data cleaning created clean tokens, which helped extract meaning from the articles. Dimensionality reduction helps prevent erroneous results and gives the right balance. The best results in terms of all the evaluation metrics were derived from Dimensionality reduced Bag of Words, and Feedforward Neural Network was the leading model. Thus, Bag of Words should be the vectorizer of choice, and Neural network models should be chosen for getting the best results. This model can be translated into the real world with small tweaks, which will give excellent results in the detection of fake articles and aid platforms to give the best user experience to their customers.
