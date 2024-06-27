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
        <img src="https://private-user-images.githubusercontent.com/133969661/343965090-c1675022-a2e7-4303-b00c-92530aeb2088.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk1MjY0MTEsIm5iZiI6MTcxOTUyNjExMSwicGF0aCI6Ii8xMzM5Njk2NjEvMzQzOTY1MDkwLWMxNjc1MDIyLWEyZTctNDMwMy1iMDBjLTkyNTMwYWViMjA4OC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyN1QyMjA4MzFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1lNmE4N2ZlMWYyNGJjZGM0ZWZhZjRlNTgxZTEzODM1NzNiZTYyNTAyYjJkNmQ5MzJlYmFiYzg0NTg3NDI4OWNiJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.S5jMlnwQarDqXRwKZM_9SnzvYBeQKdJyT0ZtCioNJE4" alt="Image Description">
        <figcaption>First Evaluation(before add new features)</figcaption>
    </figure>
  <figure>
        <img src="https://private-user-images.githubusercontent.com/133969661/343965206-1954ea4d-487a-4c4f-a2bf-2de52a83769d.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk1MjY0MTEsIm5iZiI6MTcxOTUyNjExMSwicGF0aCI6Ii8xMzM5Njk2NjEvMzQzOTY1MjA2LTE5NTRlYTRkLTQ4N2EtNGM0Zi1hMmJmLTJkZTUyYTgzNzY5ZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyN1QyMjA4MzFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02ZTYyNmM3YWEyNmE2MDllMGJhODliMTc4YTRiYTUwN2NlNGUzZDFhNGFkMWQ0ZDE4NjQxNDBhY2I0MGFmOWU3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.IG4cdzJqranbQuFMmY-edldWTf3vF8I3uaCV7pOT2k0" alt="Image Description">
        <figcaption>Final Evaluation(after add new features)</figcaption>
    </figure>
  <img src="https://private-user-images.githubusercontent.com/133969661/343965162-95638f93-2b90-49bf-974f-9bc3341cf52f.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk1MjY0MTEsIm5iZiI6MTcxOTUyNjExMSwicGF0aCI6Ii8xMzM5Njk2NjEvMzQzOTY1MTYyLTk1NjM4ZjkzLTJiOTAtNDliZi05NzRmLTliYzMzNDFjZjUyZi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyN1QyMjA4MzFaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1mY2EwNzA5YmY3ZjRjMzU0YzE1MDNlNjhlMDc4NGFkZGE3OGIwYWVlYjc3YTlmYTdiNmRmODBhNDJkNDY5NDNmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.cVXgMiIZhd43OsX1TUZenDnmEz2f4LQb3PmnWQfKsmo" alt="Image Description">
        <figcaption>Model</figcaption>
    </figure>
</body>

  <h1>Avg Temp Prediction</h1>

<body>
    <h2>Project Description</h2>
    <p>In this code, we're using historical weather data to predict average temperatures using a type of deep learning model called LSTM. We start by preparing the data: removing unnecessary columns, encoding city names, and handling missing values. Then, we split the data into training and testing sets and scale it for the model. The LSTM model is set up with layers for learning patterns in the data. We train the model using the training data and validate its performance with the test data. Finally, we make predictions for future temperatures and adjust them back to their original scale for analysis.
    </p>

   <figure>
        <img src="https://private-user-images.githubusercontent.com/133969661/343966872-b7bba123-2346-4397-8a04-9eee6ba5d92d.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk1MjY5MjUsIm5iZiI6MTcxOTUyNjYyNSwicGF0aCI6Ii8xMzM5Njk2NjEvMzQzOTY2ODcyLWI3YmJhMTIzLTIzNDYtNDM5Ny04YTA0LTllZWU2YmE1ZDkyZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNjI3JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDYyN1QyMjE3MDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02Y2E1YmFjMTI5NGY1NzViMWU5MzIwYTc4OGFiOWQyNDZhNDgyOThlZTI0N2I3ZjhiY2MyN2IzZTA1ODllYTUwJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.vBfneg56ksbMcRKwxbyvhuYpBm-Le_9lc-3OqDLpVqg" alt="Image Description">
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
