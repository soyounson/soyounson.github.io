---
layout: post
title: Occam's razor

---

## "오컴의 면도날 법칙 (Occam's razor or Ockham's razor)"

머신러닝에서 거론되는 **오컴의 면도날 법칙** 이란, **simple is the best** 를 의미한다. 이는 동일한 성능을 같은 간단한 모델과 복잡한 모델이 있을때 간단한 모델을 선택하는 것으로 **과적합 (overfitting)** 을 방지하고 머신러닝의 **일반화 (generaliazation)** 와 일맥상통한다. 단, 여기서 가장 간과하지 말아야 하는 부분은 **동일한 성능** 인 조건에만 법칙이 만족된다는 것이다. 
우선, **오컴의 면도날 법칙** 및 머신러닝에서 사용되는 이유에 대해서 좀 더 자세하게 살펴보도록 하자. 


## Table of Contents

- Ockham's razor
- Ockham's razor (or Occam's razor) in Machine Learning
- Simplicity
- Reference 

## Ockham's razor (or Occam's razor)

우선, Ockham은 14세기 영국 살았던 프란체스코 수도사로 scholastic philosopher 이자 theologian 였다[1]. 그가 처음으로 주장한 내용을 정리하면, 어떤 일이 발생했을 때 가장 적은 추측을 사용한 방법이 더 올바를 수 있다고 하였다. 단, 여기서 중요한 가정이 있는데, 이건 적은 추측 및 단순한 설명을 한 것과 많은 추측 및 복잡한 설명 둘 다 똑같이 잘 작동할 때에만 적용된다는 것이다 [2]. 아래는 이에 대한 설명을 의미한다. 

>[William of Ockham](https://simple.wikipedia.org/wiki/William_of_Ockham), a [Franciscan](https://simple.wikipedia.org/wiki/Franciscan) [friar](https://simple.wikipedia.org/wiki/Friar) who studied [logic](https://simple.wikipedia.org/wiki/Logic) in the [14th century](https://simple.wikipedia.org/wiki/14th_century), first made this principle well known. In [Latin](https://simple.wikipedia.org/wiki/Latin_language) it is sometimes called **lex parsimoniae**, or "the [law](https://simple.wikipedia.org/wiki/Law) of briefness". William of Ockham supposedly (see below) wrote it in Latin:
>
>- *Entia non sunt multiplicanda praeter necessitatem.
>
>This translates roughly:
>
>- *More things should not be used than are necessary.*
>
>- *Plurality should not be posited without necessity.* 
>
>This means if there are several possible ways something might have happened, the way which uses the fewest guesses is probably the correct one. However, Occam's razor only applies when the simple explanation and complex explanation both work equally well. If a more complex explanation does a better job than a simpler one, then you should use the complex explanation.

좀 더 일반적인 관점에서 설명하면 아래와 같다. 즉, 적은 가정을 기반으로 경우가 더 많은 가정을 기반으로 하는 것보다 상대적으로 더 정확하고 설명력이 있다는 것이다. 따라서 **사고의 절약 원리**라고도 부른다. 

> **Occam's razor** (or **Ockham's razor**) is a [principle](https://simple.wikipedia.org/wiki/Principle) from [philosophy](https://simple.wikipedia.org/wiki/Philosophy). Suppose an event has two possible [explanations](https://simple.wikipedia.org/wiki/Explanation). The explanation that requires the fewest assumptions is usually correct. Another way of saying it is that the more [assumptions](https://simple.wiktionary.org/wiki/assumption) you have to make, the more unlikely an explanation. Occam's razor applies especially in the [philosophy of science](https://simple.wikipedia.org/wiki/Philosophy_of_science), but also appears in everyday life.

즉, 어떠한 현상을 설명하는데 (어떠한 분야라도 상관없다) 더 많은 가정을 하게 된다면 이는 제약 조건이 많아지고 더 복잡해진다는 것을 의미한다. 따라서 동일한 결과를 도출한다면 간단한 가정으로 간단하게 설명 가능한 것이 더 설명력이 있고, 제약 조건이 적다는 것이다. 

## Why razor? 

그렇다면 왜 **면도날 (razor)** 라는 사용 한 것일까? 여기서 사용한 면도날은 철학적 비유 (philosophical metaphors)라고 볼 수 있다. 즉, 철학에서 면도칼은 현상에 대한 있을 법하지 않은 설명을 제거하거나 불필요한 행동을 피할 수 있게 해주는 원칙 또는 경험 법칙이다 [3,4]

>In philosophy, a razor is a principle or a rule of thumb, that allows for the elimination (the “shaving off”) of unlikely explanations for a phenomenon.
>
>A philosophical razor is not an unbreakable law or rule, it is not always right 100% of the time, but it is right more often than not, and is therefore a useful mental shortcut that allows you to make decisions and solve problems quicker and easier.

따라서 **오컴의 면도날 법칙**이 과학자들이 현상에 대하여 특정 이론 모델 (theoretical models)을 만들 때, 불필요한 가정을 **"깎아내다 (shaving away)"** 것을 의미한다 [5]. 즉, 앞서 설명한 듯 간단한 것을 선택하는데 이를 위해서는 불필요한 가정이나 조건들을 깎아내고 현상에 대한 근본적이고 핵심적인 부분만을 고려한다는 의미로 해석이 가능하다. 이에 대하여 아래 **simplicity**에서 좀 더 다룰 예정이다. 

> Occam's razor is used as a heuristic, or "rule of thumb" to guide scientists in developing theoretical models. The term "razor" refers to the "shaving away" of unnecessary assumptions when distinguishing between two theories. 

## Ockham's razor (or Occam's razor) in Machine Learning 

이러한 오컴의 면도날이 머신러닝에서 거론되는 이유는 아래와 같다 [6].

>  Occam's Razor is a principle that likes simplicity.It says that the simplest solution is usually the best one. In machine learning, this means that **if we have two models that work about as well as each other, we should choose the simpler one**.

그렇다면 왜 머신러닝에서 simple model 을 선택하라는 **오컴의 면도날 법칙 (Occam's razor principle)**이 거론되는 걸까? 이는 **(1) 복잡한 모델이 오버피팅이 될 가능성이 훨씬 높고 (2) 간단한 모델 일수록 더 설명 가능하고 이해하기 쉽기 때문이다.**

> **Why is Occam’s Razor so useful in machine learning?** It helps us **avoid overfitting**, which is when a model works well on the training data but not on new data. By choosing simpler models, we make sure our model learns the pattern in the data, not the noise. Also, simpler models are usually easier to understand and explain, which is important in many industries.

특히, 귀납적 학습의 머신러닝 분야에서는 오컴의 면도날이라 불리는 기본 법칙이 통용되고 있다 [7]. 그렇다면, 여기서 머신러닝에서 **귀납적 학습 (Inductive learning)** 과 **연역적 학습 (deductive learning)**의 차이는 무엇일까 [8,9]?

>  Inductive and deductive machine learning are two different approaches used to teach computers to recognize patterns and make predictions, but they operate in distinct ways. **Inductive machine learning starts with specific examples and then generalizes to broader principles**. It's like learning from specific cases and then applying that knowledge to similar situations. On the other hand, **deductive machine learning begins with general principles or rules and then applies them to specific cases to make predictions or decisions.**  It's like starting with a set of rules and then using them to classify or make decisions about specific instances.

즉, 머신러닝에서 **귀납적 학습**의 경우 데이터를 기반으로 특정 패턴이나 규칙등을 추론하고 이를 기반으로 일반화된 법칙이나 원리 등을 찾는 것이고, **연역적 학습**의 경우는 일반적인 법칙이나 원리를 특정 사례에 적용해서 예측이나 결정에 도달하는 것이라고 볼 수 있다. 일반화된 설명을 빌리면 [7]

> - **귀납적 학습**은 복수의 구체적인 사실로부터 학습 결과인 구체적인 지식을 이끌어 냄. 
> - **연역적 학습**은 기초적인 추상적 개념에서 구체적인 지식을 도출하면서 학습을 진행함.

따라서 앞서 귀납적 학습의 머신러닝 분야의 경우 똑같은 결과와 성능이 나온다면 간단한 모델 (혹은 법칙? 원리?)을 사용하는 것이 일반화 관점에서도 귀납적 논리 전개 방식을 따르는 것이 된다. 



## Simplicity 

그렇다면 머신러닝에서 **simplicity**가 왜 중요할까? 이는 머신러닝이라는 분야뿐만 아니라 물리학, 공학 나아가 현실 세계에서도 중요하다. 사람들은 왜 **search for simplicity** 하는 걸까 [10]?

> Physics aims to uncover fundamental laws and principles that govern the behavior of the physical world. These laws are often expressed in the form of concise mathematical equations, representing simple and elegant relationships. **The pursuit of simplicity means seeking the underlying patterns and unifying principles that can explain a wide range of phenomena.** Occam's Razor: Occam's Razor is a principle in philosophy that suggests the simplest explanation is often the best one. **Physics embraces this principle by striving to find the simplest explanations that account for observed phenomena.** By seeking simplicity, physicists aim to minimize unnecessary complexity and assumptions, leading to more elegant and comprehensive theories. Simple theories often possess greater predictive power. **When the fundamental principles of physics are expressed in simple terms, they can be applied to a wide variety of situations and used to make accurate predictions.** By reducing complexity, physicists can develop models that are easier to understand and apply, making it possible to predict and explain phenomena across different scales and contexts.

위에서 설명하였듯 simplicity를 추구한다는 것은 광범위한 현상들에 적용 할 수 있고, 설명 가능한 근본적이고 핵심적인 (fundamental) 패턴이나 법칙을 찾고, 이를 통하여 정확한 예측이 가능하도록 하는 것이다. 

좀 더 풀어서 설명한다면 현실 세계에 광범위한 현상 (*X0, y0*) 들이 발생하는데 이들을 설명 할 수 있는 무언가 가 필요하다. 이를 위하여 우리는 간단하지만 (simple) 통합적이고 (comprehensive) 일반적이며 (general) 이고 탄탄한 (robust) 한 법칙 *f(X)*이 필요하다. 이를 기반으로 기존에 우리가 관측한 현상들에 대하여 설명 가능하고 나아가서 이를 기반으로 어떠한 조건 (*X1*) 에서 새로운 결과 (*y1*) 을 예측할 수 있는 것이다. 

이는 머신러닝의 **일반화 (generalization)**과도 일맥상통하는 것으로 이러한 일반화 성능을 저하시키는 것이 **과적합 (overfitting)**이므로 유의해야 한다는 것은 모두가 아는 사실 일 것이다. 

우리는 가능하다면 간단하게 만들려고 한다. 이것은 이해 가능하고, 설명 가능하고, 일반화 및 통합화가 가능하기 때문이다. 그리고 그러한 간단한 것은 결국은 현상의 가장 핵심적이고 근본적인 것을 나타낸다고 볼 수 있다. 따라서 간단한 것은 쉬우면서도 어려운 것이라 생각한다. 그래서 재밌는 것 같다. 



## Reference 

1. https://simple.wikipedia.org/wiki/William_of_Ockham
1. https://simple.wikipedia.org/wiki/Occam%27s_razor
1. https://hawthornrotary.org.au/stories/what-is-a-philosophical-razor
1. https://en.wikipedia.org/wiki/Philosophical_razor
1. https://www.aaas.org/taxonomy/term/10/origin-and-popular-use-occams-razor#:~:text=Occam's%20razor%20is%20used%20as,when%20distinguishing%20between%20two%20theories.
1. https://vitalflux.com/occams-razor-in-machine-learning-examples/
1. 기초부터 배우는 인공지능 성안당 
1. https://www.linkedin.com/pulse/difference-between-inductive-machine-learning-deductive-korvage-dtoqc/
1. https://wikidocs.net/167323
1. https://brainly.com/question/33378293
