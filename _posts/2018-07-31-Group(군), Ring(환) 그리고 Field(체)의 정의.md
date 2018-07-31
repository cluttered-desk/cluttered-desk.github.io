---
title: Group(군), Ring(환) 그리고 Field(체)의 정의
date: 2018-07-31T17:55:08+00:00
author: cluttered desk
layout: post
tags: Mathematics
---

# Overview

추상대수(Abstract Algebra)라는 분야의 이름에서 알 수 있듯이, 추상대수는 기존의 수학이 다루던 것들에서 추상화를 거치고 거친 뒤에야 남은 극도로 단순한 것들에 대한 수학이라 할 수 있겠다. 이를테면 Classical Mechanics가 주변 모든 물체들을 particle로 보아 분석하는 것처럼(기억하자, rigid body는 결국 고전역학적 관점에서 매우 많은 입자로 이루어진, 그리고 그 계를 강체라고 부르기 적당한 상호작용이 서로 작용하는 입자계일 뿐이다.), 추상대수는 수많은 수학적 개체들을 각각의 원소와 연산, 그리고 그것들이 가진 구조에만 집중한다.

그 구조라 하면 제목에서 말한 것처럼 크게 Group, Ring 그리고 Field가 있을 것이다. 사실 추상대수를 들을 정도로 수학과 수업에 자신의 시간을 투자할 계획이 없는 사람일지라도, 저 각각의 이름 정도는 반드시 마주치게 되기 마련이므로(당장 Vector space가 어떤 field 위에서 정의됨을 생각해 보자.), 각각이 어떤 구조를 지칭하는지 정도는 알아두면 좋다.

우선 기본적으로 각각은 일단 집합과 한개(Group의 경우) 혹은 두개의 연산(Ring과 Field의 경우)로 이루어진다. 좀더 자세히 살펴보자. 

## Group(군)

어떤 집합 $G$와 그 원소에 대한 이항연산(보통 multiplication이라고 부른다) $\cdot$ 에 대해, 다음 성질들을 만족시키는 경우에 이 두개의 세트 $(G,\cdot)$가 군을 이룬다고 한다. 

1. 일단 연산 아래에서 닫혀있고,
2. 결합볍칙이 성립한다. 그 말인 즉슨, $a,b,c\in G$일때 $(a\cdot b)\cdot c = a\cdot(b\cdot c)$라는 이야기이다.
3. 또한 항등원과 역원이 존재한다.

추가적으로 덧붙이자면 교환법칙이 성립할 필요는 없다는 것이다. 교환법칙이 성립한다면 abelian group이라 부른다. 또한 3에서, right inverse와 left inverse가 같다. 즉 $a\cdot b = b\cdot c=I$라면은, $a=c$ 라는 이야기이다. $a\cdot b\cdot c=a=c$이기 때문이다.

그럼 군에는 대표적으로 무엇이 있을까? 우선 Lorentz Transformation이 Group이다. Lorentz Transformation이

$$\begin{pmatrix}\cosh{\rho}&\sinh{\rho}\\ \sinh{\rho}&\cosh{\rho}\end{pmatrix}$$

의 형태로 써지고, 연산을 일반적인 행렬곱으로 정의하고 1,2,3을 점검해 보자.

꼭 이런 뭔가 수리적인 예만 있는 것은 아니다. 또 다른 예로는, n개의 공의 배열과 각각을 섞는 것을 연산이라고 한다면 이 역시 군을 이룬다. (Symmetric Group혹은 Permutation Group이라 한다.) 항등원은 당연히 존재하고(공을 그대로 냅두면 된다.), 역원도 어떤 섞는 연산의 역과정으로 존재하며, 자명히 닫혀있으며 associative하다. 이를 생각할때 commutative 하지 않음에 주의하자. $a(bc)$를 생각할때 $(bc)a$와 헷갈리기 쉽다.

## Ring(환)

이제 Group의 정의에서 하나씩 살을 붙여가는 식으로 이해하는 것이 좋다. Ring은 Group의 정의에서 하나의 연산을 더 필요로 한다. 보통 Addition이라 한다. 이제 집합 $R$과 연산 $\cdot, +$ 에 대해 다음 성질을 만족하면 세트 $(R,\cdot,+)$가 환을 이룬다고 한다.

1. $(R,+)$가 아벨군이고,
2. $(R,\cdot)$이 모노이드이다. 모노이드라는건 $\cdot$에 대해 항등원이 존재하고 associative하다는 이야기이다.
3. 분배법칙 $a\cdot(b+c)=(a\cdot b)+(a\cdot c)$와  $(b+c)\cdot a=(b\cdot a)+(c\cdot a)$가 성립한다.

주의할 것은 2.이다. 책마다 정의가 $(R,\cdot)$이 monoid라는 책이 있고, magma(monoid의 정의에서 항등원의 존재가 빠진 것) 이 있다. 조금 더 표준적인 정의는  monoid인 것으로 보인다.

여기에 multiplication이 commutative한지에 따라 commutative ring과 noncommutative ring으로 나뉜다.

예로는 아주 친숙한 것들이 있다. 일단 정수가 일반적으로 알고 있는 덧셈과 곱셈에 대해 (commutative) ring일 것이고, 행렬 또한 (noncommutative) ring이다. 

## Field(체)

Field의 정의는 Ring에서 시작한다. $+$에 대한 identity를 $0$으로 쓰자. 그리고 이제 $0$빼고 모든 원소에 대해 연산 $\cdot$에 대한 inverse가 존재한다 하자. 이런 ring을 division ring이라 한다.

그렇다면 field는 commutative division ring으로 정의된다.

예로는 실수집합이 통상적인 곱셈과 덧셈에 대하여 field를 이룬다. 이제 여기서 대부분의 notation이 실수에서 통용되는 그대로인 것을 알 수 있다. 괜히 $+$의 identity 가 $0$인게 아니다. 마찬가지로 $\cdot$의 identity로 $1$로 자주 쓴다.(그러나 보통 이쪽은 $I$가 더 많은 듯 하다.)

여기서 division ring의 정의에 대해 의아함이 생길 수도 있다. 실수에서야 진짜로 $0$은 inverse가 없다 치지만, 모든 경우에도 그럴 것인가? 답은 그렇다이다. 아래를 보자. 임의의 원소 $a$에 대해,

$$a\cdot 0=a\cdot (0+0)=a\cdot 0+a\cdot0$$

이고, 이제 양변에 $a\cdot 0$의 addition에 대한 inverse를 더해보자.

