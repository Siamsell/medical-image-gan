
# Medical Image Synthesis with GANs

The project entails employing **Generative Adversarial Networks (GANs)**—an ambitious class of deep learning models—to create realistic medical images. The method is used in the **DCGAN (Deep Convolutional GAN)** model with inspiration from **StyleGAN** for extra visual realism and diversity.
# Medical Image Synthesis with GANs

The project entails applying **Generative Adversarial Networks (GANs)**—a class of deep learning that shoots high—to generate realistic medical images. The process is applied under the **DCGAN (Deep Convolutional GAN)** model based on **StyleGAN** for increased visual realism and diversity.

## What is a GAN?

A **Generative Adversarial Network (GAN)** is a machine learning algorithm that consists of two neural networks: a Generative Network and a Discriminator Network.

- **Generator**: Produces synthetic data (e.g., images) from noise.
- **Discriminator**: Learns to identify whether data is real or synthetic data.
Both models are trained jointly within a framework of a game where the generator attempts to deceive the discriminator, and the discriminator attempts to detect counterfeit data.
-


```mermaid
graph TD
    A[Noise Aléatoire]:::noise --> B[Générateur]:::generator
    B --> C[Images Synthétiques]:::fake
    D[Images Réelles]:::real --> E[Discriminateur]:::discriminator
    C --> E
    E --> F[Feedback]:::loss
    F -->|Mise à jour| B
    F -->|Mise à jour| E
    
    classDef noise fill:#F0F8FF,stroke:rgb(5, 28, 47),stroke-width:2px
    classDef generator fill:#E6E6FA,stroke:rgb(23, 6, 55),stroke-width:2px
    classDef fake fill:#FFE4E1,stroke:rgb(102, 27, 14),stroke-width:2px
    classDef real fill:#F0FFF0,stroke:#2E8B57,stroke-width:2px
    classDef discriminator fill:rgb(213, 171, 185),stroke:#DB7093,stroke-width:2px
    classDef loss fill:rgb(186, 186, 170),stroke:#FFD700,stroke-width:2px
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
- `imagmedical/` – JPG image storage directory created from DICOM for training
---
## Technologies Used

| Tool / Library    | Purpose                             |
|-------------------|-------------------------------------|
| Python 3.x        | Programming language                |
| PyTorch / TensorFlow | Deep learning frameworks           |
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
## Future Improvements

- Use high-end **StyleGAN2/3** modules

- Ranked by metrics such as **FID** or **IS**
- Use a **web-based interactive generator**
- Train on **larger and labeled datasets**
