---
id: 1059
title: 'Simple pendulum of arbitrary amplitude &#8211; 작은 각도 근사 없이 진자의 주기 구하기'
date: 2017-11-13T09:06:39+00:00
author: Abraxas Academy
layout: post
tags: Physics
---
물리토픽인듯 싶지만 사실 수학에 더 가깝다. 진자의 운동방정식은 $l^2\ddot{\theta}=-lg\sin(\theta)$였고, 여기서 $\sin(\theta)=\theta$로 근사해 푸는게 작은 각도 근사다. 근사 없이 미분방정식을 풀어보자. 에너지를 사용하면
 ![url=https://flic.kr/p/Dm79iU](https://farm5.staticflickr.com/4569/24512728958_bd16b66074_b.jpg)
  당연히 $\theta_{max}$는 진폭이 최대일때의 각도고, 뭐 에너지를 사용하니까 혹시 완죤 새로운 방정식이 나왔다고 생각하는 분은 없을 것이라 생각한다. 오일러-라그랑주를 한번 쓰면 원래 알던 식이 나온다. 그럼 뭐 이제 다 풀린 것처럼 보이는데, 왜냐면

![url=https://flic.kr/p/Gxe9f4](https://farm5.staticflickr.com/4561/26607646279_2f5ded811e_b.jpg)

이니까 그냥 양분 적분하면 될 것 같지만, 문제는 우변이다. 일단 그냥 써놓고 시작하자. 일단
 ![url=https://flic.kr/p/Dm79xw](https://farm5.staticflickr.com/4570/24512729748_ace70d9a5d_h.jpg)

이고, 우변의 루트 안쪽이 $\cos{\theta}=1-\sin^2{\dfrac{\theta}{2}}$임을 이용하면 $2\sin^2{\dfrac{\theta}{2}}-2\sin^2{\dfrac{\theta_{Max}}{2}}$가 되니까, $\sin{\dfrac{\theta}{2}}=\sin{\dfrac{\theta_{Max}}{2}}\sin{\phi}$로 치환하면 
 ![url=https://flic.kr/p/Gxe8ZV](https://farm5.staticflickr.com/4561/26607645459_047d6ca996_k.jpg)
 을 얻는다. 근데 우변, 적분 안된다. 정확히는 Gaussian Integral처럼 초등함수꼴로 부정적분이 나오지를 않는다. 꽤 유명해서 이름도 따로 있는데, 제 1종 타원적분, Elliptic Integral of the first kind라고 부르며, 다음과 같이 정의한다. 

 ![KakaoTalk_20171123_021755566](https://farm5.staticflickr.com/4541/38527134556_7d02c402a5_c.jpg)

다만 $\phi=\pi/2​$인 경우에 한하여 이를 Complete Elliptic Integral of the first kind 라고 부르고, 즉 $K(m)=F\big(\dfrac{\pi}{2},\sqrt{m}\big)​$으로 정의하여 다음과 같이 정의한다. 그림의 $F​$안의 $m​$의 루트가 빠진 것은 실수이다.

![KakaoTalk_20171123_021755942](https://farm5.staticflickr.com/4565/26807930769_75d6678662_c.jpg)

이걸 위 식에다 넣으면 임의의 진폭에 대한 주기의 공식을 얻고, $\theta_{Max}\rightarrow 0$이면 주기가 원래 작은각 근사를 사용해 유도했던 $2\pi\sqrt{\dfrac{l}{g}}$이 되는 걸 알 수 있다.