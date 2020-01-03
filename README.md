# Transfer Learning Implementation
 Program implementing Transfer learning technique for the Devanagari Character Recognition. 
 
Transfer Learning refers to is a machine learning method where a model developed for a task is reused as the starting point for a model on a second task. Hence preventing from training model from scratch thus saving the training time and computational power.
 
Three Approaches has been used in order to carry out the transfer learning for the purpose of Devanagari Character Recognition and the accuracy of all three approach has been compared.
1) The VGG16 model pretrained over imagenet dataset was loaded and with all convolutional layer frozen only changing the dense layer according to requirement of classes for the classification of Devanagari Characters. 
2) The VGG16 model now is not totally freezed. The last layers of convolutional layers along with dense layers is fine tuned.
3) A custom Model pretained on MNIST dataset(for number classification) which is similar to Devanagari Character Dataset was loaded and with all convolutional layer freezed and dense layer fine tuned was used for the training of Devanagari dataset.

Hence transfer Learning was implemented.

# Models and Weights
1) vgg16 model is provided by keras which is pretrained on imagenet dataset
2) mnist.json is the model trained for MNIST Dataset and mnist.h5 is the weights obtained after training MNIST dataset.
3) VGG total frozen model.json is the model used for transfer learning with all convolutional layers of VGG model freezed. 
4) weights for Devanagri classification with total frozen VGG layers.h5 contains weights saved after training using first approach
5) VGG fine tuning.json is the model used for transfer learning with last layers convolutional layers of VGG model fine tuned. 
6) weights for Devanagri classification with VGG last layers fine tuned.h5 contains weights saved after training using second approach
7) MNIST Model fine tuning.json is model used for transfer learning with pretrained custom model trained on MNIST data.
8) weights for Devanagri classification using fine tuning over MNIST Model.h5 contains weights saved after training using third approach 
