# Reconstruction_attack

The goal of this project is to attack a neural network during its federated training. We assume that you are the attacker, and thus that you have directly access to the update of your victim. This attack is described in the paper Deep leakage from gradient.

The Deep Leakage from Gradients is an algorithm to obtain the training inputs and the labels of a model. Firstly, we begin by generating in a random way a pair of dummy inputs and dummy labels. Secondly, we use these inputs and labels to do forward and backward propagation for the neural network. Then, we derivate the gradients from these data. Finally, we minimize the distance between our result gradient and the shared gradient to guess the original data. Therefore, when the distance between these gradients becomes very smaller, the resulting images that we get from the attack with these data becomes also better.
