# English-to-Bengali-Neural-Machine-Translation-with-Attention

1. Attention Mechanism: Encoder states are concatenated with the decoder state of the previous time step. Then it is fed to a neural network whose output layer activation function is a softmax over time. This produces alphas which signify the amount of attention we should give to each state of the encoder.
2. Alphas are multiplied with corresponding encoder states to produce a context vector. This context vector concatenated with targeted output (which is used for Teacher-Forcing) is used as the input for a single time step of the decoder.
3. Procedures 1 & 2 are repeated for each time step of the decoder.
4. While predicting, we have to build a separate decoder model. This time, the decoder produces one output and uses that output as the input along with the context vector to produce the output of the next time step. 
