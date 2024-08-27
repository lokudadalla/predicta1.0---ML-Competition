# predicta1.0---ML-Competition

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
      <h1>Weather Classification</h1>

<body>
    <h2>Project Description</h2>
    <p>
        First, I analyze the data to identify the most and least important features. I then remove the less important features. Afterward, I split the data into training and test sets. To improve preprocessing, I use a method named Pipeline and also apply SMOTE to balance the imbalanced classes in the data. I employ XGBoost as the model and fine-tune some hyperparameters to achieve better results and reduce overfitting. Then, I predict using the model and evaluate it to determine its performance. Upon realizing that the F1 scores for "Thunderstorm," "Light Perception," and "Partly Cloudy" were lower compared to others, I added new features to enhance performance. Finally, I reran the model.
    </p>
   <figure>
        <img src="https://github.com/lokudadalla/predicta1.0---ML-Competition/blob/040c5138b5a193111b6e27e1a3e1bbaf64b46f75/images/1.png" alt="Image Description">
        <figcaption>First Evaluation(before add new features)</figcaption>
    </figure>
  <figure>
        <img src="https://github.com/lokudadalla/predicta1.0---ML-Competition/blob/c5825bdd35fd3cccd7ed1eeb89ff70a33da4bc98/images/2.png" alt="Image Description">
        <figcaption>Final Evaluation(after add new features)</figcaption>
    </figure>
  <img src="https://private-user-images.githubusercontent.com/133969661/343965162-95638f93-2b90-49bf-974f-9bc3341cf52f.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjM5MTAzNTksIm5iZiI6MTcyMzkxMDA1OSwicGF0aCI6Ii8xMzM5Njk2NjEvMzQzOTY1MTYyLTk1NjM4ZjkzLTJiOTAtNDliZi05NzRmLTliYzMzNDFjZjUyZi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwODE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDgxN1QxNTU0MTlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zNGI2M2ZjNjJiZmZlZThlZWUwNjYxODlhNzg4NDExOThjN2VkYzkzNTY4Y2M0NWQyOWY2NGY4NWYzNWRhM2YyJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.qhl8DCz04bHXaUho8H1HHfm3yCsDOOBCSjF4ldBe6Ks" alt="Image Description">
        <figcaption>Model</figcaption>
    </figure>
</body>

  <h1>Avg Temp Prediction</h1>

<body>
    <h2>Project Description</h2>
    <p>In this code, we're using historical weather data to predict average temperatures using a type of deep learning model called LSTM. We start by preparing the data: removing unnecessary columns, encoding city names, and handling missing values. Then, we split the data into training and testing sets and scale it for the model. The LSTM model is set up with layers for learning patterns in the data. We train the model using the training data and validate its performance with the test data. Finally, we make predictions for future temperatures and adjust them back to their original scale for analysis.
    </p>

   <figure>
        <img src="https://private-user-images.githubusercontent.com/133969661/343966872-b7bba123-2346-4397-8a04-9eee6ba5d92d.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjM5MTAzNTksIm5iZiI6MTcyMzkxMDA1OSwicGF0aCI6Ii8xMzM5Njk2NjEvMzQzOTY2ODcyLWI3YmJhMTIzLTIzNDYtNDM5Ny04YTA0LTllZWU2YmE1ZDkyZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwODE3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDgxN1QxNTU0MTlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNTNjNmM0MDg1NTI5NWIzY2VkYjI4YWI0YWFhMmEwMWUwM2NmNzRkNmQwNWM4YzkwMGE3MGNjNDYzN2FjN2RlJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.Zx-bQP1wpHdhI-XgD3MqojKugcOwZCr4mJTBkqRmF14" alt="Image Description">
        <figcaption>First Evaluation(before add new features)</figcaption>
    </figure>
</body>

<h2>Resources</h2>

<ul>
    <li><a href="https://www.kaggle.com/competitions/predicta-1-0-predict-the-unpredictable-part-2/data">Dataset for weather classification</a></li>
    <li><a href="[/code/preprocess.py](https://www.kaggle.com/competitions/predicta-1-0-predict-the-unpredictable/data)">Dataset for Avg Temp Prediction</a></li>
    <li><a href="https://www.geeksforgeeks.org/smote-for-imbalanced-classification-with-python/">SMOTE Details</a></li>
    <li><a href="https://medium.com/analytics-vidhya/how-to-apply-preprocessing-steps-in-a-pipeline-only-to-specific-features-4e91fe45dfb8)">Pipeline Technique Details</a></li>
</ul>

<p>For more details, check out the <a href="https://github.com/yourusername/yourrepository/wiki">Wiki</a>.</p>

</body>
</html>

</html>
