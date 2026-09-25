Developed a convolutional autoencoder for dimensionality reduction and image reconstruction using the Overhead-MNIST dataset, focusing on Stadium and Oil Gas Field aerial imagery.

Key work:
- Performed data loading, pixel scaling, visualization, and preprocessing on 28×28 grayscale images, using a 128-dimensional latent representation to compress the original 784-dimensional input.
- Split the dataset into 80% training, 10% validation, and 10% test sets, while training separate autoencoder models for the Stadium and Oil Gas Field classes.
- Built a baseline convolutional autoencoder using Conv2D, MaxPooling, Dense, UpSampling, and Sigmoid layers, trained with Binary Crossentropy loss.
- Evaluated reconstruction quality using Structural Similarity Index (SSIM), achieving a baseline mean test SSIM of 0.4903.
- Improved the architecture by adding convolutional refinement layers to the encoder and decoder and introducing a combined MSE + SSIM loss to better preserve image structure and fine-grained visual details.
- Performed hyperparameter tuning across different encoder/decoder refinement configurations, loss functions, and learning rates, with the best configuration using encoder and decoder refinement, MSE + SSIM loss, and a learning rate of 5×10⁻⁴.
Achieved a mean test SSIM of 0.7377 with the improved autoencoder, increasing reconstruction quality by 0.2474 compared with the baseline.
- Achieved class-level mean SSIM improvements from 0.6753 to 0.8238 for Stadium and from 0.3148 to 0.6561 for Oil Gas Field.