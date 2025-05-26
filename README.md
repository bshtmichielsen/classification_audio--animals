# Pytorch Lightning example for audio classification
The repo contains a notebook that serves as an example on how to use Pytorch Lightning for the purpose of audio classification. The data files are included in the repo and are a subset of [YashNita's Animal Sound Dataset](https://github.com/YashNita/Animal-Sound-Dataset). Feel free to use this example in your Machine Learning course. As this is merely an example for getting started, the notebook is dileberately incomplete and/or does not follow common practice, it is a learning example and improvements are left to the reader to make and reason about.

## Possible considerations
The following is a list of considerations for improvement or for your own project.

- The train/val/test-split is random and does not guarantee that all classes are represented well in val and test. This is of a particularly concern for unbalanced data (which this example has) as it is technically possible that any particular class does not appear in val or test and therefore the model cannot be validated or tested for that class. To counter this issue the split was made to quite largely favour the val and test proportions whereas a common practice would be to keep them smaller and have more train data.
- There is no test on whether the model is overfitted, it may very well be.
- Currently only 13 MFCC features are extracted from librosa, quite likely additional features may be interesting to add.
- Adding a Confusion Matrix might be a good idea.
- more?