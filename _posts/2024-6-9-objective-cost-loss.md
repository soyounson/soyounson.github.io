---
layout: post
title: Objective function, Cost function, Loss function
---
### 목적함수 vs 손실함수 (objective function vs cost function), 둘의 차이점은?

머신러닝/딥러닝에 대한 책들을 살펴보면 모델 평가나 최적화 부분에서 목적 함수 (objective function)나 손실함수 (loss function, cost function, error function)가 빈번하게 사용된다. 하지만 글을 읽다보면 손실함수에 대하여 논하면서 어느 순간 목적 함수, *L*에 대하한 식을 기술하고 있는 경우가 종종 존재해서 둘이 동일한 개념인지 완전히 다른 개념인지 헷갈린다. 

결론부터 얘기하면 목적함수가 좀 더 포괄적이고 상위의 개념이다.  둘의 차이에 대하여 정리한 것을 인용하면, <span style="color:red"> 목적함수(obejctive function)</span>는 무엇인가를 최소화 (minimize) 혹은 (maximize) 하는 함수를 의미하고, <span style="color:blue"> 손실함수 (cost function, loss function, error function) </span> 란 무엇인가를 최소화 (minimize) 하는 함수라고 한다. 즉, <span style="color:blue"> 손실함수 (cost function, loss function, error function)</span>의 경우는 loss, error, cost를 최소화 하는 함수라고 볼 수 있다. 따라서 <span style="color:red">목적함수 (objective function)</span> 가 최소화(minimize)를 목적으로 한다면 <span style="color:red">목적함수 (objective function)</span>가 <span style="color:blue"> 손실함수 (cost function, loss function, error function)</span>와 같다고 볼 수 있다 [1,2]

> The function we want to <span style="color:cyan">minimize</span> or <span style="color:pink">maximize</span> is called the <span style="color:red">objective function</span>, or criterion. When we are <span style="color:cyan">minimizing</span> it, we may also call it the <span style="color:blue">cost function, loss function, or error function</span>.

## Table of Contents

- Objective function 
- Cost function vs Loss function vs Error function
- Reference 

## Objective function

그렇다면 목적함수라는 것은 정확히 무엇일까? 목적함수는 최적화 문제를 풀기 위한 함수이다 [1]. 따라서 이러한 목적함수는 최적화 방향이 최소화 시키느냐 최대화 시키느냐에 따라서 손실함수이기도 하고 그 반대이기도 하다 (특정 도메인에서 보상상함수 ( [reward function](https://en.wikipedia.org/wiki/Reward_function)), 이익함수 ([profit function](https://en.wikipedia.org/wiki/Profit_function)), 효용함수 ([utility function](https://en.wikipedia.org/wiki/Utility_function)), 적합도함수 ([fitness function](https://en.wikipedia.org/wiki/Fitness_function))) [3]. 이러한 목적 함수는 ML에서 훈련중 최적화시키는 모든 함수에 대한 가장 일반적인 용어이다 [1]. 이러한 목적함수에 대한 정의에 대하여 설명한 자료를 보면 아래와 같다 [2].

>  <span style="color:red">Objective Function</span> is the objective of the Linear Programming Problem as the name suggests. In linear programming or linear optimization, we use various techniques and methods to find the optimal solution to the linear problem with some constraints. The technique can also include inequality constraints as well. The objective function in Linear Programming is to optimize to find the optimum solution for a given problem.

여기서는 따로 다루진 않지만, 이러한 목적함수의 기울기 계산해서 최적화 문제를 푸는 것이 경사하강법 (gradient descent)이다. 

## Cost function vs Loss function vs Error function

<span style="color:blue"> 손실함수 (cost function, loss function, error function)</span> 혹은 비용함수 혹은 에러함수는 일반적으로 동의어 (**synonymous**)로 간주된다. 따라서 최적화 문제에서 손실을 최소화시키는 함수라고 본다 [3].

> In [mathematical optimization](https://en.wikipedia.org/wiki/Mathematical_optimization) and [decision theory](https://en.wikipedia.org/wiki/Decision_theory), a <span style="color:blue">loss function or cost function** (sometimes also called an error function)</span> is a function that maps an [event](https://en.wikipedia.org/wiki/Event_(probability_theory)) or values of one or more variables onto a [real number](https://en.wikipedia.org/wiki/Real_number) intuitively representing some "cost" associated with the event. An [optimization problem](https://en.wikipedia.org/wiki/Optimization_problem) seeks to minimize a loss function. 

하지만 이 세가지 함수를 좀 더 자세하게 구분하면, <span style="background-color:cyan">손실함수(loss function)</span> 혹은 <span style="background-color:cyan">오류함수 (error function)</span>는 단일 훈련 예제에 대한 것이고, <span style="background-color:Skyblue">비용함수 (cost function)</span> 는 전체 훈련 세트(또는 미니 배치 경사하강법의 경우 미니 배치)에 대한 것 이다. 따라서 비용함수가 손실함수나 오류함수 대비 좀 더 일반적인 함수라고 볼 수 있다. 좀 더 자세한 내용은 아래와 같다 [4].

> The loss function (or error) is for a single training example, while the cost function is over the entire training set (or mini-batch for mini-batch gradient descent). Therefore, a loss function is a part of a cost function which is a type of an objective function.
>
> - [Loss function](https://primo.ai/index.php?title=Loss)
>
>   is usually a function defined on a data point, prediction and label, and measures the penalty. For example:
>
>   - square loss l(f(xi|θ),yi)=(f(xi|θ)−yi)2, used in linear Regression
>   - hinge loss l(f(xi|θ),yi)=max(0,1−f(xi|θ)yi), used in SVM
>   - 0/1 loss l(f(xi|θ),yi)=1⟺f(xi|θ)≠yi, used in theoretical analysis and definition of accuracy 
>
> - Cost function
>
>    is usually more general. It might be a sum of loss functions over your training set plus some model complexity penalty (regularization). For example:
>
>   - Mean Squared Error MSE(θ)=1N∑Ni=1(f(xi|θ)−yi)2
>   - SVM cost function SVM(θ)=∥θ∥2+C∑Ni=1ξi (there are additional constraints connecting ξi with C and with training set)
>
> - Objective function
>
>    is the most general term for any function that you optimize during training. For example, a probability of generating training set in maximum likelihood approach is a well defined objective function, but it is not a loss function nor cost function (however you could define an equivalent cost function). For example:
>
>   - MLE is a type of objective function (which you maximize)
>   - Divergence between classes can be an objective function but it is barely a cost function, unless you define something artificial, like 1-Divergence, and name it a cost
>
> - Error function - [Backpropagation](https://primo.ai/index.php?title=Backpropagation); or automatic differentiation, is commonly used by the gradient descent optimization algorithm to adjust the [weight](https://primo.ai/index.php?title=Activation_Functions#Weights) of neurons by calculating the gradient of the [loss function](https://primo.ai/index.php?title=Loss). This technique is also sometimes called backward propagation of errors, because the error is calculated at the output and distributed back through the network layers. 



우선 각 함수들에 대한 concept을 정리하였고, 좀 더 자세한 부분은 추후 업데이트 예정이다. 



## Reference 

1. https://stats.stackexchange.com/questions/179026/objective-function-cost-function-loss-function-are-they-the-same-thing
1. [objective function] https://www.geeksforgeeks.org/objective-function/
1. [loss function, wikipedia] https://en.wikipedia.org/wiki/Loss_function
1. [objective function, loss function, cost function, error functio] https://primo.ai/index.php?title=Objective_vs._Cost_vs._Loss_vs._Error_Function
