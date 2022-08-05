# NNFL-Second-Sem-2022
These are the assignments of the course Neural Network and Fuzzy Logic (BITS F312) prepared with a group of teaching assistants during second semester 2020-21 at BITS Pilani. 

Assignment - 1

Changes/Clarifications in Part A of Part 1
In the function initialize_parameters(X, Y), you're supposed to initialize biases to zeros and that should bring your sgd_losses[2000] close to "0.42061". In the current version, you can change "0.359x" to "0.42061".
We have provided the solution for two functions, i.e., standardize(X) and loss(y_pred, y_true).

Changes/Clarifications in Part B of Part 1
In initialization(I, H1, H2, H3, O), along with bias, initialize weights for momentum (m_dw{i} and m_db{i}) and RMS  (v_dw{i} and v_db{i}) to zeros. You have to keep the weights in the range [0,0.1) and not [0,1). 
Please take care of the dimensions while performing matrix multiplication in feed_forward(X, params) function. 
In back_prop_linear(da_layer, z_layer, input, act_fxn, m, lmbda, weight), there's a typo in the documentation. dz will not be directly equal to dsigmoid or dwish. To calculate dz, you need to multiply da_layer with either dsigmoid or dwish. Please take care of the dimensions. 

Changes/Clarifications in Part 2
There is a typo in the documentation of the Custom Model section. We have instructed you to use softmax activation for the last layer of your model but it is supposed to be sigmoid.

Assignment - 2

CNN Assignment 
for identity_downsample, keep kernel_size=3, stride=2, and padding=1.
for 2nd Conv layer of ResBlock, keep kernel_size=3, stride=1, and padding=1.

RNN Assignment 
1. Read the input line by line using `readlines()`rather than `read()`. You could ideally use `read()` too but that would create a different vocab and thus fail test cases.
2. For `pad_sequence()`, ensure that per line of the dataset, you get only one sequence. If there are tokens beyond SEQ_LEN, let them be.
3. For the rnn, assume that the output has a length = HIDDEN_LEN, rather than EMB_DIM. While both can be used, the assignment is following the first case.
