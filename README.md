# Assigment - DAT305

## Useful commands

Evaluate CNN:

```bash
tensorboard --logdir .\logs\
```

## Running the notebooks

### 1. Install UV

```bash
# On macOS and Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# On Windows
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

# Or using pip
pip install uv
```

### 2. Create venv

```bash
#creates venv and downloads all packages from pyproject.toml
uv sync
```

### 3. Use the virtual enviroment for the jupyter notebooks

source .venv/bin/activate  # On Windows: .venv\Scripts\activate

## Task 5: Tumor Segmentation

Goal: Students will build and evaluate a tumor segmentation model (brain tumor) using a
simple dataset. Predict both tumor segmentation mask and tumor type (benign vs
malignant) from the same model. We want students to add uncertainty estimation
(uncertainty quantification + Calibration plots).

The project begins with data preparation, where an MRI dataset is downloaded and
preprocessed by resizing the images to a consistent resolution, normalizing pixel
intensities, and splitting the data into training and testing sets. In Step 2: Baseline Model,
we experiment with at least two different models for tumor classification to establish
baseline performance. Next, in Step 3: Model Training, we focus on training a
segmentation model using the labeled tumor masks, optimizing it with Dice loss and
evaluating performance through Intersection over Union (IoU) metrics. For Step 4:
Evaluation, the predicted tumor masks are compared against the ground-truth annotations,
and quantitative results are reported using the Dice coefficient and IoU scores. Finally, in
Step 5: Extensions (Optional), we explore improvements such as applying data
augmentation techniques like flipping, rotating, and adjusting contrast to increase model
robustness, as well as incorporating uncertainty estimation approaches such as Monte Carlo
Dropout or Deep Ensembles to enhance the reliability of the predictions.
Datasets: Brain MRI Images for Brain Tumor Detection

## Instructions

1. Data Preprocessing:
   * Read data from the given source
   * Apply pre-processing techniques if needed
   * Split dataset into train, validation and test set
2. Exploratory Analysis
   * To begin this exploratory analysis, first use matplotlib to import libraries and define
   functions for plotting the data. Depending on the data, not all plots will be made.
3. Feature Extraction
   * Explore possible feature extraction for your data
4. Model selection
   * You can explore traditional machine learning models, deep learning models, or transformer models
5. Evaluation Metrics
   * Confusion matrix
   * Precision, Recall, and F1-score for a more detailed analysis of the model performance
6. Model Training
   * Train the model on the training split and validate on the development test split.

## General Information

A compulsory programming assignment (*Approved/Not approved*), which must be passed to qualify for the written exam. The assignment will be assessed based on both a report and an oral presentation.
The project can be done individually as well as in groups. Project topics will be announced later.

### Programming Assignment Grading Policy

* 25% Data preprocessing steps and visualizations
* 50% Model selection and implementation
* 10% Model comparison
* 15% Oral presentation + report
* To pass the project, you need to collect at least 70%
