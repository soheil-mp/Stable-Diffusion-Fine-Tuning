# Fine-Tuning Stable Diffusion on Gaming Assets

<br>

## Introduction

Welcome to our repository dedicated to fine-tuning Stable Diffusion, an open-source neural network for generating high-quality images. This project aims to enhance the capabilities of Stable Diffusion by fine-tuning it with gaming asset datasets.

Stable Diffusion is a deep learning, text-to-image model released in 2022 based on diffusion techniques. It is primarily used to generate detailed images conditioned on text descriptions, though it can also be applied to other tasks such as inpainting, outpainting, and generating image-to-image translations guided by a text prompt (Wikipedia contributors, 2024). 

<br>

## Getting Started

### Prerequisites

- Python 3.9+
- Installing the dependencies listed in `requirements.txt`.
```
pip install -r requirements.txt
```





<br>

## Data Preparation

To prepare your data for fine-tuning the Stable Diffusion model, follow these steps:

### Step 1: Organize Your Image Dataset

Place the images you wish to use for fine-tuning inside the `./data/images/` folder. Ensure that your dataset consists of high-quality images relevant to the gaming domain or any other style you're targeting.

### Step 2: Write Prompt for Images 

#### Single Prompt (for Dreambooth)

In Dreambooth, using a single, well-defined prompt is crucial as opposed to multiple prompts for each image. This approach ensures consistency and focus, allowing the model to deeply understand and adhere to the specific theme and style you're aiming for. A single, detailed prompt effectively guides the model's generative process, leading to more coherent and stylistically consistent outputs. The preciseness of this singular prompt is instrumental in achieving high-quality, relevant results that accurately reflect your project's vision.

#### Multiple Prompt Generation using BLIP (for Keras-CV)
For implementing stable diffusion with Keras-CV, a critical component is the creation of accurate and relevant prompts for each image in the dataset. To automate this process, the BLIP (Berkeley Language Image Program) model is employed for automatic captioning. Utilize the script located in `./auto_captioning/auto_captioning.ipynb` to generate captions. Follow the step-by-step guide in the notebook to efficiently create descriptive captions for each image in your dataset. It's important to ensure that these captions accurately reflect the content of the images. To guarantee precision and contextual relevance, manually review and, if necessary, revise the captions. This process ensures that each image is paired with a single, descriptive prompt, optimizing the stable diffusion process in Keras-CV.

<br>

## Fine-Tuning Process

To do.

<br>

## Evaluation

To do.

