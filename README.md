# Restaurant Recommender System

This project demonstrates a restaurant recommendation system implemented using machine learning and neural networks. The system processes user preferences and recommends a restaurant using a trained neural network model. A GUI is provided for user interaction.

## Key Features

1. **Data Preprocessing**
   - Reads data from an Excel file containing user preferences.
   - Handles missing values and converts restaurant preferences into one-hot encoded vectors.
   - Prepares training data using a leave-one-out approach for each user.

2. **Neural Network Model**
   - A feed-forward neural network with the following architecture:
     - Input layer matching the number of restaurant classes.
     - Two hidden layers with 16 and 8 neurons, respectively, using ReLU activation.
     - Output layer with softmax activation for multi-class probability predictions.
   - Loss function: Sparse Categorical Crossentropy.
   - Optimizer: Adam.

3. **Model Training**
   - Trains the neural network using the prepared dataset.
   - Employs an 80-20 split for training and validation.

4. **Recommendation System**
   - Predicts a suitable restaurant for a user based on their selected preferences.

5. **Graphical User Interface (GUI)**
   - Built using `tkinter` for easy interaction.
   - Allows users to select up to four restaurants from a dropdown menu.
   - Displays a recommended restaurant based on the neural network's prediction.

## Dependencies

- `pandas`
- `numpy`
- `scikit-learn`
- `tensorflow`
- `tkinter`

Install the dependencies using:
```bash
pip install -r requirements.txt
```

## How to Run

1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```
2. Navigate to the project directory:
   ```bash
   cd <project_directory>
   ```
3. Install dependencies.
4. Run the notebook to train the model and save it.
5. Start the GUI application:
   ```bash
   python restaurant_recommender.py
   ```

## File Structure

- **Restaurant Recommender.ipynb**: Notebook with the full implementation of the system.
- **restaurant_recommender.py**: Script to launch the GUI application.
- **requirements.txt**: Lists required Python libraries.
- **model.h5**: Saved model file.

## Notes

- Ensure the input Excel file is correctly formatted with user preferences.
- The GUI application requires the trained model to make predictions.
