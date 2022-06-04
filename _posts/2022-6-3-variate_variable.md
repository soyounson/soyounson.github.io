---
layout: post
title: Multivariate vs Multivariable <img src="/images/B-icon-ver.png" width="30">
---



<img src="/images/B-icon-ver.png" width="200">

모두의 연구소에서 진행하는 "함께 콘텐츠를 제작하는 콘텐츠 크리에이터 모임"인 **COCRE(코크리)** 의 2기 회원으로 제작한 글입니다

[🐘 코크리가 궁금하다면 클릭!](https://medium.com/modulabs/cocre-%EC%BD%94%ED%81%AC%EB%A6%AC-%EB%A5%BC-%EC%86%8C%EA%B0%9C%ED%95%A9%EB%8B%88%EB%8B%A4-c3a4e9519e85)

------------------------------------


### Multivariate or Multivariable?

가끔 "Do you know it? what does it mean?" 이라는 질문이 들어오면, 잠시 정적하면서 생각을 정리해야 하는 경우가 있다. 

머릿속으로는 두둥실 기억의 구름 속 🌥🌥🌥 어딘가에 있는 기록?저장되어 있는  꺼내보려 하는데, 그게 잘 안된다. 

분명 알고 있는 것인데, 갑자기 왜 생각이 안나는지 혹은 생각은 나는데 왜 말을 잘 못하고 버벅 거리는지...

갑자기 식은땀이 주르륵 흘러내리면서, "OMG, I know that..." 그리고 눈이 뱅글뱅글 돌아가게 된다 👀 . 


<img src="/images/cookie-monster.gif" width="400">

[image source](https://www.google.com/imgres?imgurl=https%3A%2F%2Fc.tenor.com%2Fe2dMDgfK9-oAAAAC%2Fcookie-monster.gif&imgrefurl=https%3A%2F%2Ftenor.com%2Fsearch%2Fcookie-monster-googly-eyes-gifs&tbnid=1zH-sH5FYVY3kM&vet=12ahUKEwjtgqr1npD4AhWSdd4KHcNPDeAQMygAegUIARDcAQ..i&docid=ksDSqZR8ehuvDM&w=498&h=351&q=gif%20eye%20spin%20sesame%20street&ved=2ahUKEwjtgqr1npD4AhWSdd4KHcNPDeAQMygAegUIARDcAQ)

무엇이 문제였을까? 내가 몰랐던 것일까? 아니면 수박 겉핥기식으로 알았던 것일까? 

아마 둘 다 일 것이다.

> "네가 설명하지 못한다면 그건 네 것이 아니다." 그리고 "이해하지 못하면 책장을 넘기지 말아라". 
> 분명 로버트가 했던 말일 것이다. 4 ~ 5년전 일인데도 여전히 선명한 말들이 있다. 

<img src="/images/thinking.gif" width="300">

[image source](https://www.google.com/search?q=elmo+cold+gif&sxsrf=ALiCzsYSPdQVkSSpC9aSNqqbazsZZs1J3g:1654327020526&source=lnms&tbm=isch&sa=X&ved=2ahUKEwjj0JmzoJP4AhXMqVYBHVtgBzIQ_AUoAXoECAEQAw&biw=1338&bih=741&dpr=2#imgrc=OUpEFXgmr06rNM&imgdii=uNqLHnkpDl1FsM)

아무튼, Variate 와 Variable을 구별해서 써야 한다는 것은 신선한 충격이었다. 🐟 ~

뭐! 이제부터 알아보자 :)


-----------------------------------------------------------------------

☾ Table of contents

☺︎ Variate/Variable       
  - Uni-/Multi-         
  - Multivariate/Multivariable
 
☻ Reference

-----------------------------------------------------------------------


### ☺︎ Variate/Variable 

우선, 사전적 의미를 확인해보자.                
(단, 바로 답을 확인하고 싶으면 조금만 내려가서 `☻ Multivariate/Multivariable` 섹션에 있는 표를 확인하는 것을 추천한다!)

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

즉, 아주 roughly하게 이해하자면 variate는 종속변수인 y, variable은 독립변수인 x라고 볼 수 있다.

위에서 언급되었듯, variate란 변량으로 변하는 양이다. 무엇인가 (input혹은 variable)에 따라서 영향을 받아서 변하는 양으로 볼 수 있고, 이 특성은 종속적이기 때문이다.

흠...그래도 여전히 완벽하게 이해가 되지는 않는 것 같다. 

<img src="/images/cookie-monster-sesame-street.gif" width="300">
[image_source](https://www.google.com/search?q=gif+sesame+street&tbm=isch&ved=2ahUKEwjtgqr1npD4AhWSdd4KHcNPDeAQ2-cCegQIABAA&oq=gif+sesame+street&gs_lcp=CgNpbWcQAzIFCAAQgAQyBggAEB4QBzIICAAQHhAHEAUyBggAEB4QBTIGCAAQHhAFMgYIABAeEAUyBggAEB4QBTIGCAAQHhAIMgYIABAeEAgyBggAEB4QCDoICAAQHhAIEAdQ8wdY4g5goRBoAXAAeAGAAY4HiAHcDJIBCTAuNC4xLjYtMZgBAKABAaoBC2d3cy13aXotaW1nwAEB&sclient=img&ei=t3KZYq3LBpLr-QbDn7WADg&bih=962&biw=1265&rlz=1C1GCEU_enKR961KR961#imgrc=8KLZXsbmuvNU6M)

좀 더 자세한 부분은 multivariate와 multivariable을 비교하면서 확인하도록 하자. 


#### ☻ Uni-/Multi-

우선, warmup으로 uni와 multi를 구분하자면 말 그대로 하나인지 (uni) 혹은 다수인지 (multi)나타내는 것이다.
wikitionary에서 어원학 관점에서 본다면 uni-는 Latin에서 온 것으로 다음과 같다 [3]. 

~~~~~~~~~~~~~~~~
Etymology
: From Latin uni-, combining form of unus (“one”).
Prefix
: one, single
Synonyms
: mono-
~~~~~~~~~~~~~~~~

그렇다면 multi-의 어원을 확인해보자 [4].

~~~~~~~~~~~~~~~~
Etymology
: From Latin multī, from multus.
Prefix
: multi-
  - More than one; pertaining to more than one thing.
  - Many; pertaining to many things.
Synonyms
  - (many): poly- (from Ancient Greek)
  - (more than one): pluri- (from Latin)
~~~~~~~~~~~~~~~~



#### ☻ Multivariate/Multivariable





The term "multivariate" refers to multiple independent variables or numerous measurements of the same independent variable, while the term "multivariable" refers to numerous dependent variables but only one independent variable.

| Univariate | Multivariate | Univariable | Multivariable |
|---|---|---|---|
|단변량, 1개 종속변수|다변량, 여러개 종속변수|단변수, 1개 독립변수|다변수, 여러개 독립변수|


 

 ``` 


 ```
 
 <img src="/images/sesame_hooray.gif" width="400">

[source code](https://www.google.com/search?q=gif+sesame+street&tbm=isch&ved=2ahUKEwjtgqr1npD4AhWSdd4KHcNPDeAQ2-cCegQIABAA&oq=gif+sesame+street&gs_lcp=CgNpbWcQAzIFCAAQgAQyBggAEB4QBzIICAAQHhAHEAUyBggAEB4QBTIGCAAQHhAFMgYIABAeEAUyBggAEB4QBTIGCAAQHhAIMgYIABAeEAgyBggAEB4QCDoICAAQHhAIEAdQ8wdY4g5goRBoAXAAeAGAAY4HiAHcDJIBCTAuNC4xLjYtMZgBAKABAaoBC2d3cy13aXotaW1nwAEB&sclient=img&ei=t3KZYq3LBpLr-QbDn7WADg&bih=962&biw=1265&rlz=1C1GCEU_enKR961KR961#imgrc=YMO7GoJPUxQLgM)

### ☻ Reference
1. 네이버 국어/영어사전 
2. [StackExchange : Mathematics] (https://math.stackexchange.com/questions/204705/differences-between-variable-and-variate#:~:text=Variate%3A%20%22a%20quantity%20having%20a,to%20assume%20different%20numerical%20values.%22)
3. [wikitionary : uni-](https://en.wiktionary.org/wiki/uni-)
4. [wikitionary : multi-](https://en.wiktionary.org/wiki/multi-)



4. https://www.researchgate.net/post/What-is-the-difference-between-Muntivaiate-analysis-and-multivariable-analysis#:~:text=The%20term%20%22multivariate%22%20refers%20to,but%20only%20one%20independent%20variable.
5. https://mansoostat.tistory.com/23


🌺 **Thanks for reading. Hope to see you again :o)**



 <img src="/images/VLrW.gif" width="400">

[source code](https://www.google.com/search?q=gif+sesame+street&tbm=isch&ved=2ahUKEwjtgqr1npD4AhWSdd4KHcNPDeAQ2-cCegQIABAA&oq=gif+sesame+street&gs_lcp=CgNpbWcQAzIFCAAQgAQyBggAEB4QBzIICAAQHhAHEAUyBggAEB4QBTIGCAAQHhAFMgYIABAeEAUyBggAEB4QBTIGCAAQHhAIMgYIABAeEAgyBggAEB4QCDoICAAQHhAIEAdQ8wdY4g5goRBoAXAAeAGAAY4HiAHcDJIBCTAuNC4xLjYtMZgBAKABAaoBC2d3cy13aXotaW1nwAEB&sclient=img&ei=t3KZYq3LBpLr-QbDn7WADg&bih=962&biw=1265&rlz=1C1GCEU_enKR961KR961#imgrc=m2x9GgVp9fgX5M)

<img src="/images/oldmen.gif" width="400">

[image source](https://www.google.com/imgres?imgurl=https%3A%2F%2Fc.tenor.com%2FlQkPc7ZIU1IAAAAC%2Fsesame-street.gif&imgrefurl=https%3A%2F%2Ftenor.com%2Fview%2Fsesame-street-waldorf-stadtler-gif-7292732&tbnid=8bm5GXKojvK1-M&vet=12ahUKEwiIh8DPvZH4AhXeTPUHHceFBlIQMygPegUIARC0Ag..i&docid=2M_p7Dw-5L7ooM&w=350&h=200&q=gif%20sesame%20street&ved=2ahUKEwiIh8DPvZH4AhXeTPUHHceFBlIQMygPegUIARC0Ag)


<img src="/images/sesamest-sesame.gif" width="400">

[image source](https://www.google.com/search?q=gif+sesame+street&tbm=isch&ved=2ahUKEwjtgqr1npD4AhWSdd4KHcNPDeAQ2-cCegQIABAA&oq=gif+sesame+street&gs_lcp=CgNpbWcQAzIFCAAQgAQyBggAEB4QBzIICAAQHhAHEAUyBggAEB4QBTIGCAAQHhAFMgYIABAeEAUyBggAEB4QBTIGCAAQHhAIMgYIABAeEAgyBggAEB4QCDoICAAQHhAIEAdQ8wdY4g5goRBoAXAAeAGAAY4HiAHcDJIBCTAuNC4xLjYtMZgBAKABAaoBC2d3cy13aXotaW1nwAEB&sclient=img&ei=t3KZYq3LBpLr-QbDn7WADg&bih=962&biw=1265&rlz=1C1GCEU_enKR961KR961#imgrc=naqrHsFeasScLM)


<img src="/images/elmo-freezing.gif" width="400">

[image source](https://www.google.com/search?q=elmo+cold+gif&sxsrf=ALiCzsYSPdQVkSSpC9aSNqqbazsZZs1J3g:1654327020526&source=lnms&tbm=isch&sa=X&ved=2ahUKEwjj0JmzoJP4AhXMqVYBHVtgBzIQ_AUoAXoECAEQAw&biw=1338&bih=741&dpr=2#imgrc=OUpEFXgmr06rNM)

<img src="/images/study_sesame.gif" width="400">

[image_source](https://www.google.com/search?q=gif+sesame+street&tbm=isch&ved=2ahUKEwjtgqr1npD4AhWSdd4KHcNPDeAQ2-cCegQIABAA&oq=gif+sesame+street&gs_lcp=CgNpbWcQAzIFCAAQgAQyBggAEB4QBzIICAAQHhAHEAUyBggAEB4QBTIGCAAQHhAFMgYIABAeEAUyBggAEB4QBTIGCAAQHhAIMgYIABAeEAgyBggAEB4QCDoICAAQHhAIEAdQ8wdY4g5goRBoAXAAeAGAAY4HiAHcDJIBCTAuNC4xLjYtMZgBAKABAaoBC2d3cy13aXotaW1nwAEB&sclient=img&ei=t3KZYq3LBpLr-QbDn7WADg&bih=962&biw=1265&rlz=1C1GCEU_enKR961KR961#imgrc=UhY8fdWJqtIQMM&imgdii=DaOJJ-897H6GxM)

<img src="/images/giphy.gif" width="400">

[image_source](https://www.google.com/imgres?imgurl=https%3A%2F%2Fmedia3.giphy.com%2Fmedia%2FMtmFbGJ6YsUEg%2Fgiphy.gif&imgrefurl=https%3A%2F%2Fgiphy.com%2Fexplore%2Fberm&tbnid=hrNDNQYoyacLCM&vet=10CB4QxiAoBWoXChMI-N6Olp-Q-AIVAAAAAB0AAAAAECA..i&docid=otbErsbmbr_PIM&w=420&h=340&itg=1&q=gif%20sesame%20street&ved=0CB4QxiAoBWoXChMI-N6Olp-Q-AIVAAAAAB0AAAAAECA)

