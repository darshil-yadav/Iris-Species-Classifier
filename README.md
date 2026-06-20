🌸 Iris Species Classifier
A machine learning project that uses a K-Nearest Neighbors (KNN) algorithm to predict the species of an Iris flower based on its physical measurements.

This repository contains the model development process, data exploration, and the serialized prediction model ready for deployment.

🎯 Project Overview
The goal of this project is to accurately classify Iris flowers into one of three species (Setosa, Versicolor, or Virginica) using sepal and petal dimensions (length and width).

The model was trained using the classic Iris dataset and achieves a 98% prediction accuracy.

💻 Tech Stack
Language: Python

Libraries: Scikit-Learn, Pandas, NumPy, Matplotlib, Seaborn

Environment: Jupyter Notebook

Serialization: Pickle

📂 Repository Structure
flowers.ipynb: The core Jupyter Notebook containing the data loading, exploration, model training (KNeighborsClassifier), evaluation, and testing.

flower_model.pkl: The exported, pre-trained KNN model saved via Pickle. This allows the model to make predictions in other applications without needing to be retrained.

🚀 How to Use
To run this project locally on your machine:

1. Clone the repository:
git clone https://github.com/darshil-yadav/Iris-Species-Classifier.git
cd Iris-Species-Classifier

2. Load the pre-trained model in your own Python script:
import pickle

# Load the saved model
with open('flower_model.pkl', 'rb') as f:
    model = pickle.load(f)

# Make a new prediction (Sepal Length, Sepal Width, Petal Length, Petal Width)
new_flower = [[5.1, 3.5, 1.4, 0.2]]
prediction = model.predict(new_flower)

print(prediction) 
# Output: [0] (Corresponds to 'setosa')
🔮 Future Updates
Streamlit Web Application: The next major phase of this project is to build an interactive frontend using Streamlit. This will allow users to input sepal and petal measurements via a clean webpage GUI and get real-time species predictions without touching any code.

Data Scaling Integration: Implementing StandardScaler to optimize the distance calculations for the KNN algorithm.
