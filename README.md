<h1>Chat Conversation Intent Classifier</h1>

<h2>Overview</h2>
<p>This project focuses on classifying customer chat messages into predefined intent categories using Natural Language Processing (NLP) and Machine Learning techniques.
The goal is to identify whether a given message represents a Complaint, Query, or Feedback.</p>
<p>The model analyzes textual patterns and learns distinguishing features to accurately classify user intent in customer conversations.</p>

<h2>Objective</h2>
<ul>
  <li>Classify chat messages into Complaint, Query, or Feedback</li>
  <li>Build a complete NLP pipeline for multi-class classification</li>
  <li>Understand feature extraction using TF-IDF</li>
  <li>Evaluate model performance using standard metrics</li>
</ul>

<h2>Dataset</h2>
<p>The dataset used contains customer service conversations labeled with multiple intent categories.</p>
<p>Each record includes:</p>
<ul>
  <li>Text input (user message)</li>
  <li>Intent label</li>
</ul>

<p>The original dataset contains multiple intent classes which were mapped into three categories:</p>
<ul>
  <li>Complaint – refund issues, delivery problems, payment issues</li>
  <li>Query – order status, product inquiries, help requests</li>
  <li>Feedback – reviews, greetings, appreciation</li>
</ul>

<p>Dataset Link: <a href="https://www.kaggle.com/datasets/scodepy/customer-support-intent-dataset" target="_blank">
https://www.kaggle.com/datasets/scodepy/customer-support-intent-datasett</a></p>

<h2>Tech Stack</h2>
<ul>
  <li>Python</li>
  <li>Pandas, NumPy</li>
  <li>Matplotlib</li>
  <li>Scikit-learn</li>
  <li>Natural Language Processing (NLP)</li>
</ul>

<h2>Data Preprocessing</h2>
<p>Text data was cleaned and standardized before training the model:</p>
<ul>
  <li>Converted text to lowercase</li>
  <li>Removed URLs</li>
  <li>Removed special characters and punctuation</li>
  <li>Handled missing values</li>
  <li>Stored cleaned text in a separate column</li>
</ul>
<p>These steps help reduce noise and improve model performance.</p>

<h2>Exploratory Data Analysis (EDA)</h2>
<p>Initial analysis and visualizations were performed:</p>
<ul>
  <li>Distribution of intent classes</li>
  <li>Text length distribution</li>
  <li>Inspection of cleaned versus original text</li>
</ul>
<p>This helped in understanding dataset structure and class balance.</p>

<h2>Feature Engineering</h2>
<h3>TF-IDF Vectorization</h3>
<p>Text data was converted into numerical form using TF-IDF:</p>
<ul>
  <li>Transforms text into numerical feature vectors</li>
  <li>Captures importance of words and phrases</li>
  <li>Reduces the influence of common words</li>
</ul>
<p>This allows machine learning models to effectively process textual input.</p>

<h2>Model Building</h2>
<h3>Algorithm Used: Logistic Regression</h3>
<ul>
  <li>Supervised learning algorithm suitable for multi-class classification</li>
  <li>Efficient and scalable for large datasets</li>
  <li>Performs well with high-dimensional sparse text data</li>
</ul>
<p>The model was trained on TF-IDF-transformed features to classify user intent.</p>

<h2>Model Evaluation</h2>
<p>The model was evaluated using:</p>
<ul>
  <li><b>Accuracy Score</b> to measure overall performance</li>
  <li><b>Confusion Matrix</b> to analyze prediction errors</li>
  <li><b>Classification Report</b> including:
    <ul>
      <li>Precision</li>
      <li>Recall</li>
      <li>F1-score</li>
    </ul>
  </li>
</ul>
<p>These metrics provide detailed insights into model performance across all classes.</p>

<h2>Visualizations</h2>

<h3>Intent Distribution</h3>
<p>Shows the distribution of Complaint, Query, and Feedback in the dataset.</p>
<img src="https://github.com/IshitaSinha2002/Customer-Intent-Classifier/blob/main/Intent%20Dist.png" width: 500px; height: 400px; object-fit: cover;>

<h3>Confusion Matrix</h3>
<p>Displays actual versus predicted classifications.</p>
<img src="https://github.com/IshitaSinha2002/Customer-Intent-Classifier/blob/main/Confusion%20Matrix.png" width: 500px; height: 400px; object-fit: cover;>

<h2>Key Insights</h2>
<ul>
  <li>The dataset contains diverse real-world customer interactions</li>
  <li>Mapping multiple intents into three categories simplifies classification</li>
  <li>TF-IDF effectively captures meaningful text patterns</li>
  <li>Logistic Regression performs well for intent classification</li>
</ul>

<h2>Prediction System</h2>
<p>A prediction system was implemented to classify new user messages.</p>
<p>The process involves:</p>
<ul>
  <li>Cleaning the input text</li>
  <li>Transforming it using the trained TF-IDF vectorizer</li>
  <li>Passing it to the trained model</li>
  <li>Returning the predicted intent</li>
</ul>

<h3>Sample Input and Output</h3>
<p>Input: Where is my order? <br>
Intent: Query</p>

<h2>Conclusion</h2>
<p>This project demonstrates how NLP and machine learning techniques can be applied to understand customer intent in conversations.
It provides a complete workflow from preprocessing and feature extraction to model evaluation and prediction.</p>
