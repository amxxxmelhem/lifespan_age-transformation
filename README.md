
# Lifespan Age Transformation Prediction

This project focuses on **facial age transformation**—generating images of a person's face at different ages using deep learning techniques. It is based on the repository [Lifespan_Age_Transformation_Synthesis](https://github.com/royorel/Lifespan_Age_Transformation_Synthesis), and utilizes a GAN-based architecture for age progression and regression across a human lifespan.

---

## 🔍 Project Description

The goal of this project is to synthesize realistic face images showing the same person at different age stages. This can be used for:

- Visualizing aging effects on faces
- Forensic investigations
- Entertainment and media
- Data augmentation for facial recognition

The model operates by **traversing a latent space** that represents different age groups, and generates interpolated images along the age progression path.

---

## 📁 Project Structure

```
Lifespan_Age_Transformation_Synthesis/
│
├── data/                 # Dataset loading and preprocessing
├── models/               # Model definitions (e.g., GAN architecture)
├── options/              # Test and train options
├── checkpoints/          # Pretrained models (downloaded)
├── results/              # Output images
├── util/                 # Utility functions for visualization, etc.
├── download_models.py    # Script to download pretrained models
├── test.py               # Script for inference/testing
└── requirements.txt      # List of dependencies
```

---

## 🧪 Setup and Usage

### 1. Clone the repository

```bash
git clone https://github.com/royorel/Lifespan_Age_Transformation_Synthesis
cd Lifespan_Age_Transformation_Synthesis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
pip install Pillow==9.4.0  # Required for compatibility with ANTIALIAS
```

### 3. Download pre-trained models

```bash
python download_models.py
```

### 4. Run age transformation

```bash
python test.py --dataroot /path/to/images --name lifespan_synthesis --model lifespan
```

Use flags like `--traverse` to interpolate across age groups, and `--in_the_wild` for real-world images.

---

## 🖼️ Example Results

Given an input image:

![Input Face](results/input_example.jpg)

The model produces:

- Aged versions (older and younger)
- Smooth transitions between age groups

---

## ⚙️ Model Options

| Option           | Description                                    |
|------------------|------------------------------------------------|
| `--traverse`     | Interpolate across latent space (ages)         |
| `--interp_step`  | Controls granularity of interpolation          |
| `--in_the_wild`  | Enables preprocessing for unaligned images     |

---

## 📚 Acknowledgements

This project builds on the official repository:
- [Lifespan Age Transformation Synthesis (GitHub)](https://github.com/royorel/Lifespan_Age_Transformation_Synthesis)
- Authors: Roy Or-El, et al.

---

## 📜 License

This project is distributed under the MIT License. Please refer to the original repository's license for more details.
