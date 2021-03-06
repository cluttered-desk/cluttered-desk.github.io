---
id: 1151
title: 'Roche limit: 로쉬 한계-위성과 모행성의 최소 거리'
date: 2017-11-25T21:44:24+00:00
author: Abraxas Academy
layout: post
tags: Physics
---
모행성의 주위를 도는 천체를 위성이라 한다. 이 둘 사이의 거리는 무한정 가까워질수 없는데, 왜냐하면 너무 가까워지게 되면 조석력에 의해 천체 자체가 박살이 나기 때문이다. 그 거리를 구해보자.

사실 이는 썩 만만한 작업은 아닌데, 왜냐하면 천체는 강체가 아니기 때문에 타원형으로 찌그러지고, 계산이 복잡해지기 때문이다. 하지만 귀찮으니까 그냥 강체라 치고 풀자.

아래 그림을 보자.

[![KakaoTalk_20171123_020850643](https://farm5.staticflickr.com/4585/38584390271_f913067410_c.jpg)](https://www.flickr.com/gp/152463819@N08/uBhdD6)

둘 사이의 거리를 까먹고 안썼는데, $d$라 하자. 위성의 반지름은 $r$이다. 그럼 케플러의 제3법칙 $T^2 = {\dfrac{4\pi^2}{G (M)}} a^3$에 의해, ($M>>m$이다)

$\omega^2 = \dfrac{GM}{d^3}$이다.  따라서 이제 $$(r+d)\omega^2-d\omega^2+\frac{GM}{d^2}-\frac{GM}{d+r}^2\simeq\frac{GM}{d^3}+r\omega^2=\frac{3GMr}{d^3}=\frac{Gm}{r^2}$$

을 만족하는 $d$가 Roche limit(조석력이 중력과 평형을 이루는 지점을 찾은 것이다)이므로 $$d=r\bigg(\frac{3M}{m}\bigg)^{(1/3)}$$을 얻는다.