# Disentangled-Face-Editing-via-Individual-Walk-in-Personalized-Facial-Semantic-Field
This project demonstrates the examples of disentangled face editing by our method. More experiment results will be public.
We conduct our experiments on the face datasets FFHQ and CelebaHQ. The homepage of FFHQ is at https://github.com/NVlabs/stylegan and the dataset can be downloaded at https://drive.google.com/drive/folders/1u2xu7bSrWxrbUxk-dT-UvEJq8IjdmNTP. The homepage of CelebaHQ is at [https://github.com/NVlabs/stylegan](https://github.com/tkarras/progressive_growing_of_gans) and the dataset can be downloaded at [https://drive.google.com/drive/folders/1u2xu7bSrWxrbUxk-dT-UvEJq8IjdmNTP](https://drive.google.com/drive/folders/0B4qLcYyJmiz0TXY1NG02bzZVRGs?resourcekey=0-arAVTUfW9KRhN-irJchVKQ).

Only the single target attribute (e.g., eyeglasses, gender, expression, or mustache) is edited with the others unchanged. The background and identity are preserved during editing. All results are with high resolution 1024*1024.
![1.jpg](https://github.com/lcd21/PFSF/blob/main/FigEditedExamplesOurmethod.jpg)

The framework of our method. For a given face image, the personalized facial semantic field (PFSF) is built by inverting it into the latent space of GAN and retraining GAN together, which is colored blue. After the PFSF is built, the generator of GAN is fixed and a pretrained facial attribute classifier is used as supervision for searching disentangled non-line semantic direction in the PFSF. This individual non-linear walk aims to walk in the right semantic direction, making the given face image edited according to the semantic target (e.g., smiling). The editing process is colored in orange. Finally, the edited portrait is fused with the background of the original image.
![3.jpg](https://github.com/lcd21/PFSF/blob/main/Framework.jpg)

Visual comparison between examples edited from InterFaceGAN and our method. InterFaceGAN removes the mustache and background from the top instance while adding eyeglasses, and adds eyeglasses to the bottom face during aging. In contrast, our method preserves other attributes and the background quite well.
![3.jpg](https://github.com/lcd21/PFSF/blob/main/FigentangledExamples.jpg)




