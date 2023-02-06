# MLP_training_with_noisy_labels
Jupyter notebook for the training of neural networks with potentially noisy labels. This implementation uses pytorch and trains an MLP with and without noisy labels on the MNIST dataset.

## Sources and notes
- Much of the EM code is copied or adapted from https://github.com/Ryo-Ito/Noisy-Labels-Neural-Network as well as some of the data visualization concepts. This notebook uses Pytorch+Numpy whereas the code it is based off of uses Chainer+Numpy.
- Original paper this notebook is based off of https://www.eng.biu.ac.il/goldbej/files/2012/05/icassp_2016_Alan.pdf (Training deep neural-networks based on unreliable labels)
- Helpful link regarding this topic https://github.com/subeeshvasu/Awesome-Learning-with-Label-Noise
- A generalized MLP (i.e. can have more than a single hidden layer) was written with a structure and training loops similar to Patrick Loebers pytorch videos https://www.youtube.com/watch?v=0_PgWWmauHk. The usability/generality is mildly inspired by sklearns mlp class
- Random seed funtionality for batching / training is not included, but could be added, or switch to pytorch native batching / loader functions

## General use case and results

- One section is included to train a baseline MLP model based on the default labels

  ![baseline_training](https://user-images.githubusercontent.com/20343526/216840115-9563f90e-43cd-4578-a979-62c291a2c9e5.png)

<br><br>
  
  
- Another section is included to alter the labels to a noisy version and then attempts to correct them via the algorithm proposed by Bekker and Goldberger. If the algorithm performs as advertised, then you should get a similar image to the following where labels in red are the noisy labels that have been attempted to be "corrected"

  ![noisy_label_correction](https://user-images.githubusercontent.com/20343526/216840213-d2504c6f-fc98-4204-b99b-5353d163b323.png)

<br><br>

## Note
- This is NOT an official implementation. Please help fix any bugs you may find :)
