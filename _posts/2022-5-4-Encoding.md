---
layout: post
title: Categorical Variables Encoding
---

우선 Encoding에 대하여 자세하게 이해하기에 앞서, 내가 가장 궁금했던 부분은 목적 (purpose)였다. 

물론, Encoding을 해야하는 목적에 대하여 자세하게 인지하고 있다면 더할 나위없이 좋겠지만, 가끔 우리는 이유도 모른채 방법론을 찾는 경우가 있다.

나 또한 그랬다. 같이 일하는 coworker가 Categorical variable을 처리하기 위해 one-hot encoding을 해야한다고 해서 무작정 찾아서 업무를 진행하려 했지만 이해가 가지 않아서 찾아보게 되었다. 


사실 Encoding 방법은 엄청 많다. googling만해도 여러개의 Encoding 방법들이 sample code와 함께 잘 정리되어 있고, 이를 갖다가 쓰는 것은 매우 쉽다. 하지만, 가장 중요한 부분은 やっぱり (역시나) "Why?"같다. 

물론, 꼭 알 필요는 없을 수도 있지만, 사실 이걸 정확하게 이해하지 못한다면 이번 문제는 풀 수 있지만, 다음번에 조금 다른 문제가 주어졌을때 과연 내가 Endoding을 생각해 낼 수 있을까? 아니면 과연 Encoding을 적용할 수 있을까가 우리의 관심사 일거라고 생각한다. 

아무튼, 나한테 중요한 것은 지금 right now 이 문제를 푸는 것이 아니라 앞으로 다양한 문제를 푸는 것일테니 말이다.

자, 서론은 여기까지!



그래서 categorical data는 encoding을 해줘야 한다. 그 이유에 대해서 살펴보고, 어떠한 방법을 고려해서 "내가 갖고 있는 문제"를 잘 풀수 있을지 생각해보려 한다. 아주 자알!



-----------------------------------------------------------------------

☾ Table of contents

☺︎ Variables or Features? : 변수란?

☺︎ Categorical variables : 범주형 변수란?

☺︎ Categorical variables Encoding : 범주형 변수 인코딩?

☻ Reference 

-----------------------------------------------------------------------

## ☺︎ Variables or Features?
변수 (variable)는 literally (말 그대로) 변하는 수를 의미한다 [1]. 

사전적 의미의 variable is not consistent or having a fixed pattern; liable to change.

조금 더 deep dive한 의미를 wikipedia에서 본다면 [2], 

> In computer programming, a variable is an abstract storage location paired with an associated symbolic name, which contains some known or unknown quantity of information referred to as a value; or in simpler terms, a variable is a container for a particular set of bits or type of data (like integer, float, String etc...). A variable can eventually be associated with or identified by a memory address. The variable name is the usual way to reference the stored value, in addition to referring to the variable itself, depending on the context. This separation of name and content allows the name to be used independently of the exact information it represents.


이를 좀 더 Data science (or data analysis) 관점에서 바라본다면 value (값) 는 두가지로 나눠질 수 있고, 여기서 우리가 ***고려하는 변수 (Features, Variable)는 Known value 에 속하는 값으로 예측을 수행하는데 사용되는 입력 변수라고 볼 수 있다.*** 



Known value	Predicted value
name	Features (변수)
Attribute (속성)
Predictor (예측변수)
Dimension (차원)
Observation (관측치)
Independent Variable (독립변수)	Lable (라벨)
Class (클래스)
Target (목푯값)
Response (반응)
Dependent Variable (종속변수) 


이러한 변수는 (혹은 데이터라는 큰 관점에서 본다면) 다음과 같이 Qualitative (Categorical) 혹은 Quantitative (Numerical)로 나눌수 있다. (아래 Schematic 참고)






## ☺︎ Categorical  variables 
Categorical (범주형)은 특성에 따라 범주로 구분하여 측정한 변수이며, 좀 더 자세하게 살펴보면 ***a. 순서가 없는 명목형 (nominal)*** 과 ***b. 순서가 있는 (ordinal)*** 로 나눌수 있다. 

Nominal (명목형)	
순서와 상관없고, 의미없이 이름만 의미가 부여 가능한 경우
(Gender, 성별; 자동차 브랜드; 꽃 종류; 눈동자 색 등)	
Ordinal (순서형)
어떤 기준에 따라 순서에 의미를 부여하는 경우
(교육 수준; 만족도; 생활 수준 등 우위가 존재하는 경우)


## ☺︎ Categorical  Variables Encoding 
하지만, 범주형 변수의 경우 string으로 되어 있기 때문에 features (입력변수)로 고려하기 위해서는 숫자로 인코딩 작업을 해줘야 한다. 

이에 대한 설명을 조금 추가하자면 [3] 

Machine learning models require all input and output variables to be numeric.
This means that if your data contains categorical data, you must encode it to numbers before you can fit and evaluate a model.


이제 범주형 변수는 반드시 encoding을 통해서 숫자로 변환 작업을 진행해야 우리가 원하는 모델에 적용 할 수 있다는 부분은 이해했다. 

여기서 중요한 부분은 데이터의 정보 손실을 최소화하기 위해서는 데이터에 맞는 적절한 인코딩이 필요하다는 것이다. 



이때, Categorical variables에서도 type에 따라서 적절한 encoding방법이 나눠지게 된다.  (아래 Schematic 참고)




이를 기반으로 내가 갖고 있는 features (or variables, dataset 등)에 맞춰서 encoding을 고려하면 좋을 것으로 생각된다. 



### a. One-hot encoding (get dummies)
쉽게 말해서 해당 column내의 category (혹은 label) 0과 1의 벡터로 encoding시키는 것이다. 



장단점을 자세하게 정리하면 다음과 같다 [4]

Advantages	Disadvantages
+ 사용하기 매우 편함
+ 각 category는 구분되어 있어서 편향이 적다. 	


여기서 limitation은 범주가 많아질 수록 2^n만큼 column(열)이 추가된다. 

따라서 gender 같이 male, Female의 경우, [0,1] 혹은 [1,0]이 되겠지만, 여러개의 category로 나눠진 데이터의 경우 열의 수는 계속적으로 추가된다. 



자세한 부분은 아래 schematic을 고려하면 될 것 이다. 



<그림>



### b. Mean encoding 
이는 supervised encoding개념으로 발생횟수에 따라서 그 값을 갖게 된다. 문제는 categories의 분포도가 치우친 경우이다. 



### c. Label encoding 
Label의 의존성이 커진다.

## ☻ Reference 
1. 변수(wikipedia) : https://ko.wikipedia.org/wiki/%EB%B3%80%EC%88%98
2. Variables (wikipedia) : https://en.wikipedia.org/wiki/Variable_(computer_science) 
3. https://machinelearningmastery.com/one-hot-encoding-for-categorical-data/
4. Types of Encoding : https://www.analyticsvidhya.com/blog/2020/08/types-of-categorical-data-encoding/


encoding https://sjpyo.tistory.com/16

https://wyatt37.tistory.com/11

https://techblog-history-younghunjo1.tistory.com/99

https://azanewta.tistory.com/46





Thanks for reading. Hope to see you again :o)
