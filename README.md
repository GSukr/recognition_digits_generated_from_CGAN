# recognition_digits_generated_from_CGAN
Evaluating labeled images generated using Conditional Generative Adverserial Nets 
Evaluating labeled images generated using Conditional Generative Adverserial Nets (CGAN)
This notebook evaluates the quality of fake labeled images generated using CGAN

CGAN implemetation used: https://github.com/eriklindernoren/Keras-GAN/blob/master/cgan/cgan.py, but this can be substituted for alternate implementations.

Intrinsic measures that indicate high quality generated images:

* The predictive accuracy of the discriminator should approach 0.5 indicating that the generated images are indintinguishable from the real images.
* The (binary cross-entropy) loss of the generator as well as the loss of the discriminator, approach -log(0.5)=0.69

Extrinsic measures that indicate high quality generated images:

* Class distribution in the real and the generated images are very similar.
* A model trained on generated data has similar predictive accuracy as a model trained on the original images.

Results indicate that the approach presented in this notebook does very well in terms of both intrinsic measures and the first extrinsic measure, but has room for improvement in terms of the second extrinsic measure.


