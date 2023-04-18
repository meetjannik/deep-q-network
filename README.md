# Deep Q-Networks

Replication of ["Human-Level Control Through Deep Reinforcement Learning"](https://www.nature.com/articles/nature14236). 

## Requirements

To install requirements:

```setup
pip install -r requirements.txt
```

## Implementation Details

I implemented the environment wrapper in an attempt to make it applicable to all OpenAI Gym Atari environments. However, I have not evaluated it on environments other than Breakout and Pong, wherefore specifics of other environments might not be considered. 

I use the training parameters as described in the original paper, except I use a smaller replay memory and start experience replay earlier than the original authors.

The agent achieves a game score of 129.8 on Breakout using experience replay and target Q, while the original authors achieve 316.6. In general, results of deep reinforcement learning methods are difficult to reproduce due to non-determinism in standard benchmark envrionments, combined with variance intrinsic to the methods [(Henderson et al. 2018)](https://ojs.aaai.org/index.php/AAAI/article/view/11694). However, this might also be a bug in the code. 

<div align="center">
  
  https://user-images.githubusercontent.com/62884101/226115786-cae633c3-9ba8-4952-8e9f-fedbc6267cff.mp4

</div>

### Citation   
```
@article{
  title={Human-Level Control Through Deep Reinforcement Learning},
  author={Volodymyr Mnih and Koray Kavukcuoglu and David Silver and Andrei A. Rusu and Joel Veness and Marc G. Bellemare and Alex Graves and Martin Riedmiller and Andreas K. Fidjeland and Georg Ostrovski and Stig Petersen and Charles Beattie and Amir Sadik and Ioannis Antonoglou and Helen King and Dharshan Kumaran and Daan Wierstra and Shane Legg and Demis Hassabis},
  journal={Nature},
  year={2015}
}
```
