---
id: 1046
title: 선형대수의 Replacement Theorem
date: 2017-11-10T03:28:03+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
Replacement Theorem은 vector space 단원에서 제일 중요한지는.... 잘 모르겠고 어쨌든 응용할 껀덕지가 제일 많은 정리이다. 이쪽 단원의 웬만한 따름정리들은 이거 이용해서 증명한다.

**Replacement Theorem: $V=span(G)$라 하자. 여기서 $G$는 $n$개의 벡터를 원소를 가지는 집합이다. 만약 $L$이 $V$의 $m$개의 linearly independent한 벡터를 원소로 가지는 subset이라면, $m\leq n$이고, $Span(L\cup H)=V$인 $n-m$개의 벡터를 원소로 가지는 $G$의 subset $H$이 존재한다.**

그러니까 조금 풀어 얘기하자면 어떤 generating set이 있으면 얘가 generate한 vector space의 linearly independent한 set은 generating set보다는 많은 원소를 가질 수는 없고, 또 $G$에서 몇개 골라 $L$에다 집어넣어 다시 Generating set으로 만들 수 있단 이야기이다.

**Proof:** 수학적 귀납법을 사용한다. $L=\emptyset$이라면, $H=G$가 조건을 만족하는 $G$이다. $G$가 $n$개의 벡터를 원소로 가진다 하자. 정리가 $k\in\mathbb{N}=m$에 대하여 성립한다고 가정하고, $k+1$에 대하서 증명을 시작하자. $L$이 벡터$m+1$개짜리 linearly independent한 집합이면 자명히 그 subset인 $m$개짜리에 대해서 가정을 적용할 수 있다.  $m\leq n$이겠고 우선, 또한 이거랑 합집합이 $V$를 generates하는 $G$의 원소 $n-m$개짜리 subset이 있을 것이다. 이제 이 합집합이 $V$를 generate하니까, 아까 $L$에 남아있던 그 벡터 하나는 이 합집합의 linear combination으로 표현 가능하다.

그런데 이 말은 $n-m$이 $0$이면 $L$이 linearly dependent하다는 말이므로 $n-m>0$을 얻는다. 이제 아까 그 linear combination을 생각하자. 방금과 같은 이유로 $G$의 subset의 원소에 붙는 계수들 중 $0$이 아닌게 적어도 하나 이상은 있을 것이고, 그럼 이제 잘 이항하고, 양변 나누고, 하면 이 원소인 vector를 $G$의 subset중 이 원소 빼고 나머지 원소들과 $L$의 linear combination인 표현식을 얻는다.  이 표현식을 구성하는 벡터들을 원소로 가지는 집합을 $L\cup H$이라 해도 좋고, 그럼 $span(L\cup H)$가 가정에서 말했던 generating set을 포함하므로 $L\cup H$역시 generating set이다.

 &nbsp;