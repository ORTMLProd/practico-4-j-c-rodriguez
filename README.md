# Práctico 4

This project demonstrates the process of feature engineering and data preprocessing for training a deep learning model on the CIFAR-10 dataset. The workflow includes data preprocessing steps such as resizing and normalization, implementing a transform pattern, building and training a convolutional neural network (CNN) model, tracking experiments using Weights & Biases (wandb), and hyperparameter tuning.

## Feature Engineering/Data Preprocessing

Feature engineering and data preprocessing are crucial steps in preparing data for machine learning models. In this project, we perform the following steps:

### Preprocessing (Resizing, Normalization, etc.)

- **Resizing**: Adjusting the images to a consistent size to ensure uniformity in input dimensions.
- **Normalization**: Scaling pixel values to a standard range, typically [0, 1], to help the model converge faster during training.

These preprocessing steps help in transforming raw data into a format suitable for modeling, enhancing the model's performance and training efficiency.

### Transform Pattern

The transform pattern involves creating a preprocessing pipeline that standardizes the input data before it is fed into the model. This ensures that the data is in the right format and scale, making the training process more efficient.

## Modeling

In this project, we build a Convolutional Neural Network (CNN) using TensorFlow and Keras. The model is designed to classify images from the CIFAR-10 dataset, which consists of 60,000 32x32 color images in 10 different classes.

The modeling process includes:

- **Defining the Model Architecture**: Building a CNN with multiple layers including convolutional layers, batch normalization, max pooling, dropout, and dense layers.
- **Compiling the Model**: Setting the optimizer, loss function, and metrics for the model.
- **Training the Model**: Fitting the model on the training data and validating it on the test data.

### Experiment Tracking with wandb

Experiment tracking is essential for keeping records of different model runs, including their configurations, hyperparameters, and results. We use Weights & Biases (wandb) to track our experiments. This allows us to monitor the training process, compare different runs, and analyze the performance of the model over time.

### Wandb Alerts

Wandb provides alerts to monitor training progress and notify you of any significant events, such as achieving a new best accuracy or encountering a drop in performance. Alerts help in keeping track of the training process and quickly responding to issues.

## Hyperparameter Tuning

Hyperparameter tuning involves finding the best set of hyperparameters for the model. This can include tuning the learning rate, batch size, number of epochs, and architecture-specific parameters like the number of filters in convolutional layers. We use tools like wandb sweeps for systematic hyperparameter optimization.

---

This README provides an overview of the key components of the project. If you need further customization or additional sections, please let me know!
