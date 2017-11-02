---
layout: home
---

Hello, everyone. Thanks for visiting our website.   
This website serves as the guide and introduction to (Deep) Reinforcement Learning for RL beginners.  

## For beginners:

我们希望您在阅读本系列文章前已接触过(或已掌握)如下课程，书籍以及框架：

 - 一定的机器学习基础：
    - [CS229: Machine Learning][1]
    - [Hung-yi Lee: Machine Learning][2]
    - [周志华: 机器学习][3]
    - [Yuh-Jye Lee: Machine Learning][4]
 - 一定的深度学习基础：
    - [CS231n: Convolutional Neural Networks for Visual Recognition][5] 
    - [CS224d: Deep Learning for Natural Language Processing][6]
    - [Ian Goodfellow: Deep Learning][7]   「[chinese version][8]」
    - [Hung-yi Lee:Machine Learning and having it deep and structured][9]
 - 一定的深度学习框架使用经验：
    - [TensorFlow][10]
        - [CS 20SI: Tensorflow for Deep Learning Research][11]   
        - [aymericdamien/TensorFlow-Examples][12]
    - [PyTorch][13] 
        - [PyTorchZeroToAll][14] 
    - [Keras][15] 

若您没有任何机器学习(深度学习)的基础，我们希望您先花一点时间学习相关的课程(书籍)。   
若您没有接触过上述深度学习框架，我们也希望您先花一些时间来学习它。   
上面我们已经给出了适合您学习的机器学习/深度学习/主流框架教程。  
若本系列文章不符合您的味口，您还可学习如下 强化学习 的相关教程：  

- [Dave Silver: Reinforcement Learning][16]
- [Dave Silver —— Tutorial: Deep Reinforcement Learning][17]
- [CS 294: Deep Reinforcement Learning][18]
- [Morvan: Reinforcement Learning][19]
- [Reinforcement Learning: An Introduction][20]
- [Flood Sung: 智能单元][21]
- [MILA: Reinforcement Learning Summer School][22] 「[zhihu][23]」
 

## Coverage:

我们希望通过概念的讲解，论文的讲解，实际案例讲解三种方式来完成本系列文章。  
对于经典的算法(如DQN,A2C,A3C)，我们会详细介绍其原理以及一些实际的Demo(如 Flappy bird, Atari game)等等。对于与RL或者DRL相关的package(如openai-gym)等，我们也会进行相应的讲解。  

整个系列分为 强化学习 和 深度强化学习 两个部分。  
强化学习的部分我们会从最基本的概念开始，包括什么是RL，MDP,到MC方法，TD learning, Q learning。同时我们也会讲解 MCTS以及详尽介绍AlphaGo Zero。
进入深度强化学习部分后，我们将会着重在论文的分析以及实践上。我们会介绍自2013年DeepMind发布DQN以来至现在的所有经典算法和架构，并通过大量的Demo来进行实例讲解。当然，您也可以跳过强化学习的部分，直接从深度强化学习的部分开始学习。

### Reinforcement Learning Part:

 - [Introduction to Reinforcement Learning (强化学习简介)][24]
 - Markov decision process (马尔科夫过程)
 - Model-free Reinforcement Learning (模型无关的强化学习)
 - Integrating Learning and Planning
 - Policy Gradient
 - Exploration and Exploitation

### Deep Reinforcement Learning Part:

- Deep Q Network 
    - Playing Atari with Deep Reinforcement Learning
    - Human-level control through deep reinforcement learning
    - Demo 1 : Flappy Bird
    - Tutorial : OpenAI-gym tutorial
    - Demo 2 : Atari Game
- Introduction to AlphaGO Zero
    - Monte Carlo tree search
    - Mastering the game of Go without human knowledge
- Double DQN 
    - Deep Reinforcement Learning with Double Q-learning
    - Demo 1 : Flappy Bird
- Other improvements:
    - Prioritized Prioritized Experience Replay
    - Dueling Network Architectures for Deep Reinforcement Learning
    - Demo 1 : Flappy Bird
    - Demo 2 : Atari Game
- Deep Deterministic Policy Gradient
    - Deterministic Policy Gradient Algorithms
    - Continuous control with deep reinforcement learning
    - Demo 1 : OpenAI games
- A3C(A2C)
    - Asynchronous Methods for Deep Reinforcement Learning
    - Demo 1 : OpenAI games
- ACER
    - Sample Efficient Actor-Critic with Experience Replay
    - Demo 1: OpenAI games
- ACKTR
    - Scalable trust-region method for deep reinforcement learning using Kronecker-factored approximation
- Trust Region Policy Optimization
- Distributed Proximal Policy Optimization
    - Proximal Policy Optimization Algorithms
    - Emergence of Locomotion Behaviours in Rich Environments
- Rainbow
    - Rainbow: Combining Improvements in Deep Reinforcement Learning

如果您发现任何错误，或是有任何建议及意见，亦或是您希望加入本系列文章的撰写，请联系 [我们][25] ！


  [1]: http://cs229.stanford.edu/
  [2]: http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17.html
  [3]: https://cs.nju.edu.cn/zhouzh/zhouzh.files/publication/MLbook2016.htm
  [4]: http://ocw.nctu.edu.tw/course_detail.php?bgid=1&gid=1&nid=563#.WfcvbFtL-Ul
  [5]: http://cs231n.stanford.edu/
  [6]: http://cs224d.stanford.edu/
  [7]: http://www.deeplearningbook.org/
  [8]: https://github.com/exacity/deeplearningbook-chinese
  [9]: http://speech.ee.ntu.edu.tw/~tlkagk/courses_MLDS17.html
  [10]: https://www.tensorflow.org/
  [11]: https://web.stanford.edu/class/cs20si/
  [12]: https://github.com/aymericdamien/TensorFlow-Examples
  [13]: http://pytorch.org/
  [14]: https://github.com/hunkim/PyTorchZeroToAll
  [15]: https://keras.io/
  [16]: http://www0.cs.ucl.ac.uk/staff/D.Silver/web/Teaching.html
  [17]: http://icml.cc/2016/tutorials/deep_rl_tutorial.pdf
  [18]: http://rll.berkeley.edu/deeprlcourse/
  [19]: https://morvanzhou.github.io/tutorials/machine-learning/reinforcement-learning/
  [20]: http://incompleteideas.net/sutton/book/the-book.html
  [21]: https://zhuanlan.zhihu.com/intelligentunit
  [22]: https://mila.quebec/en/cours/deep-learning-summer-school-2017/
  [23]: https://zhuanlan.zhihu.com/p/28922147
  [24]: https://rl-tutorial.github.io/2017/11/02/intro-to-rl.html
  [25]: https://zhuanlan.zhihu.com/rl-tutorial