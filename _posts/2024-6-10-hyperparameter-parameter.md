---
layout: post
title: Hyper parameter vs parameter
---
### Hyperparamter vs parameter, 우리가 튜닝해야 하는 것은?

머신러닝/딥러닝을 하는데 있어 Hyperparameter은 너무 익숙하다. 왜냐하면 hyperparameter tuning이 중요하다는 것은 항상 듣는 얘기이기 때문이다. 그렇다면 Hyperparameter은 무엇이고, parameter와 차이는 무엇일까?

요약하자면 <span style="color:gold"> parameter</span>은 모델 <span style="background-color:gold">내부 (internal) 구성</span>으로 학습 과정 중에서 데이터 기반으로 자동 조정되기 때문에 실무자가 설정해주는 값이 아닌 반면에, <span style="color:orchid"> hyperparameter </span>은 모델 <span style="background-color:orchid">외부 (external) 구성</span>으로 실무자가 설졍해주는 값이다. 예로 신경망에서 <span style="color:gold"> parameter</span>은 weight, bias이며, <span style="color:orchid"> hyperparameter </span>은 learning rate, batch size, number of hidden layer, number of neuron 등에 해당된다 [1]. 

> <span style="color:gold">Parameters</span> are derived from data, while <span style="color:orchid">hyperparameters</span> are set by the practitioner. In model, <span style="color:gold">parameters</span> are the core components that the model uses to make predictions. <span style="color:orchid">Hyperparameters</span> are the settings that dictate how the learning process occurs.

## Table of Contents

- Hyperparameter (초매개변수)
- Parameter (매개변수)
- Hyperparameter vs Parameter? 
- Reference 

## Hyperparameter (초매개변수)

<span style="color:orchid"> Hyperparameter </span> (하이퍼파라미터, 초매개변수)는 학습과정의 세부사항을 지정하는 값으로 앞서 설명하였듯 모델  <span style="background-color:orchid">외부 (external) </span>에서 받아오는 값이라고 할 수 있다. 머신러닝 프로젝트에서는 실무자, 데이터 사이언티스트 등이 설정해줄수도 있고, Grid search, Random search, Bayesian optimization 등을 통하여 최적의 값을 받아서 올수도 있다. 즉, 모델 입장에서는 <span style="background-color:orchid">외부 (external) </span> 들어오는 값이기에 학습과정 중에는 업데이트가 되거나 변하는 값들이 아니다. 

같은 맥락에서 **hyper**는 **top-level** 을 의미하며 이는 **hyper**parameter가 지정되어 모델 외부에서 들어옴에 따라 학습 과정이나 모델 매개변수들이 제어되기 때문이다 [2,3]. 

>  The prefix 'hyper_' suggests that they are **top-level** parameters that control the learning process and the model parameters that result from it.

## Parameter (매개변수)

<span style="color:gold"> Parameter </span>(파라미터, 매개변수)는 아래와 같이 다양한 의미가 있지만 머신러닝에서 사용되는 의미는 mathematical definition인 특정 상황에 맞게 값이 선택되고 다른 가변 수량과 관련하여 표현될 수 있는 수량이라고 볼 수 있다. 즉, 상황에 맞게 모델 <span style="background-color:gold">내부 (internal)</span>에서 값이 정해지므로 머신러닝 프로젝트에서는 학습과정 중에 최적의 솔루션을 얻기 위하여 계속적으로 업데이트 가능한 값이다 [5].

>**TECHNICAL**
>
>a numerical or other measurable factor forming one of a set that defines a system or sets the conditions of its operation.
>
>**MATHEMATICS**
>
>a quantity whose value is selected for the particular circumstances and in relation to which other variable quantities may be expressed.
>
>**STATISTICS**
>
>a numerical characteristic of a population, as distinct from a statistic of a sample.

<span style="color:gold">parameter </span>의 어원을 확인하면 아래와 같다. 

> **para-** : [Greek] beside
>
> **metron**: [Greek] measure 

## Hyperparameter vs Parameter? 

그렇다면 머신러닝 프로젝트를 진행하는데 있어서 우리가 신경써야 하는 것들은 어떤 것일까? 둘의 차이에 대하여 머신러닝에서의 쓰임에서 표로 비교하면 아래와 같다 [1,6,7]. 

| <span style="color:gold"> Parameter </span>          | <span style="color:orchid"> Hyperparameter </span>           |
| ---------------------------------------------------- | ------------------------------------------------------------ |
| internal                                             | Outernal                                                     |
| During training (learned from data)                  | before training                                              |
| Model-spefic                                         | Model-independent                                            |
| Optimization algorithms (Gradient Descent, Adam etc) | Hyperparameter tuning (Grid search, Bayesian optimization)   |
| not set manually                                     | set manually (using heuristics)                              |
| how the model will perform on unseen data            | how efficinet and accurate the optimization process is in the estimating parameters |

여기서 실질적으로 실무자나 데이터사이언티스트가 신경써야 하는 것은 <span style="color:gold">parameters</span>와 <span style="color:orchid">hyperparameters</span> 둘 다 해당한다. 단, <span style="color:orchid">hyperparameters</span>의 경우 그 값들을 직접 지정해주는 것이고 <span style="color:gold">parameters</span>의 경우 적절한 optimization algorithms을 지정해줌으로써 모델이 학습되는 부분에서 최적의 값들을 찾도록 해주는 것이다. 즉,  <span style="background-color:orchid">직접적인 값 (direct value)</span>들을 지정해주느냐 (<span style="color:orchid">hyperparameters</span>) 혹은  <span style="background-color:gold">간접적으로 값</span>들이 지정되도록 해주느냐 (<span style="color:gold">parameters</span>)의 차이 일 뿐이지 모두 실무자나 데이터사이언티스트가 신경 써야 하는 것은 맞다고 생각한다. 

더 알게되는 부분이 있다면 추후 업데이트 할 예정이다. 

## Reference 

1. https://www.linkedin.com/pulse/parameter-vs-hyperparameters-machine-learning-sanjay-kumar-mba-ms-phd/
1. [hyperparameter, wikipedia] https://en.wikipedia.org/wiki/Hyperparameter_(machine_learning)
1. https://towardsdatascience.com/parameters-and-hyperparameters-aa609601a9ac
1. [parameter, wikipedia] https://en.wikipedia.org/wiki/Parameter
1. [Oxford Languages](https://languages.oup.com/google-dictionary-en) 
1. https://www.geeksforgeeks.org/difference-between-model-parameters-vs-hyperparameters/
1. https://machinelearningmastery.com/difference-between-a-parameter-and-a-hyperparameter/
