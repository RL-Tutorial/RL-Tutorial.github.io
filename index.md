---
layout: home
---

Hello, everyone. Thanks for visiting our website.   
This website serves as the guide and introduction to (Deep) Reinforcement Learning for RL beginners.  

## For beginners:

我们希望您在阅读本系列文章前已接触或学习过(但非必需)如下课程，书籍以及框架：

 - 数学部分：
    - [Linear Algebra Review and Reference][1]
    - [Review of Probability Theory][2]
 - 机器学习部分：
    - [CS229: Machine Learning][3]
    - [Hung-yi Lee: Machine Learning][4]
    - [Yuh-Jye Lee: Machine Learning][5]
    - [周志华: 机器学习][6]
 - 人工智能部分： 
    - [UC Berkeley: CS188 Artificial Intelligence][7]
    - [CS221: Artificial Intelligence: Principles and Techniques][8]
 - 深度学习部分：
    - [CS231n: Convolutional Neural Networks for Visual Recognition][9] 「[bilibili][10]」
    - [CS224d: Deep Learning for Natural Language Processing][11]
    - [Hung-yi Lee:Machine Learning and having it deep and structured][12]
    - [Ian Goodfellow: Deep Learning][13]   「[chinese version][14]」
 - 深度学习框架部分：
    - [TensorFlow][15]
        - [CS 20SI: Tensorflow for Deep Learning Research][16]   
        - [aymericdamien/TensorFlow-Examples][17]
    - [PyTorch][18] 
        - [PyTorchZeroToAll][19] 
    - [Keras][20] 

若您没有任何机器学习(深度学习)的基础，我们希望您先花一点时间学习相关的课程(书籍)。   
若您没有接触过上述深度学习框架，我们也希望您先花一些时间来学习它。   
上面我们给出了兴许适合您学习的人工智能/机器学习/深度学习教程。  
若本系列文章不符合您的味口，您还可学习如下 强化学习 的相关教程：  

- [Dave Silver: Reinforcement Learning][21] 「[chinese translation][22]」
- [Dave Silver —— Tutorial: Deep Reinforcement Learning][23]
- [CS 294: Deep Reinforcement Learning][24]
- [CS234: Reinforcement Learning][25]
- [CMU 10703: Deep Reinforcement Learning and Control][26] 
- [Morvan: Reinforcement Learning][27]
- [Reinforcement Learning: An Introduction][28]
- [Flood Sung: 智能单元][29]
- [MILA: Reinforcement Learning Summer School][30] 「[zhihu][31]」
 

## Tutorial Coverage:

我们希望通过概念的讲解，论文的讲解，实际案例讲解三种方式来完成本系列文章。  
对于经典的算法(如DQN,A2C,A3C)，我们会详细介绍其原理以及一些实际的Demo(如 Flappy bird, Atari game)等等。  
对于与RL或者DRL相关的package(如openai-gym)等，我们也会进行相应的讲解。  

整个系列分为 强化学习 和 深度强化学习 两个部分。  
强化学习的部分我们会从最基本的概念开始，包括什么是RL，MDP,到MC方法，TD learning, Q learning。  
当然在这一部分也会涉及到与DRL有关的知识。同时我们也会讲解 MCTS以及详尽介绍AlphaGo Zero。  
深度强化学习部分，将会着重在论文的分析以及实践上。  
我们会介绍自2013年DeepMind发布DQN以来至现在的所有经典算法和架构，并通过一些的Demo来进行实例讲解。  
当然，您也可以跳过强化学习的部分，直接从深度强化学习的部分开始学习，或者两个部分交叉进行学习。  
不管怎样，希望我们的文章能够给您些许帮助！    

### Reinforcement Learning Part:

 - [Introduction to Reinforcement Learning][33]
 - Markov decision process
    - Markov Property
    - Markov Process
    - Markov Reward Process (MRP)
    - Markov Decision Process (MDP)
    - Partially Observable Markov Decision Process (POMDP)
 - Model-free Reinforcement Learning
    - Model-free prediction
        - Monte-Carlo (MC) Learning
        - Temporal Difference (TD) Learning
    - Model-free control
        - On-Policy Learning
        - Off-Policy Learning
 - Value Function Approximation 
 - Policy Gradient
 - Model-Based Reinforcement Learning
 - Others
    - Exploration and Exploitation
    - Multi-Armed Bandits 
    - Monte Carlo tree search
    - Introduction to AlphaGO Zero

### Deep Reinforcement Learning Part:

- Value-based
    - (DQN) Deep Q Network 
        - [Playing Atari with Deep Reinforcement Learning][34]
        - [Human-level control through deep reinforcement learning][35]
        - Demo 1 : Flappy Bird
        - Tutorial : OpenAI-gym tutorial
        - Demo 2 : Atari Game
    - Other improvements:
        - [(DDQN) Deep Reinforcement Learning with Double Q-learning ][36]
        - Prioritized Prioritized Experience Replay
        - Dueling Network Architectures for Deep Reinforcement Learning
        - Demo 1 : Flappy Bird
        - Demo 2 : Atari Game
- Actor-Critic
    - (DDPG) Deep Deterministic Policy Gradient 
    - (A3C) Asynchronous Methods for Deep Reinforcement Learning
    - (ACER) Sample Efficient Actor-Critic with Experience Replay
    - (ACKTR) Scalable trust-region method for deep reinforcement learning using Kronecker-factored approximation
    - Demo: Atari Game
- More
    - (TRPO) Trust Region Policy Optimization
    - (DPPO) Distributed Proximal Policy Optimization
        - Proximal Policy Optimization Algorithms
        - Emergence of Locomotion Behaviours in Rich Environments
    - Rainbow: Combining Improvements in Deep Reinforcement Learning


如果您发现任何错误，或是有任何建议及意见，亦或是您希望加入本系列文章的撰写，请联系 [我们][32] ！





  [1]: http://cs229.stanford.edu/section/cs229-linalg.pdf
  [2]: http://cs229.stanford.edu/section/cs229-prob.pdf
  [3]: http://cs229.stanford.edu/
  [4]: http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17.html
  [5]: http://ocw.nctu.edu.tw/course_detail.php?bgid=1&gid=1&nid=563#.WfcvbFtL-Ul
  [6]: https://cs.nju.edu.cn/zhouzh/zhouzh.files/publication/MLbook2016.htm
  [7]: http://ai.berkeley.edu/course_schedule.html
  [8]: http://web.stanford.edu/class/cs221/
  [9]: http://cs231n.stanford.edu/
  [10]: http://www.bilibili.com/video/av13260183/index_1.html
  [11]: http://cs224d.stanford.edu/
  [12]: http://speech.ee.ntu.edu.tw/~tlkagk/courses_MLDS17.html
  [13]: http://www.deeplearningbook.org/
  [14]: https://github.com/exacity/deeplearningbook-chinese
  [15]: https://www.tensorflow.org/
  [16]: https://web.stanford.edu/class/cs20si/
  [17]: https://github.com/aymericdamien/TensorFlow-Examples
  [18]: http://pytorch.org/
  [19]: https://github.com/hunkim/PyTorchZeroToAll
  [20]: https://keras.io/
  [21]: http://www0.cs.ucl.ac.uk/staff/D.Silver/web/Teaching.html
  [22]: http://list.youku.com/albumlist/show/id_49376145.html
  [23]: http://icml.cc/2016/tutorials/deep_rl_tutorial.pdf
  [24]: http://rll.berkeley.edu/deeprlcourse/
  [25]: http://web.stanford.edu/class/cs234/index.html
  [26]: https://katefvision.github.io/
  [27]: https://morvanzhou.github.io/tutorials/machine-learning/reinforcement-learning/
  [28]: http://incompleteideas.net/sutton/book/the-book.html
  [29]: https://zhuanlan.zhihu.com/intelligentunit
  [30]: https://mila.quebec/en/cours/deep-learning-summer-school-2017/
  [31]: https://zhuanlan.zhihu.com/p/28922147
  [32]: https://zhuanlan.zhihu.com/rl-tutorial
  [33]: {{ site.BASE_PATH }}/2017/11/02/intro-to-rl.html
  [34]: {{ site.BASE_PATH }}/2017/12/03/dqn.html
  [35]: {{ site.BASE_PATH }}/2017/11/04/dqn2.html
  [36]: {{ site.BASE_PATH }}/2017/12/08/ddqn.html
