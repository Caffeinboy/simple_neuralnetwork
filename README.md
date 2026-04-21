# Iris Detection — Simple Neural Network

Jupyter Notebook project for classifying Iris flowers (Setosa, Versicolor, Virginica) using a simple feedforward neural network. The notebooks walk through data exploration, preprocessing, model building, training, evaluation, and prediction.

## Repository Overview
- Language: Jupyter Notebook (100%)
- Description: iris detection
- Purpose: Educational and reproducible pipeline for training a simple neural network on the Iris dataset.

## Notebooks (recommended order)
1. `01_Data_Exploration.ipynb` — Load and explore the Iris dataset, visualize feature distributions and correlations.  
2. `02_Data_Preprocessing.ipynb` — Clean, normalize/scale features, encode labels, and create train/test splits.  
3. `03_Model_Building.ipynb` — Define a simple feedforward neural network (Keras/TensorFlow or pure NumPy variants).  
4. `04_Model_Training.ipynb` — Train the model, save checkpoints, and plot training/validation curves.  
5. `05_Model_Evaluation.ipynb` — Evaluate the trained model on the test set, produce confusion matrix and classification report.  
6. `06_Predictions.ipynb` — Demonstrate making predictions on new samples and visualizing results.

## Quick Start (local)
1. Clone the repository:
```bash
git clone https://github.com/Caffeinboy/simple_neuralnetwork.git
cd simple_neuralnetwork
(Optional) Create and activate a virtual environment:
bash
python -m venv venv
# macOS / Linux
source venv/bin/activate
# Windows (PowerShell)
venv\Scripts\Activate.ps1
Install dependencies:
bash
pip install -r requirements.txt
# or minimal set:
# pip install jupyter numpy pandas scikit-learn matplotlib seaborn tensorflow
Launch Jupyter Notebook / Lab:
bash
jupyter notebook
# or
jupyter lab
Open and run the notebooks in the order listed above.

Dataset
This project uses the classic Iris dataset (150 samples, 4 features):

sepal length (cm)
sepal width (cm)
petal length (cm)
petal width (cm)
Notebooks load the dataset from scikit-learn by default, or from an included CSV if present. No external download is required unless you prefer to use a custom dataset.

Model
A simple feedforward neural network is used for classification. Typical example architecture:

Code
Input (4) → Dense(16, ReLU) → Dense(8, ReLU) → Dense(3, Softmax)
Training uses categorical cross-entropy and the Adam optimizer. Notebooks include both a Keras/TensorFlow implementation and notes for a pure NumPy educational variant.

Example scripts (if present)
02_data_preprocessing.py — prepares and saves scaled train/test arrays and label encoders.
03_model_building.py — builds and saves model architecture (JSON).
04_model_training.py — trains model, saves best_model.h5 and final_model.h5, and plots history.
05_model_evaluation.py — loads saved model and evaluates on the test set, prints classification report, and renders confusion matrix.
06_predictions.py — loads scaler + model and demonstrates prediction on a sample input.
Run the scripts in sequence (if present):

bash
python 02_data_preprocessing.py
python 03_model_building.py
python 04_model_training.py
python 05_model_evaluation.py
python 06_predictions.py
Evaluation
Notebooks and scripts generate:

Accuracy, precision, recall, F1-score
Confusion matrix visualizations
Training and validation loss/accuracy plots
Use scikit-learn's classification_report and confusion_matrix utilities for detailed metrics.

Tips & Notes
For reproducible results, set a random seed at the start of each notebook (NumPy, TensorFlow, and Python random).
Try different architectures, activations, batch sizes, and learning rates to see effects on performance.
Use K-fold cross-validation (scikit-learn) to evaluate model stability on small datasets.
If using TensorFlow/Keras, prefer a virtual environment and pin package versions in requirements.txt.
Dependencies (example)
Add exact versions to requirements.txt for reproducibility. Example minimal list:

Code
jupyter
numpy
pandas
scikit-learn
matplotlib
seaborn
tensorflow>=2.0    # optional if using Keras/TensorFlow
joblib             # for saving scalers/encoders
Reproducibility
Save model weights and architecture (.h5, .json) and preprocessing objects (scaler.joblib, label_binarizer.joblib) in the repo or a release.
Record random seeds and environment package versions (pip freeze > requirements.txt).
Troubleshooting
Out of Memory / GPU issues: Reduce batch size, lower model size, or run on CPU.
Slow training: Use smaller models, reduce epochs, or enable GPU.
Low accuracy: Verify preprocessing, check label encoding, increase training data or try transfer learning.
Contributing
Contributions, issues and feature requests are welcome. Please:

Fork the repository
Create a feature branch (git checkout -b feature/my-change)
Commit your changes (git commit -m "feat: add ..."), and push (git push origin feature/my-change)
Open a Pull Request
License
This project is provided under the MIT License — see the LICENSE file for details.

Contact
If you have questions or want to collaborate, open an issue or submit a PR. You can also reach me via my GitHub profile: https://github.com/Caffeinboy.
