# SCDAAcoursework

Ling Chen s2308010
Xi Chen   s1817189

In coursework_q1.ipynb, class LQR_Ricatti is focused on Exercise 1.1. H,M,C,D,R,T should be provided to initialize the class, where C,R,D are 2*2 matrices, H, M are matrices and T is a positive number. For the method solve_Ricatti(self,t_grid), the input is a numpy array or a torch tensor. For the other two method, control_value(self,t,x) and markov_control(self,t,x), the input should be one torch tensor of dimension batch size (for time) and another torch tensor of diemension batch size * 1 * 2 (for space). After running the class, an example is provided. The parameters can be changed here. 

Then, the method calculate_error(num_time_steps,num_samples) is based on Exerciese 1.2. The inputs are positive integers, representing number of time steps and number of samples respectively. In the method, all the parameters H,M,C,D,R,T, and x_grid can be changed. After running the method, two log-log plots are displayed with different numbers of time steps and different numbers of samples.

In the file coursework final version q234.ipynb, we complete the other three sections of the coursework. 

The first block is the same as the code for Exercise 1.1. Then we generate the sample data for the rest part. H,M,C,D,R,T can be changed in the second block. Then, using the generated data, the third block takes the neural network with hidden layer size of 100 for value function, and plots the training loss. The next part is the FFN class, which is supervised learning of Markov control. Similarly to 2.1, the code trains the given data and plot the training loss, with t_samples, x_samples and m_samples in the type of torch tensors. Here n_epochs is equal to the number of samples. The loss are calculated by MSE in both Exercise 2.1 and 2.2.

For Exercise 3, we assume that n equals to m (size of x sample), and the timestep size is also equals to m. The parameters n,m,H,M,C,D,R,T,sigma can be changed. The samples of t, x, and u are Numpy array in this part. Then, the resulting sample of u is calculated. After that, the model is trained with the method train_pde(), and the plot of training loss is displayed.

For the final section, the first block is the same as that in Exercise 3. Then, alpha is initialized, which could be changed. alpha is updated and v is estimated in the for loop, while the number of iterations is also equal to m and n. Finally, we take the mean of the difference between each column of estimated v (v_alpha) and the optimal value from Exercise 1.1 (v_true).
