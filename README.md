
# GAN-Based Medical Image Generation

This project explores the use of **Generative Adversarial Networks (GANs)**—a powerful class of deep learning models—to generate realistic synthetic medical images. The implementation is based on the **DCGAN (Deep Convolutional GAN)** architecture, with inspiration drawn from **StyleGAN** to improve visual quality and diversity.

## What is a GAN?

A **Generative Adversarial Network (GAN)** is a machine learning framework comprising two neural networks:

- **Generator**: Produces synthetic data (e.g., images) from random noise.
- **Discriminator**: Attempts to distinguish between real data and generated (fake) data.

These two models are trained simultaneously in a game-like scenario where the generator aims to fool the discriminator, while the discriminator tries to detect fake data.

---
 
##  Project Description

### 1. Dataset Preparation
We used medical images in **DICOM format**, commonly used for medical imaging data. These were converted to standard **JPG format** using the open-source software **3D Slicer**. The code for the conversion process is included in the `tojpg.ipynb` notebook.

### 2. Model Implementation
The GAN implementation is provided in the Jupyter notebook `dcgan-img-medical.ipynb`, which includes:
- Generator and Discriminator architectures
- Data loading and preprocessing
- Training loop for simultaneous optimization
- Output visualization

### 3. StyleGAN Influence
We integrated techniques inspired by **StyleGAN** to enhance the diversity and visual quality of the generated images. These modifications were experimental and focused on style mixing and latent vector transformations.

### 4. GitHub Integration
The project started from an open-source GAN repository on GitHub. The models and training logic were adapted to work specifically with medical images and to support DICOM conversion.

---

##  Project Structure

- `dcgan-img-medical.ipynb` – Full GAN implementation (generator, discriminator, training)
- `tojpg.ipynb` – Script to convert DICOM images to JPG using slicer
- `outputs/` – Folder for generated images after each epoch
- `imagmedical/` – Folder for converted JPG images used for training

---

## Technologies Used

- Python 3.x
- PyTorch (or TensorFlow, depending on your implementation)
- NumPy
- fast ai
- Matplotlib
- 3D Slicer (for DICOM conversion)

---

##  Livale Demo

Visit the live demo: **[https://your-username.github.io/gan-project](https://your-username.github.io/gan-project)**  
(Replace this link with your actual GitHub Pages URL if applicable)

---

## Sample Results

Here are sample outputs from the trained GAN:

![DCGAN](https://od.lk/s/ODZfNjkzODM2OTRf/dcgansimple.jpg)

![style gan](https://od.lk/s/ODZfNjkzODM2OTZf/stylegan.jpg)
![Generator and Discriminator Loss During Training](https://od.lk/s/ODZfNjkzODM3NjFf/loss.jpg)
---
https://od.lk/s/ODZfNjkzODM3NjFf/loss.jpg
## Author

- **Your Name**
-sellami siham   - fatma zouhre bedjbedj   -ikram saidani
 
---

## Future Improvements

- Integrate more advanced StyleGAN features.
- Use image quality metrics such as FID or IS to evaluate outputs.
- Deploy an interactive online tool to generate new samples.
