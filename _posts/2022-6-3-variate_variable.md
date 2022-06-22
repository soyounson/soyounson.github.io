---
layout: post
title: Multivariate vs Multivariable <img src="/images/B-icon-ver.png" width="30">
---

### Multivariate (다변량) vs Multivariable (다변수)란?

가끔 "Do you know it? what does it mean?" 이라는 질문이 들어오면, 잠시 정적하면서 생각을 정리해야 하는 경우가 있다. 

머릿속으로는 두둥실 기억의 구름 속 🌥🌥🌥 어딘가에 있는 기록?저장되어 있는  꺼내보려 하는데, 그게 잘 안된다. 

분명 알고 있는 것인데, 갑자기 왜 생각이 안나는지 혹은 생각은 나는데 왜 말을 잘 못하고 버벅 거리는지...

갑자기 식은땀이 주르륵 흘러내리면서, "OMG, I know that..." 그리고 눈이 뱅글뱅글 돌아가게 된다 👀 . 

<p align="center">
<img src="/images/cookie-monster_googly_eye.gif" width="350">
</p>

무엇이 문제였을까? 내가 몰랐던 것일까? 아니면 수박 겉핥기식으로 알았던 것일까? 

아마 둘 다 일 것이다.

> "네가 설명하지 못한다면 그건 네 것이 아니다." 그리고 "이해하지 못하면 책장을 넘기지 말아라". 
> 분명 로버트가 했던 말일 것이다. 4 ~ 5년전 일인데도 여전히 선명한 말들이 있다. 


<p align="center">
<img src="/images/elmo_thinki.gif" width="300">
</p>

아무튼, Variate 와 Variable을 구별해서 써야 한다는 것은 신선한 충격이었다. 🐟 ~

뭐! 이제부터 알아보자 :)

-----------------------------------------------------------------------

☾ Table of contents

☺︎ Variate/Variable       
  - Uni-/Multi-         
  - Multivariate/Multivariable
  
☺︎ Variable types 

☻ Reference

-----------------------------------------------------------------------


### ☺︎ Variate/Variable 

우선, 사전적 의미를 확인해보자.                
(단, 바로 답을 확인하고 싶으면 조금만 내려가서 `☻ Multivariate/Multivariable` 섹션에 있는 schematic을  추천한다!)

~~~~~~~~~~~~~~~~~~~~~
◦ Variate : 변량
◦ Variable : 변수 
~~~~~~~~~~~~~~~~~~~~~

를 의미한다 [1]. 국어 사전의 의미를 한번 확인해보면 

~~~~~~~~~~~~~~~~~~~~~
◦ 변량 (Variate)
  1.	수학 주어진 조건에 따라 변화하는 양.
  2.	수학 통계에서, 조사 내용의 특성을 수량으로 나타낸 것. 신장이나 체중 따위처럼 구간 내 값을 연속적으로 취할 수 있는 연속 변량과, 득점처럼 분리된 값만 취하는 이산 변량이 있다.
◦ 변수 (Variable)
  1.	어떤 상황의 가변적 요인.
  2.	수학 어떤 관계나 범위 안에서 여러 가지 값으로 변할 수 있는 수.
~~~~~~~~~~~~~~~~~~~~~

가 된다. 그럼 statistics에서 define한 variate와 variable은 무엇일까 [2]?

~~~~~~~~~~~~~~~~~~~~~
◦ Variate: "a quantity having a numerical value for each member of a group, 
especially one whose values occur according to a frequency distribution." 
◦ Variable: "a factor or quantity able to assume different numerical values."
~~~~~~~~~~~~~~~~~~~~~

즉, 아주 roughly하게 이해하자면 variate는 종속변수인 y, variable은 독립변수인 x 라고 볼 수 있다.

위에서 언급되었듯, variate란 변량으로 변하는 양이다. 무엇인가 (input혹은 variable)에 따라서 영향을 받아서 변하는 양으로 볼 수 있고, 이 특성은 종속적이기 때문이다.

흠...그래도 여전히 완벽하게 이해가 되지는 않는 것 같다. 


<p align="center">
<img src="/images/cookie_monster_think.gif" width="350">
</p>

좀 더 자세한 부분은 multivariate와 multivariable을 비교하면서 확인하도록 하자. 


#### ☻ Uni-/Multi-

우선, warmup으로 uni와 multi를 구분하자면 말 그대로 하나인지 (uni) 혹은 다수인지 (multi)나타내는 것이다.
wikitionary에서 어원학 관점에서 본다면 uni-는 Latin에서 온 것으로 다음과 같다 [3]. 

~~~~~~~~~~~~~~~~
◦ Etymology
: From Latin uni-, combining form of unus (“one”).
◦ Prefix
: one, single
◦ Synonyms
: mono-
~~~~~~~~~~~~~~~~

그렇다면 multi-의 어원을 확인해보자 [4].

~~~~~~~~~~~~~~~~
◦ Etymology
: From Latin multī, from multus.
◦ Prefix
: multi-
  - More than one; pertaining to more than one thing.
  - Many; pertaining to many things.
◦ Synonyms
  - (many): poly- (from Ancient Greek)
  - (more than one): pluri- (from Latin)
~~~~~~~~~~~~~~~~

즉, uni-는 한개, multi-는 여러개로 보고 가면 될 것이다. 

#### ☻ Multivariate/Multivariable [5]

그럼, 둘의 차이는 아래 schematic을 참고바란다.             
(아래 schematic은 블로그 글[5]을 참고하여 제가 작성한 것 입니다.)

<p align="center">
<img src="/images/variate_variable.jpg" width="700">
</p>

이러한 Univariate/Multivariate/Univariable/Multivariable은 대표적으로 regression analysis에서 사용되어 지는데, 좀 더 detail하게 확인해보면 [6], 

~~~~~~~~~~~~~~~~
The term "multivariate" refers to multiple independent variables or numerous measurements of the 
same independent variable, while the term "multivariable" refers to numerous dependent variables 
but only one independent variable.

repeatedly, 

Multivariable analysis is used for analysis with one outcome (dependent variable) and multiple 
independent (predictors or factors) while Multivariate is used for the analysis with more than 
1 outcome variables (eg, repeated measures) and multiple independent variables.
~~~~~~~~~~~~~~~~


직관적인 관점에서 생각해보면,

Multivariate means more than 1 dependent variable (y) but multivariable means more than 1 Independent variable (x) 라고 볼 수 있다. 

즉, 다변량 (multivariate)는 종속변수 (대표적으로 y)가 여러개이고, 다변수 (multivariable)는 독립변수 (대표적으로 x)가 여러개임을 의미한다. 

아마도 풀고 있는 문제, 혹은 읽고 있는 article (or paper)를 보면서 생각을 정리하면 이 의미가 좀 더 명확해 질 것이라 생각한다. 

### ☺︎ Variable types 

살짝 더 deep dive하게 생각해보면 (후에 작성할 feature engineering 글에서 언급 할 내용이지만), variable의 type에 대해서 확인해보자. 

Variable (혹은 데이터라는 큰 관점에서 본다면)은 다음과 같이 Qualitative (Categorical) 혹은 Quantitative (Numerical)로 나눌수 있다. (아래 schematic은 제가 작성한 것 입니다.)

<p align="center">
<img src="/images/Feature_type.jpg" width="700">
</p>

이 글에서 다루고 있지는 않지만, data analysis을 위한 feature engineering, preprocessing, data cleaning등에서 내가 갖고 있는 variable의 type이 어떤 것인지, 분석을 위해 어떤 식으로 encoding을 진행해야 하는지 (혹은 다른 processes)에 대해서는 나중에 차차 다뤄볼 예정이다. 

-----------------------------------

아무튼, 내가 공부하다가 궁금했던 부분을 누군가와 공유하는 것은 참 마음이 따스해지는 일이라고 생각한다.   

물론 이 글이 완벽하지 않지만, 누군가가 이 주제에 대해서 이해하는데 아주 조그마한 trigger p't라도 되길 바란다 🙏🏻.

도움이 되었으면 좋겠다 :)

<p align="center">
<img src="/images/chicken_happy.gif" width="450">
</p>


### ☻ Reference
1. 네이버 국어/영어사전 
2. [StackExchange: Mathematics](https://math.stackexchange.com/questions/204705/differences-between-variable-and-variate#:~:text=Variate%3A%20%22a%20quantity%20having%20a,to%20assume%20different%20numerical%20values.%22)
3. [wikitionary: uni-](https://en.wiktionary.org/wiki/uni-)
4. [wikitionary: multi-](https://en.wiktionary.org/wiki/multi-)
5. [모찌의 라이프 레코드: Univariate,Multivariate vs. Univariable,Multivariable](https://mansoostat.tistory.com/23)
6. [ResearchGate: difference between Muntivaiate analysis and multivariable analysis](https://www.researchgate.net/post/What-is-the-difference-between-Muntivaiate-analysis-and-multivariable-analysis#:~:text=The%20term%20%22multivariate%22%20refers%20to,but%20only%20one%20independent%20variable)


### ☻ image sources
1. [Giphy](https://giphy.com/search/sesame-street)
2. [Tenor](https://tenor.com/view/cookie-monster-crazy-eyes-gif-20394322)


🌺 **Thanks for reading. Hope to see you again :o)**


-----------------------------------


<p align="center">
<img src="/images/B-icon-ver.png" width="150">
</p>

모두의 연구소에서 진행하는 "함께 콘텐츠를 제작하는 콘텐츠 크리에이터 모임"인 **COCRE(코크리)** 의 2기 회원으로 제작한 글입니다

[🐘 코크리가 궁금하다면 클릭!](https://medium.com/modulabs/cocre-%EC%BD%94%ED%81%AC%EB%A6%AC-%EB%A5%BC-%EC%86%8C%EA%B0%9C%ED%95%A9%EB%8B%88%EB%8B%A4-c3a4e9519e85)





