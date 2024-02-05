# Fine-Tuning Stable Diffusion on Gaming Characters

<br>

## Introduction

Welcome to this repository which is dedicated to fine-tuning Stable Diffusion, an open-source neural network for generating high-quality images. This project aims to enhance the capabilities of Stable Diffusion by fine-tuning it with gaming asset datasets.

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

Place all the images you wish to use for fine-tuning inside the `./data/images/` folder. 

### Step 2: Write Prompt for Images 

- Single Prompt (for Dreambooth): <br> In Dreambooth, only a single well-defined prompt is used for fine-tuning all the images. 
- Multiple Prompt (for Keras-CV): <br> To implement stable diffusion with Keras-CV, we require a separate prompt for each image in our dataset. Utilize the BLIP model to automatically generate descriptive captions for each image in the dataset (using the `./preparation/auto prompting using BLIP.ipynb` script). 



<br>

## Fine-Tuning Process

### Using Dreambooth

In this approach, the Stable Diffusion model got fine-tuned using Dreambooth. It involves setting up the model from huggingface and fine-tuning it with given gaming characters. The fine-tuned model then is used to generate new artwork related to gaming characters.



### Using Keras-CV

In this appraoch, the Stable Diffusion model got fine-tuned using TensorFlow's Keras framework. A custom class is used for handling the training processes (including loss calculation and gradient updates) which updates part of the weight of the the diffusion model.






<br>

## Evaluation

The fine-tuned stable diffusion model has generated a set of character images for evaluation. The images confirm the model's ability to:
- [x] Presence of Requested Object: Each image clearly displays the intended fantasy characters.
- [x] Variation in Design: There's evident variation among characters, with differences in shapes and colors showcased.
- [x] Background Simplicity: Characters are set against solid, non-complex backgrounds for clarity.
- [x] Separation from Background: The subjects are well-differentiated from the backdrop, ensuring easy discernibility.

### Character Variation

<table align="center">
  <tr>
    <td><img src="https://raw.githubusercontent.com/SoheilMohammadpour231754/Stable-Diffusion/main/generated%20artworks/dreambooth/a%20demon%20dressed%20in%20red%20and%20holding%20a%20sword.png" alt="Demon with sword" width="200"></td>
    <td><img src="https://raw.githubusercontent.com/SoheilMohammadpour231754/Stable-Diffusion/main/generated%20artworks/dreambooth/Elfs%20with%20arrows.png" alt="Elfs with arrows" width="200"></td>
    <td><img src="https://raw.githubusercontent.com/SoheilMohammadpour231754/Stable-Diffusion/main/generated%20artworks/dreambooth/Gandalf%20the%20gray.png" alt="Gandalf the gray" width="200"></td>
  </tr>
  <tr>
    <td align="center">A demon</td>
    <td align="center">Two Elfs</td>
    <td align="center">A wizard</td>
  </tr>
</table>

### Colour Variation of Same Characters

<table align="center">
  <tr>
    <td><img src="https://raw.githubusercontent.com/SoheilMohammadpour231754/Stable-Diffusion/main/generated%20artworks/dreambooth/Knights%20in%20blue%2C%20black%20and%20white%20with%20an%20elaborate%20helmet%20on%20their%20head.png"  width="200"></td>
    <td><img src="https://raw.githubusercontent.com/SoheilMohammadpour231754/Stable-Diffusion/main/generated%20artworks/dreambooth/Knights%20in%20red%2C%20black%20and%20white%20with%20an%20elaborate%20helmet%20on%20their%20head.png" width="200"></td>
    <td><img src="https://raw.githubusercontent.com/SoheilMohammadpour231754/Stable-Diffusion/main/generated%20artworks/dreambooth/Knights%20in%20green%2C%20black%20and%20white%20with%20an%20elaborate%20helmet%20on%20their%20head.png" width="200"></td>
  </tr>
  <tr>
    <td align="center">Blue Knights</td>
    <td align="center">Red Knights</td>
    <td align="center">Green Knights</td>
  </tr>
</table>

<br>

