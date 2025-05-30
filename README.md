# Animal Audio Classifier
This repository contains a Jupyter notebook that serves as a practical example of how to utilize PyTorch Lightning for audio classification tasks. In this instance, we have selected a subset of [YashNita's Animal Sound Dataset](https://github.com/YashNita/Animal-Sound-Dataset), focusing on five specific animal classes: chicken, cow, donkey, frog, and sheep. To extract features from the audio data, we employ the [Librosa](https://librosa.org/doc/latest/index.html) library, which is well-regarded for its robust audio analysis capabilities. The model architecture contains two convolutional layers, each followed by a max pooling layer, leading into a fully connected layer designed to enhance classification performance. However, it is important to note that the model's accuracy is currently not satisfactory, indicating ample opportunity for improvement. I encourage students to engage with this example actively, exploring ways to refine the model and enhance its performance. This notebook is intentionally designed as a foundational starting point, and it does not strictly adhere to established best practices, allowing you the freedom to experiment and innovate as you work through the material.

## Possible considerations
The following is a list of considerations for improvement or for your own project.

- The train/val/test-split is random and does not guarantee that all classes are represented well in val and test. This is of a particular concern for unbalanced data (which this example has) as it is technically possible that a class does not appear in val or test and therefore the model cannot be validated or tested for that class. To counter this issue the split was made to quite largely favour the val and test proportions whereas a common practice would be to keep them smaller and have more train data.
- There is no evaluation on whether the model is overfitted, it may very well be.
- Currently only 13 MFCC features are extracted from librosa, quite likely additional features may be interesting to add.
- Adding a Confusion Matrix might be a good idea.
- more?

## Citation & Star
If you use my work please cite and star ⭐ this repo. Thanks!

Michielsen, Bas S.H.T. (2025) "Animal Audio Classifier" GitHub: https://github.com/bshtmichielsen/classification_audio--animals