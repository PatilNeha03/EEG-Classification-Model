# EEG Classification Model

This project aims to classify EEG (electroencephalogram) data into various brain activity categories, including seizure and non-seizure activities, using advanced machine learning models.

## Project Objective

The primary objectives of this project are:
- To classify EEG signals into seizure and non-seizure categories (Binary Classification).
- To categorize EEG signals into five distinct classes (Multi-Class Classification):
  1. Eye-open
  2. Eye-closed
  3. Hippocampal region
  4. Epileptogenic region
  5. Seizure

## Table of Contents

- [Project Objective](#project-objective)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Feature Extraction](#feature-extraction)
- [Classification Models](#classification-models)
- [Evaluation and Results](#evaluation-and-results)
- [Setup and Execution](#setup-and-execution)
- [Technologies Used](#technologies-used)
- [Contributions](#contributions)
- [License](#license)

## Dataset

The Bonn EEG dataset is used for this project. The data comprises single-channel EEG recordings with 4097 features per record. Each EEG recording is classified into five distinct categories as mentioned above.

## Data Preprocessing

- **Metadata Creation:** Efficiently created metadata to manage EEG files.
- **Label Encoding & Decoding:**
  - Label Encoder converts categorical labels into numerical indices for model compatibility.
  - Label Decoder facilitates interpretability by converting predictions back to original categorical labels.

## Feature Extraction

The project utilizes **Recurrence Quantification Analysis (RQA)** to:
- Extract recurrence and determinism features from the EEG signals.
- Analyze temporal data, providing insights into repetitive and predictable patterns.
- Generate a comprehensive feature set essential for effective classification.

## Classification Models

Two primary classification tasks are performed:

### Binary Classification
- Task: Classify EEG signals as seizure or non-seizure.
- Approach: Simplified binary labels for seizure (0) and non-seizure (1).

### Multi-Class Classification
- Task: Classify EEG signals into five activity types.
- Models Evaluated:
  - Logistic Regression
  - Random Forest
  - Decision Tree
  - XGBoost (Top performer)
- Cross-validation: 10-fold cross-validation applied to select the optimal model.

## Evaluation and Results

### Binary Classification
- High robustness and clear differentiation between seizure and non-seizure categories.
- Low false positives and negatives indicated by confusion matrix.

### Multi-Class Classification
- **Top Model:** XGBoost with an F1 Score of approximately 74%.
- Class-wise performance highlights challenges, notably in capturing Classes 1 to 4 effectively.
- Overall accuracy: 26%, indicating a need for further model refinement.

## Setup and Execution

### Running the Project
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Execute provided scripts or notebooks for preprocessing, feature extraction, model training, and evaluation.

## Technologies Used
- Python
- NumPy
- Pandas
- scikit-learn
- XGBoost
- Matplotlib (for visualizations)

