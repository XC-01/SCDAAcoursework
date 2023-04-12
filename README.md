# SCDAAcoursework

Ling Chen s2308010
Xi Chen   s1817189

In coursework_q1.ipynb, class LQR_Ricatti is focused on Exercise 1.1. H,M,C,D,R,T should be provided to initialize the class, where C,R,D are 2*2 matrices, H, M are matrices and T is a positive number. For the method solve_Ricatti(self,t_grid), the input is a numpy array or a torch tensor. For the other two method, control_value(self,t,x) and markov_control(self,t,x), the input should be one torch tensor of dimension batch size (for time) and another torch tensor of diemension batch size * 1 * 2 (for space). After running the class, an example is provided. The parameters can be changed here. 

Then, the method calculate_error(num_time_steps,num_samples) is based on Exerciese 1.2. The inputs are positive integers, representing number of time steps and number of samples respectively. In the method, all the parameters H,M,C,D,R,T, and x_grid can be changed. After running the method, two log-log plots are displayed with different numbers of time steps and different numbers of samples.
