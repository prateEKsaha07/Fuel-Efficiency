## what i did?
In this project, we cleaned and preprocessed an automobile dataset by handling missing values, encoding categorical features, and scaling numerical data. We then built a regression model using a TensorFlow Sequential neural network to predict MPG and evaluated its performance using MAE, achieving strong results (~1.62). Additionally, we explored traditional models like XGBoost for comparison. In the future, this project can be extended by using larger datasets, applying hyperparameter tuning, experimenting with advanced architectures, and deploying the model as a web application for real-time predictions.

## Dataset overview
* Total records: 398
* Features: cylinders, displacement, horsepower, weight, acceleration, model year, origin
* Target: MPG
* Removed: car name (non-useful feature)

## Pre processing
* Replaced missing values (?) with NaN
* Converted horsepower to numeric
* One-hot encoded origin
* Scaled features using StandardScaler
* Scaled target variable for neural network training

## model used (for now)
* TensorFlow Sequential Neural Network

## Neural Network Architecture
* Dense (32, ReLU)
* Dense (16, ReLU)
* Output layer (1 neuron) note: initialy used 64,32,1 but the realised that its a bit overkill for such small data set the adjusted accordingly
* Optimizer: Adam
* Loss: Mean Squared Error

## Evaluation Metrics
* Mean Absolute Error (MAE)
* R² Score (for comparison)

## Conclusion
The project demonstrates that proper preprocessing and scaling significantly improve model performance. While tree-based models like XGBoost are naturally suited for structured data, neural networks can still achieve strong results when carefully tuned.
