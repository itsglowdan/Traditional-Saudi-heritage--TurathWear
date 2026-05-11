# TurathWear

TurathWear is an AI fashion project that brings traditional Saudi heritage patterns into modern clothing designs using generative AI.

The idea started from a simple question:

How can we preserve Saudi cultural identity in a modern and interactive way instead of keeping heritage limited to traditional textiles and museums?

TurathWear answers this by allowing users to upload a plain T-shirt image, choose a Saudi heritage pattern, and automatically generate a new fashion design while preserving the original structure of the garment.

---

## Project Goal

The goal of TurathWear is not only to generate visually appealing outputs, but also to preserve the authenticity of traditional Saudi patterns while integrating them into contemporary fashion using AI.

The project focuses on:

- preserving cultural identity
- maintaining realistic garment structure
- generating clean and wearable outputs
- exploring AI applications in fashion and heritage preservation

---

## How It Works

The workflow is designed to be simple and interactive.

1. The user uploads a plain T-shirt image.
2. A heritage pattern is selected from one of the Saudi regional categories.
3. The trained AI model applies the selected pattern onto the T-shirt.
4. The final generated design is displayed and can be downloaded directly.

The system preserves the shirt shape, proportions, and overall appearance while transferring the selected heritage style.

---

## Heritage Categories

<p align="center">
  <img src="images/heritage1.png" width="250"/>
  <img src="images/heritage2.png" width="250"/>
  <img src="images/heritage3.png" width="250"/>
</p>

The dataset includes traditional patterns inspired by multiple Saudi heritage regions:

- Najdi
- Sadu
- Hijazi
- Asiri
- Eastern Region patterns

---

## Dataset

<p align="center">
  <img src="images/dataset1.png" width="250"/>
  <img src="images/dataset2.png" width="250"/>
  <img src="images/dataset3.png" width="250"/>
</p>

A custom dataset was built specifically for this project through an iterative image-processing pipeline.

Dataset statistics:

- 1,083 unique heritage patterns
- 2,166 original paired images
- 19,494 generated training samples after augmentation

The dataset was created using multiple processing stages including:

- SVG processing
- pattern tiling
- compositing pipelines
- background cleanup
- color augmentation

---

## Model

Several approaches were explored during development, including:

- Pix2Pix Conditional GAN
- Improved Pix2Pix Pipeline
- InstructPix2Pix with LoRA Fine-Tuning

After experimentation, Pix2Pix achieved the strongest overall results in terms of:

- pattern fidelity
- garment preservation
- structural consistency
- inference speed

### Selected Model Results

| Metric | Result |
|---|---|
| SSIM | 0.9454 |
| PSNR | 28.13 dB |
| Mean L1 Error | 0.0101 |

---

## Training Curves

<p align="center">
  <img src="images/training_curves.png" width="700"/>
</p>

The selected Pix2Pix model showed stable adversarial training and strong validation performance throughout training.

---

## Generated Results

<p align="center">
  <img src="images/results.png" width="900"/>
</p>

Examples of generated outputs showing different Saudi heritage patterns applied to modern T-shirt designs.

---

## Technologies Used

- Python
- PyTorch
- Pix2Pix GAN
- OpenCV
- PIL
- Gradio
- Hugging Face Spaces

---

## Live Demo

https://huggingface.co/spaces/layaniff/TurathWear

---

## Team

Developed by students from Princess Nourah bint Abdulrahman University.

- Dana Alsubaie
- Shmokh Aljomah
- Layan Alfares
- Maha Alhudaybi

---

## Note

The source code is currently private due to ongoing research and development considerations.

