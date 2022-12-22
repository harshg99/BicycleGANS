# BicycleGANS for multi-modal image to image generation

## Introduction 
This repository outlines the design and results of the Bicycle GAN project our group implemented for our final project. The network utilizes properties of both VAEs as well as GANs to improve results when compared with traditional Generative Adversarial Networks. In utilizing the abilities of VAEs to reconstruct a wide set of images from the latent space, and leveraging the image quality that GANs are capable of generating, Bicycle GAN is able to generate a diverse set of realistic image results, utilizing a single image and noise vectors for inputs.  For our application, we chose to utilize the edges2shoes dataset which provides edge maps paired with shoe images..   This network utilizes two separate discriminators called cVAE-GAN and cLR-GAN which each work to improve the quality of the image reconstruction, as well as an encoded noise vector to encourage diversity. Furthemore, our team performed both qualitative and quantitative evaluations of the network results, including utilizing FID and LPIPS scores in order to rate the network over the edge2shoe dataset.  These results as well as example output images are exhibited later in the document as we explain the subtleties of our network implementation. Additionally, we test our network over the night2day dataset which provides an evening image paired with daytime images and the maps dataset which provides matching google maps images with satellite data.


## Network 

![image](https://user-images.githubusercontent.com/28558013/209128220-40cc767a-c6c7-468b-b904-9788e3067a01.png)


## Results

Multi modal generation over the esdges to shoe dataset

![image](https://user-images.githubusercontent.com/28558013/209128100-00c38b5c-811c-4e42-8ed1-7a87370694b9.png)

Multi Modal generation over maps and night2 day datasets
![image](https://user-images.githubusercontent.com/28558013/209127889-7d0716e8-4b6a-426e-8005-ea38842877a2.png)

## Discriminator architecture comparisons
![image](https://user-images.githubusercontent.com/28558013/209128364-cf96e6a0-582d-43ef-9e1a-389a3e6e6380.png)

