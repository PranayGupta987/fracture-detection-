# Bone Fracture Detection

A notebook-based computer vision project exploring deep learning approaches for detecting and classifying bone fractures in X-ray images. The repository includes experiments with a custom CNN, ResNet, and YOLO, along with plots used to compare model performance.

> **Research and educational use only.** This project is not a medical device and has not been validated for clinical use. Its predictions must not be used to diagnose or treat patients.

## Project contents

```text
.
├── graphs/
│   ├── comparison.png
│   ├── confusion_matrices.png
│   └── epochs_vs_accuracy.png
├── models/
│   ├── cnn_model.ipynb
│   ├── resnet_model.ipynb
│   └── yolo_model.ipynb
└── requirements.txt
```

- **CNN notebook** — experiments with a convolutional neural network.
- **ResNet notebook** — experiments with a ResNet-based classifier.
- **YOLO notebook** — object detection using images and YOLO-format labels.
- **Graphs** — saved model comparison, confusion matrix, and training accuracy figures.

The notebooks are independent experiments. There is no packaged application or command-line inference tool in this repository.

## Requirements

- Python 3.10 or later is recommended.
- The packages listed in `requirements.txt` (PyTorch, TensorFlow/Keras, OpenCV, NumPy, pandas, scikit-learn, Matplotlib, Seaborn, Pillow, and IPython).
- A dataset prepared for the notebook you want to run. The dataset is not included in this repository.
- A GPU is optional, but can make model training faster. Configure a compatible PyTorch/TensorFlow environment for your hardware if needed.

## Setup

Clone the repository and create a virtual environment:

```bash
git clone https://github.com/PranayGupta987/fracture-detection-.git
cd fracture-detection-
python -m venv .venv
```

Activate it:

**Windows PowerShell**
```powershell
.venv\Scripts\Activate.ps1
```

**macOS / Linux**
```bash
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

To open the notebooks locally:

```bash
jupyter notebook
```

You can also open the notebooks in Google Colab. Before running either way, update the dataset paths in the notebook cells to point to your own data. Some cells contain paths from the original Colab/Google Drive environment, which will not work on another machine without changes.

## Dataset notes

The dataset is not distributed with this repository. Obtain a dataset you are permitted to use, and follow its license, attribution, and privacy requirements.

The YOLO notebook expects a dataset in YOLO-style directories with images, corresponding text label files, and a dataset configuration file. Update the notebook's image, label, and configuration paths to match your local dataset. The CNN and ResNet notebooks also define data paths in their cells; check and update those before execution.

Dataset organization, class names, and preprocessing should remain consistent between training and evaluation. Do not use patient-identifiable or otherwise sensitive data unless you have the required authorization and safeguards.

## Running an experiment

1. Choose a notebook under `models/`.
2. Update its dataset paths and any dataset-specific settings.
3. Run the notebook cells in order.
4. Review the generated metrics and plots, and compare them with the figures in `graphs/` where applicable.

Notebook outputs and reported metrics depend on the dataset, preprocessing, train/validation split, and runtime. Treat the checked-in plots as experiment artifacts rather than a guarantee of performance on other data.

## Results

The repository includes these visual summaries:

- [Model comparison](graphs/comparison.png)
- [Confusion matrices](graphs/confusion_matrices.png)
- [Epochs versus accuracy](graphs/epochs_vs_accuracy.png)

For meaningful comparisons, evaluate models on the same held-out data and report class-wise metrics in addition to overall accuracy, especially when classes are imbalanced.

## Limitations

- The repository does not contain the training dataset or a ready-to-use trained model.
- Notebook data paths may need editing before the notebooks will run.
- The notebooks are research experiments, not a maintained production pipeline.
- Performance on one dataset does not establish clinical accuracy, safety, or generalization to other scanners, populations, or fracture types.

## Contributing

Contributions such as clearer notebook setup, reproducibility improvements, and documentation are welcome. Please open an issue to discuss larger changes before submitting a pull request.

## License

No license file is currently included. Until a license is added, the repository's reuse and redistribution terms are not explicitly specified. Please contact the repository owner if you need permission to reuse the code.
