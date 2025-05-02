
# Medical Image Synthesis with GANs

The project entails employing **Generative Adversarial Networks (GANs)**—an ambitious class of deep learning models—to create realistic medical images. The method is used in the **DCGAN (Deep Convolutional GAN)** model with inspiration from **StyleGAN** for extra visual realism and diversity.
# Medical Image Synthesis with GANs

The project entails applying **Generative Adversarial Networks (GANs)**—a class of deep learning that shoots high—to generate realistic medical images. The process is applied under the **DCGAN (Deep Convolutional GAN)** model based on **StyleGAN** for increased visual realism and diversity.

## What is a GAN?

A **Generative Adversarial Network (GAN)** is a machine learning algorithm that consists of two neural networks: a Generative Network and a Discriminator Network.

- **Generator**: Produces synthetic data (e.g., images) from noise.
- **Discriminator**: Learns to identify whether data is real or synthetic data.
Both models are trained jointly within a framework of a game where the generator attempts to deceive the discriminator, and the discriminator attempts to detect counterfeit data.

---
## Project Description
### 1. Dataset Preparation

Medical images in **DICOM format**, the standard for medical imaging data, were utilized. Images were also translated to standard **JPG format** using open-source platform **3D Slicer**. Transformation code exists in `tojpg.ipynb` notebook.
### 2. Model Implementation

GAN implementation is demonstrated in Jupyter notebook `dcgan-img-medical.ipynb`, including:
- Generator and Discriminator architecture
- Data loading and preprocessing
- Long-term loop of optimization training
- Output visualization
### 3. StyleGAN Influence

We utilized styleGAN-based techniques for enhancing greater diversity and quality of output images. Latent vectors' style mixing and manipulation were accomplished through experiments in modification.
### 4. Integration with GitHub

We started the project from an open-source GAN repository on GitHub. The model and training environment were both modified to make them independently executable using medical images and DICOM conversion support.

---

- `dcgan-img-medical.ipynb` – Full GAN code (generator, discriminator, training)

- `tojpg.ipynb` – Python script to convert JPG images from DICOM using slicer
- `outputs/` – Where images should be output after each epoch
- `imagmedical/` – JPG image storage directory created from DICOM for training
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

???? **[GitHub Project Page](https://github.com/Siamsell/medical-image-gan)**
---
## Sample Results

### DCGAN Output

![DCGAN](https://od.lk/s/ODZfNjkzODM2OTRf/dcgansimple.jpg)
### StyleGAN-Inspired Output

![StyleGAN](https://od.lk/s/ODZfNjkzODM2OTZf/stylegan.jpg)
### Training Losses

![Training Loss](https://od.lk/s/ODZfNjkzODM3NjFf/loss.jpg)
---
## Authors

- Sellami Siham
- Fatma Zouhre Bedjbedj
- Ikram Saidani
---
##???? Future Improvements

- Use high-end **StyleGAN2/3** modules

- Ranked by metrics such as **FID** or **IS**
- Use a **web-based interactive generator**
- Train on **larger and labeled datasets**

## What is a GAN?

A **Generative Adversarial Network (GAN)** is a machine learning model that includes two neural networks: a Generative Network and a Discriminator Network.

- **Generator**: Produces artificial data (e.g., images) from random noise.
- **Discriminator**: Learns to detect whether the data is authentic or artificial data.
Both models are simultaneously trained in an environment of a game in which the generator attempts to deceive the discriminator, while the discriminator attempts to detect counterfeit data.

---
## Project Description
### 1. Dataset Preparation

Medical images in **DICOM format**, the default for medical imaging data, were utilized. Images were converted into standard **JPG format** using open-source software **3D Slicer**. Code for transformation is provided in `tojpg.ipynb` notebook.
### 2. Model Implementation

Implementation of GAN is demonstrated in Jupyter notebook `dcgan-img-medical.ipynb`, with:
- Architecture of Generator and Discriminator
- Data loading and preprocessing
- Training of long-term loop of optimization
- Visualization of output
### 3. StyleGAN Influence

We have used styleGAN-based techniques to ensure greater diversity and quality of output images. Experiments were conducted in modifying, with a direction towards style mixing and manipulating the latent vectors.
### 4. Integration with GitHub

The project started with an open-source repository of GAN on GitHub. The training environment and model were both modified such that they could be run independently with medical images and support DICOM conversion.

---
## Project Structure

- `dcgan-img-medical.ipynb` – Full GAN code (generator, discriminator, training)

- `tojpg.ipynb` – Python script to convert JPG images from DICOM using slicer
- `outputs/` – Where images should be output after each epoch
- `imagmedical/` – JPG image storage directory created from DICOM for training
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

???? **[GitHub Project Page](https://github.com/Siamsell/medical-image-gan)**
---
## Sample Results

### DCGAN Output

![DCGAN](https://od.lk/s/ODZfNjkzODM2OTRf/dcgansimple.jpg)
### StyleGAN-Inspired Output

![StyleGAN](https://od.lk/s/ODZfNjkzODM2OTZf/stylegan.jpg)
### Training Losses

![Training Loss](https://od.lk/s/ODZfNjkzODM3NjFf/loss.jpg)
---
## Authors

- Sellami Siham
- Fatma Zouhre Bedjbedj
- Ikram Saidani
---
##???? Future Improvements

- Use high-end **StyleGAN2/3** modules

- Ranked according to metrics such as **FID** or **IS**
- Use a **web-based interactive generator**
- Train on **larger and labeled datasets**
