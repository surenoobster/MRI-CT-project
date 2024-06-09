# MRI-CT-project



Disclaimer i used this project https://github.com/kaledhoshme123/VAE-CycleGAN-MRI-CT-Scan-Images
for ref and learning part

### Project: Generating CT Images from MRI Images Using VAE-CycleGAN

This study focuses on generating CT images from MRI images through the use of VAE-CycleGAN, leveraging unsupervised learning to address the challenge of limited dataset size. The inherent epistemic uncertainty due to the small sample size necessitates the use of probabilistic models for forming the latent space.

### Methodology

#### VAE-CycleGAN Architecture

The proposed model integrates Variational Autoencoders (VAE) with CycleGAN, creating a robust framework for generating CT images from MRI images. Key components include:

- **Variational Autoencoder (VAE)**: Shapes the latent space, ensuring the probability distributions are as close as possible to the standard Gaussian normal distribution.
- **CycleGAN**: Facilitates the bidirectional transformation between MRI and CT images without paired training examples.

#### Latent Space Shaping

The latent space shaping is crucial in managing the epistemic uncertainty and improving the model's generative capabilities. By ensuring that the probability distributions in the latent space are close to a standard Gaussian normal distribution, the model maintains consistency and robustness in image generation.

### Discriminator Structure

The discriminator's role is to differentiate between real and generated images, and its structure has been enhanced to extract more significant features:

- **Deeper Discriminator Structure**: A deeper network enables the extraction of more intricate features, enhancing the discriminator's ability to distinguish between real and fake images.
- **Feature Adjustment**: The methodology used in the discriminator adjusts the features extracted from previous convolutional layers based on the output of the last convolutional layer. This process ensures that the features are real and appropriate for the final convolutional output.

#### Derivative Independence Methodology

This approach forces the discriminator to adjust its weights in previous convolutional layers, ensuring the extracted features are realistic and suitable for the final layer's output. By examining the features as real or fake, the discriminator gains a deep understanding of the critical features for accurate image generation.

### Training and Data Augmentation

The model was trained for 2401 epochs using Google Colab. Due to the small sample size in the dataset, data augmentation was employed to expand the generation capacity:

- **Data Augmentation**: Each sample was augmented to create an additional copy, enhancing the model's ability to learn from a more extensive set of examples.

### Results

The model achieved promising results in generating CT images from MRI images, demonstrating:

- **High-Quality MRI to CT Transformation**: The transition from MRI to CT images yielded good results, attributed to the relative ease of this transformation.
- **Acceptable CT to MRI Transformation**: The reverse transformation (CT to MRI) was more challenging, achieving acceptable results. The difficulty is likely due to the inherent complexity and the smaller sample size in the dataset.

### Conclusion

This study highlights the effectiveness of using VAE-CycleGAN for generating CT images from MRI images. The enhancements in the discriminator structure and the use of data augmentation were critical in overcoming the challenges posed by the limited dataset size. The approach demonstrates the potential for improved medical imaging techniques, particularly in scenarios where acquiring paired MRI and CT images is impractical.






![Screenshot from 2024-06-07 19-51-51](https://github.com/surenoobster/MRI-CT-project/assets/154669584/3feba7b1-a085-4259-beb9-03be86bc5ac6)

pic from training phase 


![Screenshot from 2024-06-07 19-52-12](https://github.com/surenoobster/MRI-CT-project/assets/154669584/e5001c1e-efe7-4b1e-896f-333dd0b3ff13)

pic from generation part



![Screenshot from 2024-06-07 19-52-12](https://github.com/surenoobster/MRI-CT-project/assets/154669584/e5001c1e-efe7-4b1e-896f-333dd0b3ff13)

generating CT to MRI 
