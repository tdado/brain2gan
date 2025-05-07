# brain2gan

This repo accompanies the paper "Brain2GAN: Feature-disentangled neural coding of visual perception in the primate brain" where we aimed to characterize the high-level neural representations as recorded via cortical implants in a macaque. Our results show that feature-disentangled GAN latents outperform other candidate representations of the visual data in predicting high-level brain activity (i.e., neural encoding). We then used these feature-disentangled representations to reconstruct the perceived stimuli from brain activity with state-of-the-art quality (i.e., neural decoding). You can find our implementations of neural encoding and -decoding in the provided Jupyter notebooks. The brain recordings to achieve these results will be made available upon publication of the paper.

![Alt text](https://github.com/tdado/brain2gan/blob/main/media/img.png)

### Notebooks

The following Jupyter notebooks are included in this repository:

- `synthesis_faces.ipynb`: This notebook contains the code used to generate the stimulus dataset of face images.
- `synthesis_images.ipynb`: This notebook contains the code used to generate the stimulus dataset of natural images.
- `feature_extraction.ipynb`: This notebook contains the code used to extract intermediate feature activations from VGG16 pretrained on face and object recognition for faces and natural images, respectively, as well as language-regularized CLIP latents.
- `neural_encoding.ipynb`: This notebook contains the code used to predict brain activity from feature representations of recent deep neural networks with different properties such as feature disentanglement and language regularization.
- `neural_decoding_faces.ipynb`: This notebook contains the code used to reconstruct perceived faces from brain activity.
- `neural_decoding_images.ipynb`: This notebook contains the code used to reconstruct perceived natural images from brain activity.


### Time-based neural decoding

The use of intracranial recordings provided for spatiotemporal analysis of brain activity in unprecedented detail. The gifs illustrate how meaningful information gets extracted from the stimulus-evoked brain responses in time. Per trial, neural responses were recorded for 300 ms with stimulus onset at 100 ms. Prior to stimulus onset, the reconstruction is an average-looking image, after which it starts to take on an appearance that closely resembles the originally perceived stimulus.

<p align="center">
  <img src="https://github.com/tdado/brain2gan/blob/main/media/0093.gif" width="100" />
  <img src="https://github.com/tdado/brain2gan/blob/main/media/0018.gif" width="100" />
  <img src="https://github.com/tdado/brain2gan/blob/main/media/0038.gif" width="100" />
  <img src="https://github.com/tdado/brain2gan/blob/main/media/0001.gif" width="100" />
  
  
  <img src="https://github.com/tdado/brain2gan/blob/main/media/0094.gif" width="100" />
  <img src="https://github.com/tdado/brain2gan/blob/main/media/0197.gif" width="100" />
  <img src="https://github.com/tdado/brain2gan/blob/main/media/0081.gif" width="100" />
  <img src="https://github.com/tdado/brain2gan/blob/main/media/0114.gif" width="100" />
</p>
