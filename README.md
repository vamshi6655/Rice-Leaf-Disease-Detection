# 🌾 Rice Leaf Disease Detection Using Deep Learning

A Jupyter Notebook project for exploring rice-leaf images and training image-classification models to distinguish the disease classes in the supplied dataset.

## Project overview
The notebook includes:
- Dataset extraction and image inventory
- Exploratory data analysis and sample-image visualization
- Train/validation/test split
- Image resizing and training-only data augmentation
- A custom Convolutional Neural Network (CNN)
- MobileNetV2 transfer learning
- Accuracy, macro precision, macro recall, macro F1-score, classification reports, and confusion matrices
- Prediction helper for a new leaf image
- Model saving and a challenges/conclusion report template

## Dataset
The supplied archive is included at `data/PRCP-1001-RiceLeaf.zip`.

The project brief lists three classes: **Leaf smut**, **Brown spot**, and **Bacterial leaf blight**. The notebook discovers class-folder names from the extracted archive, so verify the detected names and counts before training. The PDF brief mentions 120 images, but the actual archive should be checked by running the notebook.

> Note: The brief also mentions “leaf blast” in one task sentence while the listed dataset classes include “Leaf smut.” This project follows the class names actually present in the dataset folders.

## Requirements
- Python 3.10 or newer recommended
- Jupyter Notebook or JupyterLab
- TensorFlow, NumPy, Pandas, Matplotlib, Seaborn, scikit-learn, Pillow

Install dependencies:
```bash
pip install -r requirements.txt
```

## Run locally
1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/Rice-Leaf-Disease-Detection.git
   cd Rice-Leaf-Disease-Detection
   ```
2. Install packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
4. Open `notebooks/Rice_Leaf_Disease_Detection.ipynb`.
5. In the notebook’s dataset path cell, set `ZIP_PATH` to the local path of `data/PRCP-1001-RiceLeaf.zip`. For example:
   ```python
   ZIP_PATH = r"data/PRCP-1001-RiceLeaf.zip"
   ```
6. Run the notebook cells in order.

## Repository structure
```text
Rice-Leaf-Disease-Detection/
├── data/
│   └── PRCP-1001-RiceLeaf.zip
├── notebooks/
│   └── Rice_Leaf_Disease_Detection.ipynb
├── models/                 # Saved model files go here after training
├── reports/                # Add exported reports/results here
├── src/                    # Optional reusable code
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Evaluation
The notebook calculates:
- Accuracy
- Macro precision
- Macro recall
- Macro F1-score
- Confusion matrix and per-class classification report

Do not claim a model accuracy until the notebook has been run and the test results have been recorded. The dataset is small, so test metrics may vary with the split and may not represent performance on field images.

## Challenges and considerations
- Small dataset: use augmentation and early stopping, and gather more independent images for stronger evaluation.
- Image variation: lighting, backgrounds, leaf angles, and camera differences may affect predictions.
- Class-name ambiguity: inspect the actual folder names and sample images before training.
- Production readiness: validate the selected model on diverse real-world field images and consult agricultural experts before relying on predictions for treatment decisions.

## Future improvements
- Add more verified images from different farms and conditions.
- Evaluate additional pretrained architectures.
- Add a simple Streamlit interface for image upload and prediction.
- Test deployment on mobile or edge devices.

## Disclaimer
Educational prototype only. This model is not a substitute for professional agricultural diagnosis.

## Project tags
`python` `deep-learning` `cnn` `mobilenetv2` `tensorflow` `image-classification` `agriculture` `jupyter-notebook`
