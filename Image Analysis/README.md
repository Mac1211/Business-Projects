# Chest Condition Analysis
The provided Python code focuses on building and training a deep learning model for classifying chest X-ray images into four categories: 'Covid-19', 'Healthy', 'Viral Pneumonia', and 'Bacterial Pneumonia'. The code leverages transfer learning by utilizing a pre-trained ResNet50 model and adding custom layers for classification.
## Key Steps and Explanation:
### Import Libraries
The code starts by importing necessary libraries for image processing, deep learning, and data visualization.
### Load and Process Data:
1) The chest X-ray images are loaded from a directory using ImageDataGenerator, which also handles image rescaling and splitting the data into training and validation sets.
2) The shape of the image batches and labels is printed to verify the data format.
3) A label translator dictionary is defined to map numerical labels to their corresponding class names.
4) The training images are visualized along with their labels.
### Transfer Learning with RestNet50:
1) The pre-trained ResNet50 model is loaded with 'imagenet' weights, excluding the top classification layers (include_top=False). The input shape is set to (256, 256, 3).
2) The model summary is printed to understand its architecture.
3) The last 10 layers of the base model are unfrozen for fine-tuning, while the rest are frozen to retain pre-trained features.
### Build and Train Model:
1) Custom classification layers are added on top of the ResNet50 base model, including average pooling, flattening, dense layers with ReLU activation, dropout for regularization, and a final dense layer with softmax activation for multi-class classification.
2) The model is compiled with categorical cross-entropy loss, RMSprop optimizer, and accuracy metric.
3) Early stopping and model checkpoint callbacks are used to prevent overfitting and save the best model during training.
4) The model is trained on the training data and validated on the validation data for 30 epochs.
### Evaluate the Model:
1) The training and validation accuracy/loss curves are plotted to visualize the model's performance over epochs.
2) The model is evaluated on a separate test dataset using model.evaluate, and the accuracy is printed.
3) Predictions are made on the test images, and a classification report is generated to show precision, recall, and F1-score for each class.
4) A confusion matrix is plotted to visualize the model's predictions and understand misclassifications.
5) The test images are visualized along with their original and predicted labels.

#### Overall, this code demonstrates how to use transfer learning with a pre-trained ResNet50 model for chest X-ray image classification. It provides a good starting point for building medical image classification models, and you can further experiment with different hyperparameters, architectures, and data augmentation techniques to improve performance.

The performance of the model might vary depending on the size and quality of the dataset. We can try collecting more data or using data augmentation to improve the results. We can explore other pre-trained models or fine-tune more layers to see if it leads to better performance. Consider using techniques like class weighting or focal loss if the dataset is imbalanced.
