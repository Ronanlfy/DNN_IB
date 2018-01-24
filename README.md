# Deep learning and communication theory

explain information flow in DNN via information theory, information bottleneck

## Getting Started

### Literature Review

- 2018/01/22-23. **The information bottleneck method** Naftali Tishby, Fernando C. Pereira, and William Bialek1

Well explain Blahut-Arimoto algorithm and the information bottleneck. 

- 2018/01/24 **Deep Learning and the Information Bottleneck Principle** Naftali Tishby and Noga Zaslavsky1

Connect DNN with IB, any DNN can be quantified by the mutual information bewteen hidden layers and input/output variables. What IB tries to do, is to find a maximally compressed mapping of the input variable that preserves as much as possible the inofrmation on the output variable. 

Maximally compression/lower complexity --> minimize  *I(X;X')*

Preserves information on the output/better generalization --> the constraints on *I(X',Y)*

Hence it becomes a Lagrnginan problem;
*L[p(x'|x)] = I(X;X') - beta x I(X',Y)*

<img width="1015" alt="ib" src="https://user-images.githubusercontent.com/23377680/35342163-a992354a-0127-11e8-99f6-f33ceed48b31.png">

*D_IB = I(X;Y|X'), R = I(X;X')* Larger R indicates high complexity/lower layers, larger D_IB means high distortion/higher layers. Each points on the black curve stands for a unique beta (slope is the negative inverse of beta).
