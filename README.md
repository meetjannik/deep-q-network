# Deep Q-Network

A PyTorch implementation of ["Human-Level Control Through Deep Reinforcement Learning"](https://www.nature.com/articles/nature14236). 

#### Implementation Details
I implemented the environment wrapper in an attempt to make it applicable to all OpenAI Gym Atari environments. However, I have not evaluated it on environments other than Breakout and Pong, wherefore specifics of other environments might not be considered. 

#### Training Details
I use the training parameters as described in the original paper, except I use a smaller replay memory (100k) and start experience replay earlier (after 25k steps). 

#### Evaluation
The agent achieves a game score of 129.8 on Breakout using experience replay and target Q, while the original authors achieve 316.6. In general, results of deep reinforcement learning methods are difficult to reproduce due to non-determinism in standard benchmark envrionments, combined with variance intrinsic to the methods [(Henderson, Peter, et al.)](https://ojs.aaai.org/index.php/AAAI/article/view/11694). However, this might also be the result of a bug in the code. 

https://user-images.githubusercontent.com/62884101/226115738-cc7f8f70-af1e-4db6-8847-ff9c68fb17e7.mp4
