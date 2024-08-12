# Movie Recommendation System Using SAE and RBM

## Project Overview
This project implements two types of neural network models to predict user ratings for movies based on the [MovieLens datasets](https://grouplens.org/datasets/movielens/). The datasets include ratings of movies by various users, which are used to train and test the models.

## Datasets
- **MovieLens 1M Dataset**: This dataset contains 1 million ratings of approximately 3,900 movies by 6,000 users.
- **MovieLens 100k Dataset**: This dataset contains 100,000 ratings of 1,700 movies by 1,000 users.

## Models Implemented

### 1. Stacked Autoencoder (SAE)
- **Architecture**: The SAE model is built with four fully connected layers.
- **Activation Function**: Sigmoid.
- **Loss Function**: Mean Squared Error Loss (MSELoss).
- **Optimizer**: RMSProp.
- **Training**: The model is trained to minimize the reconstruction error over 100 epochs.
- **Testing**: The model's performance is evaluated on a test set, calculating the root mean squared error.

### 2. Restricted Boltzmann Machine (RBM)
- **Architecture**: The RBM is defined with a visible layer (corresponding to movies) and a hidden layer (corresponding to features).
- **Training**: The RBM is trained using Contrastive Divergence over 10 epochs. The input is divided into mini-batches, and for each mini-batch, the model updates its weights.
- **Testing**: The model's performance is evaluated by comparing the predicted ratings with the actual ratings on the test set.

## How to Run the Code
1. **Prerequisites**: Ensure you have Python installed with the required packages (`pandas`, `numpy`, `torch`).
2. **Data Preparation**: Download the MovieLens datasets and place them in the appropriate directories.
3. **Run the Script**: Execute the script in a Python environment. The training and testing of both models will be performed sequentially, and the losses will be printed to the console.

## Results
The models will output the training and test losses after running. These losses indicate the performance of the models in predicting user ratings for movies.

## Future Work
- Implementing and experimenting with other neural network architectures.
- Hyperparameter tuning to improve model accuracy.
- Incorporating more sophisticated data preprocessing techniques to enhance model performance.

## Conclusion
This project demonstrates the application of deep learning techniques in recommendation systems. The SAE and RBM models show different approaches to predicting movie ratings, offering a solid foundation for further exploration in the field of recommendation systems.

## Files in the Repository
- **`sae_rbm_recommender.py`**: Contains the full implementation of the SAE and RBM models.
- **`README.md`**: This file, which provides an overview of the project, instructions for running the code, and a summary of the results.
