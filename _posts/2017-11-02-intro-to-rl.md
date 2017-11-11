---
layout: post
title: Introduction to Reinforcement Learning
---

* 目录 
{:toc}

## 0. 写在前面

你可能是一位正在学习机器学习的本科生，刚转入深度学习研究的硕士生，  
你可能是一位数学爱好者，人工智能爱好者，深度学习爱好者，  
或许是横扫棋坛的AlphaGo点燃了你对强化学习的热情，  
或许是TI7上同打败Dendi的影魔(OpenAI)点燃了你对强化学习的激情。  

我们希望你在进行强化学习之前对机器学习，深度学习有一定的了解，  
或是在大学/研究生 阶段 修过诸如人工智能，博弈论，机器学习，深度学习等课程。  
虽然这不是必须，但会对强化学习的学习有很大的帮助。

如果你没有任何机器学习(深度学习)的基础，  
我们希望你先花一点时间学习 [**主页**][1] 中推荐相关的课程(书籍)。 

下面，让我们正式打开强化学习的大门！  

我们希望你在读完本文后能明白如下几个问题：

- 什么是强化学习
    - 从感性上认识它
    - 从定义的角度理解它
- 它和传统的监督学习，无监督学习，有何区别
- 什么是深度强化学习


## 1. 什么是强化学习

---

同往常一样，我们试图弄明白第一个问题：**什么是强化学习 (Reinforcement Learning)**？   
在给它下定义之前，我们希望通过几个简单的例子，让你对它有一个直观而又感性的了解。

### 1.1 游戏机的诱惑

回想一下你的小学时期，每次考试后，若你拿了100分，将得到父母的奖励(获得1小时玩游戏的时间)；  
反之，若你没能拿到满分，不但失去了玩游戏的时间，还会受到父母的责骂。

小孩子的天性都是贪玩的，刚开始你可能不太在意，仍然不好好学习。  
但随着考试的不断增加，你发现你的游戏时间越来越少，而且还屡次受到责骂；  
你终于开始奋发图强，努力学习，成绩不断提高，
最后，你做到了每次考试都拿满分，也因此获得了大量的游戏时间，  
给你一个学习的动力，达成目标后，不仅自己开心，父母也非常满意，可谓皆大欢喜。

![][2]

提炼一下，你的目的是尽可能多地获得玩游戏的时间，而条件就是 ——「考取100分」，    
为达到这个目的，你可能会自发地不断刷题，总结解题技巧，与同学交流讨论。  
在这个过程中，你不断强化自己，最终达到自己的目标 —— 「愉快地玩游戏」。

是的，这其实就是一个典型的强化学习。

### 1.2 沙鼠の迷宫之旅

接下来我们看一个短片，它描述了一个沙鼠是如何通过不但训练从而快速走出迷宫的。  

<video src="/videos/1-1.mp4" width="95%" height="95%" controls>
Your browser does not support the video tag.
</video>

从短片中我们可以看到，在陌生的迷宫环境中，小沙鼠不断地探索迷宫的出口。  
起初它无法确定正确的方向，所以随机地进行尝试，成功找到出口可能会花去很长的时间。  
而在小沙鼠不断尝试的过程中，找到出口的时间也逐渐减少。  
到最后，它只需要不到10秒的时间，就能走出迷宫。  

没错，这也是一个强化学习的例子。

### 1.3 打砖块游戏


我们再来看一个 Google DeepMind 用强化学习来玩打砖块游戏的短片：

<video src="/videos/1-2.mp4" width="95%" height="95%" controls>
Your browser does not support the video tag.
</video>

可以看到，刚开始AI什么都不会，只是随机地乱移动。
而通过不断训练后，AI便能够很好进行游戏了。  

这是一个经典的深度强化学习的例子，我们在后续的文章中，将会给出详细介绍。  

### 1.4 试着定义一下强化学习

先来看Sutton在《[Reinforcement Learning:An Introduction][3]》中的定义：

> Reinforcement learning is learning what to do — how to map situations to actions — so as to maximize a numerical reward signal. The learner is not told which actions to take, but instead must discover which actions yield the most reward by trying them. —— Sutton

强化学习就是学习如何去做，即如何将状态和行动对应起来，从而使得最后的奖励最大。

为了得到更多玩游戏的时间，我们绞尽脑汁努力提高学习成绩。    
为了逃出迷宫，小沙鼠想方设法熟悉环境。  
我们并不太在意中间过程究竟是用了何种方法，但是我们都有一个既定的目标，朝着这个目标不断努力。  

强化学习往往都具有目标导向的特点，我们往往会采用一些**试错(trial and error)**的方法，不断去尝试与探索，在不断同环境的交互中，使得我们的目标结果或者是得到的回报最大化。  


下面介绍几个必要的概念：

- **Agent**  
有地方把它翻译为智能体，有地方则是翻译为代理，但中文翻译起来都有些许别扭，所以我们就还叫它Agent。结合上面的例子，「游戏机的诱惑」中的agent的就是我们自己(或者说我们打大脑)，「沙鼠の迷宫之旅」中，agent是小沙鼠，而「打砖块游戏」中的agent则是控制游戏的AI程序。

- **Environment - 环境**  
这个概念比较好理解，就是我们所理解的“环境”,结合上面的例子，「游戏机的诱惑」中的环境的就是这个世界，「沙鼠の迷宫之旅」中，环境则是整个迷宫，而「打砖块游戏」中的环境便是拥有这个游戏的游戏机。

- **State - 状态**  
还是用「打砖块游戏」来举例，当前状体即为游戏机显示出来的画面

- **Action - 动作**  
对于给定的一个状态，我们可能会有若干个可以选择的动作。  
比如「打砖块游戏」中我们可以选择往左边移动，往右边移动，或者不移动等。  

- **Reward - 奖励**  
在「打砖块游戏」中，我们希望尽可能地拿到高分，而每一次击中砖块，都会得到相对应的分数，这就是Reward，也是强化学习和其他机器学习问题最不同的地方。

![][4]



而我们强调如何基于**环境(environment)**而做出**行动(action)**，以取得最大化的**预期利益(reward)**。
换句话说，我们希望在给定的状态(state)下做出最佳的决策，使得最后获得的总回报(reward)最大。  



## 2. 强化学习与机器学习

---

如下图所示，强化学习是机器学习中的一种。  
我们知道监督学习(SL)往往是通过大量的有标注的训练集来对模型进行训练(最常见的就是图片分类问题)，而非监督学习(UL)则往往在寻找给定数据间的某些联系(比如分群问题)。  
强化学习(RL)则是通过不断与环境交互来进行学习。它既不是监督学习，也不是非监督学习。      

![][5]

总体来说，RL与其他机器学习算法不同的地方在于：

 - No supervisor, only a reward signal (没有监督者，只有一个reward信号)
 - Feedback is delayed, not instantaneous (反馈是延迟的，不是立即生成的)
    - 比如打砖块是打到了砖块才会有分数，在球飞行的过程中都是没有reward的 
 - Time really matters (时间具有重要的意义)
 - Agent’s actions affect the subsequent data (agent的行为会影响之后一系列的data)
 - RL is learning from interaction. (RL是通过与环境的交互来进行学习的)
 - RL does not rely on examples of correct behavior.
    - 换句话说，RL是不需要像SL那样大量有标注的training data的 
 - RL is trying to maximize a reward signal, instead of trying to find hidden structure.

与此同时，强化学习的问题往往也会涉及多个领域，多个学科，它充满了趣味，也充满了挑战。



## 3. 深度强化学习

---

随着软硬件的飞速发展，深度学习(Deep Learning)已经成为机器学习领域中炙手可热的研究方向。 其中包括了计算机视觉(Computer Vision),自然语言处理(Natural Language Processing)等等。  

如果我们将强化学习和深度学习结合起来呢？ 对，它就是深度强化学习。  
Google DeepMind在NIPS 2013上发表《Playing Atari with Deep Reinforcement Learning》一文，首次提出了深度强化学习这一概念。  
此后它们与2015年在Nature上发表了文章《Human-level control through deep reinforcement learning》，揭开了深度强化学习的新篇章。  
2016年，DeepMind在Nature上发表文章《Mastering the game of Go with deep neural networks and tree search》,同年AlpahGo以4：1的绝对优势战胜了围棋世界冠军李世石，更是将深度强化学习推上了顶点。越来越多的深度强化学习的爱好者们都涌入这股洪流。  
2017年，OpenAI开发的Dota2 AI在TI7上击败了世界级选手Dendi。而DeepMind也将战略重心转向了星际争霸2。

当然，不仅仅是游戏，深度强化学习也被用在诸如机器手臂的训练，无人驾驶汽车的训练上，它已经成为深度学习领域又一大热门研究方向！

## 4. 写在后面

正如开头所说，本篇文章的目的是希望你对强化学习有一个基本的认识，它不同于需要标注数据的监督学习，也不同于寻找数据间联系的非监督学习，它往往是目标导向的，在与环境的交互过程中进行学习。对，它就是特殊的强化学习。

在下篇文章中，我们将介绍马尔可夫决策过程(MDP)，它是强化学习的基础，同时也是必须掌握的核心部分。


  [1]: https://rl-tutorial.github.io/
  [2]: /images/1-1.png
  [3]: http://incompleteideas.net/sutton/book/bookdraft2017nov5.pdf
  [4]: /images/1-2.png
  [5]: /images/1-3.png