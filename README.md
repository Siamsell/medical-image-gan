<div align="center">
  <h1 style="font-size: 3.5rem; font-weight: 900; background: linear-gradient(90deg, #051C2F, #DB7093); -webkit-background-clip: text; color: transparent; margin-bottom: 1rem; font-family: 'Segoe UI', sans-serif;">
    MEDICAL IMAGE SYNTHESIS WITH GANS
  </h1>
  
  <div style="max-width: 600px; margin: 0 auto 2rem; padding: 0 1rem;">
    <p style="font-size: 1.1rem; color: #555; line-height: 1.6;">
      Advanced DCGAN architecture enhanced with StyleGAN techniques for generating 
      high-fidelity medical images from DICOM datasets
    </p>
  </div>

  <div style="display: flex; justify-content: center; gap: 1.5rem; margin: 2rem 0;">
    <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white&logoWidth=20">
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
    <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=Jupyter&logoColor=white">
    <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge">
  </div>
</div>

<div align="center">
  <img src="https://od.lk/s/ODZfNjkzODQ1MTZf/logo%20%281%29.png" width="800"  style="border-radius: 50%; object-fit: cover; border: 1px solid #eee; box-shadow: 0 8px 24px rgba(0,0,0,0.12); margin-top: 2rem;">
</div>

## Key Features
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; margin: 2rem 0;">
  <div style="background: #F8F9FA; padding: 1.5rem; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.05);">
    <h3 style="color: #051C2F; margin-top: 0;">Medical-Grade Synthesis</h3>
    <p>Generate DICOM-compatible synthetic images with anatomical accuracy</p>
  </div>
  <div style="background: #F8F9FA; padding: 1.5rem; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.05);">
    <h3 style="color: #051C2F; margin-top: 0;">Hybrid Architecture</h3>
    <p>DCGAN stability combined with StyleGAN's visual quality</p>
  </div>
  <div style="background: #F8F9FA; padding: 1.5rem; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.05);">
    <h3 style="color: #051C2F; margin-top: 0;">Clinical Validation</h3>
    <p>Quantitative metrics (FID, SSIM) for medical relevance</p>
  </div>
</div>
</div>

#  Medical Image Synthesis with GANs
The project entails employing **Generative Adversarial Networks (GANs)**—an ambitious class of deep learning models—to create realistic medical images. The method is used in the **DCGAN (Deep Convolutional GAN)** model with inspiration from **StyleGAN** for extra visual realism and diversity.


## What is a GAN?

A **Generative Adversarial Network (GAN)** is a machine learning algorithm that consists of two neural networks: a Generative Network and a Discriminator Network.

- **Generator**: Produces synthetic data (e.g., images) from noise.
- **Discriminator**: Learns to identify whether data is real or synthetic data.
Both models are trained jointly within a framework of a game where the generator attempts to deceive the discriminator, and the discriminator attempts to detect counterfeit data.

```mermaid
graph TD
    A[Random Noise]:::noise --> B[Generator]:::generator
    B --> C[Fake Images]:::fake
    D[Real Images]:::real --> E[Discriminator]:::discriminator
    C --> E
    E --> F[Loss Feedback]:::loss
    F -->|Update| B
    F -->|Update| E
    classDef noise fill:#F0F8FF,stroke:#051C2F,stroke-width:2px,color:black
    classDef generator fill:#E6E6FA,stroke:#170637,stroke-width:2px,color:black
    classDef fake fill:#FFE4E1,stroke:#661B0E,stroke-width:2px,color:black
    classDef real fill:#F0FFF0,stroke:#2E8B57,stroke-width:2px,color:black
    classDef discriminator fill:#D5ABB9,stroke:#DB7093,stroke-width:2px,color:black
    classDef loss fill:#BABAAA,stroke:#FFD700,stroke-width:2px,color:black
```
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
- `imagme_medical.zip/` – JPG image storage directory created from DICOM for training
- `stylgan.ipynb/` _ StyleGAN3 model
- `costum-dataset.ipynb/` _ Medical Image Dataset Loader and Visualizer for Deep Learning (PyTorch)
---
## Technologies Used

| Tool / Library    | Purpose                             |
|-------------------|-------------------------------------|
| Python 3.x        | Programming language                |
| PyTorch / TensorFlow | Deep learning frameworks         |
| NumPy             | Numerical computation               |
| Matplotlib        | Visualization                       |
| fastai            | Training simplification             |
| 3D Slicer         | DICOM image conversion              |
---
##  Livale Demo

 **[GitHub Project Page](https://github.com/Siamsell/medical-image-gan)**
---
## Sample Results
### DCGAN Output
## Dataset Name and Provider
- Dataset Name: Pancreas-CT
- Provider: The Cancer Imaging Archive (TCIA)
- URL for Access:
[dicom dataset](https://www.cancerimagingarchive.net/collection/pancreas-ct/)**
## Reading DICOM files:
DICOM files within each patient directory were searched and read recursively using the
pydicom library.
Slicing sorting:
Slices were sorted based on their Z-axis position (ImagePositionPatient[2]) to maintain
anatomical order. Volume standardization: Limited each volume to a maximum of 128
slices for intra-sample homogeneity. Normalization and resizing: Normalized all 2D slices
to pixel intensity range [0, 255] and resized to a default resolution of 256×256 pixels using
PIL library.
## Format conversion:
Converted preprocessed slices to individual JPEG (.jpg) images instead of the original
DICOM format to easily input into 2D convolutional networks.
Archiving:
Finally, the complete output directory containing the JPEG images was archived into a
ZIP file for easy storage and retrieval. Upon completion of creating the ZIP archive, the
file was stored on the local system. An attempt to drop empty slices, the final filtering
step was carried out to improve further the quality of the dataset.
Zero-filled slice is a fully black 2D image (approximately equal pixel intensity
to zero) with no useful anatomical information. These are typically at the beginning
and end of CT volumes where no patient tissue is represented. Low pixel intensity slices
were removed from the data to ensure that the model trains on only useful anatomical
information.
After the removal of all such blank slices, the cleaned collection of JPEG images were
then uploaded to Kaggle again as a cleaned curated dataset. Subsequent to this cleaned
and curated dataset, a Deep Convolutional Generational Adversarial Network (DCGAN)
was also trained for the generation of realistic fake abdominal CT slices.

### DCGAN-Inspired Output
![DCGAN](https://od.lk/s/ODZfNjkzODM2OTRf/dcgansimple.jpg)
### StyleGAN-Inspired Output

![StyleGAN](https://od.lk/s/ODZfNjkzODM2OTZf/stylegan.jpg)
### Training Losses

![Training Loss](https://od.lk/s/ODZfNjkzODM3NjFf/loss.jpg)
---
## Authors
# SS | Sellami Siham
# BF | bedj bedj Fatma Zohra
# IS | Ikram Saidani
## Future Improvements

- Use high-end **StyleGAN2/3** modules

- Ranked by metrics such as **FID** or **IS**
- Use a **web-based interactive generator**
- Train on **larger and labeled datasets**
