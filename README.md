<div align="center">

# 🐄 Cattle Body-Part Detection

**Custom CNN · Bounding-box localization · Computer vision**

![Python](https://img.shields.io/badge/Python-Computer%20Vision-3776AB?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-FF6F00?logo=tensorflow&logoColor=white)
![Status](https://img.shields.io/badge/status-academic%20experiment-64748B)

</div>

## Project overview

An academic computer-vision experiment to localize selected cattle body parts—**head, legs, and back**—from annotated images. The project explores a custom convolutional neural network, annotation preprocessing, bounding-box regression, and part classification.

The focus is **detection/localization research**, not a deployed veterinary or precision-agriculture service.

## Pipeline

1. **Dataset preparation:** Read cattle images and LabelMe-style bounding-box annotations.
2. **Target construction:** Normalize annotated regions into a fixed-slot format (one head, four legs, one back).
3. **Augmentation:** Apply brightness, contrast, saturation and horizontal-flip transformations, adjusting bounding boxes where needed.
4. **Model:** Train a custom CNN backbone with convolution/normalization blocks and separate box-regression and class-prediction outputs.
5. **Evaluation:** Inspect predicted boxes, localization overlap, class predictions and visualized examples.

## Technology

**Python · TensorFlow/Keras · NumPy · OpenCV/image processing · Jupyter Notebook**

## Repository map

```text
cattle_detection_training.ipynb   # Training and evaluation workflow
detection_utils.py               # Image/annotation processing utilities
annotations/                     # Annotation files
images/                          # Image data
outputs/results/                 # Saved analysis outputs
```

## Reproducing the experiment

Open `cattle_detection_training.ipynb` in Jupyter or Google Colab and review the notebook's import/dependency cells, dataset paths, preprocessing, training and evaluation sections before running. Environment setup, path configuration and dataset permissions may require adjustment. No clean end-to-end rerun is certified by this README.

## Evaluation notes

The repository demonstrates an implemented object-localization workflow. However, saved localization performance and metric methodology require further review; **do not interpret this as a production-grade body-part detector or claim independently verified accuracy**.

## Responsible data use

Verify that any included images and annotations may be redistributed, particularly if they came from external datasets or academic collaborators. Preserve attribution for the original group project.
