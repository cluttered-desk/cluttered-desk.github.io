---
id: 639
title: '비행기로 여행하기 위한 최단 경로는? &#8211; 변분법과 Beltrami Identity의 응용'
date: 2016-10-25T00:59:16+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
아마 과학동아 등지에서 너무 많이 다뤄서 이제는 진부하게 느껴질지도 모르는 이 주제는- 간단합니다. (평면에서) 어느 두 점을 연결하는 가장 짧은 경로는, 자명히 직선인데, 그렇다면 구면 위에서는 어떨까요? 이 질문에 대한 대답은 이 질문에 대한 대답과 같죠.

 

**"인천에서 출발한 비행기가 LA에 가려고 하는데, 가장 빨리 가고 싶다면 어떤 경로로 가야 할까요?"**

 

물론 현실에서는 영공 문제, 불어대는 바람이며 지구가 정확한 구 모양이 아니라는 등의 문제 때문에 더욱 복잡해질 테지만, 여기서는 깔끔히 무시합시다.

그렇다면, 물론 답은 널리 알려진 것처럼, 대원상의 경로입니다. 대원의 정의는 [이 링크](https://en.wikipedia.org/wiki/Great_circle) 를 참고해 주세요.

그러니까 구의(지구의) 중심, 인천, LA를 지나는 평면과 지구의 교선을 따라가면 가장 짧은 경로로 여행을 마칠 수 있다는 이야기입니다. 그렇다면 증명은 어떻게 해야 할까요? 역시 변분법을 사용해야겠죠.

 

구면좌표계에서 미소 길이는 다음과 같습니다. 

 

 \begin{equation}
 (ds)^2=(dr)^2+(rd\phi)^2+(r\sin{\phi}d\theta)^2
 \end{equation}
 구면 위의므로 $r=a$라 하면 $dr=0$ 입니다. 따라서
 \begin{equation}
 (ds)^2=(ad\phi)^2+(a\sin{\phi}d\theta)^2=a^2((d\phi)^2+(\sin{\phi}d\theta)^2)
 \end{equation}
 이제 범함수 $J$를 정의합시다.
 \begin{equation}
 J=\int{ds}=a\int{a\sqrt{(d\phi)^2+(\sin{\phi}d\theta)^2}}=a\int_{\theta_1}^{\theta_2}{\sqrt{(\dfrac{d\phi}{d\theta})^2+(\sin{\phi})^2}}d\theta
 \end{equation}
 여기서 Beltrami Identity를 이용해야 합니다. Beltrami Identity는 아래와 같습니다.
 \begin{equation}
 \dfrac{d}{dx}\Big(f-y^{\prime}\dfrac{\partial f}{\partial y^{\prime}}\Big)=0 \quad when\quad \dfrac{\partial f}{\partial x}=0
 \end{equation}
 종종 Second form of the Euler-Lagrange Equation 이라고도 불리우는 이 식의 증명은 아래와 같습니다.
 다음 두 식이 성립합니다.
 \begin{equation}
 \frac{df}{dx}=y^{\prime}\frac{\partial f}{\partial y}+y^{\prime \prime}\frac{\partial f}{\partial y^{\prime}}+\frac{\partial f}{\partial x}
 \end{equation}
 체인룰을 쓰면 쉽게 얻을 수 있습니다. 다음으로
 \begin{equation}
 \frac{d}{dx}\Big(y^{\prime}\frac{\partial f}{\partial y^{\prime}}\Big)=y^{\prime \prime}\frac{\partial f}{\partial y^{\prime}}+y^{\prime}\frac{d}{dx}\frac{\partial f}{\partial y^{\prime}}
 \end{equation}
 소거하면,
 \begin{equation}
 \frac{df}{dx}=y^{\prime}\frac{\partial f}{\partial y}+\frac{d}{dx}\Big(y^{\prime}\frac{\partial f}{\partial y^{\prime}}\Big)-y^{\prime}\frac{d}{dx}\frac{\partial f}{\partial y^{\prime}}+\frac{\partial f}{\partial x}
 \end{equation}
 이항하면
 \begin{equation}
 0=y^{\prime}\Big(\frac{\partial f}{\partial y}-\frac{d}{dx}\frac{\partial f}{\partial y^{\prime}}\Big)+\frac{d}{dx}\Big(y^{\prime}\frac{\partial f}{\partial y^{\prime}}-f\Big)+\frac{\partial f}{\partial x}
 \end{equation}
 가 되고, 첫번째 항은 Euler-Lagrange eq. 에 의해 0이 되므로 증명이 끝납니다. 

 

다시 본론으로 돌아와서,

Beltrami Identity를 적용하면

 

 \begin{equation}c(constant)=\sqrt{(\dfrac{d\phi}{d\theta})^2+\sin^2{\phi}}-\dfrac{(\dfrac{d\phi}{d\theta})^2}{\sqrt{(\dfrac{d\phi}{d\theta})^2+\sin^2{\phi}}}\end{equation}

를 얻게 되고, 다시 한번 더 정리하면 다음을 얻습니다.

\begin{equation}\sin^2{\phi}=c\sqrt{((\dfrac{d\phi}{d\theta})^2+\sin ^2{\phi})}\end{equation}

 따라서

\begin{equation}\frac{d\theta}{d\phi}=\dfrac{c\cdot \csc^2{\phi}}{\sqrt{1-c^2\csc^2{\phi}}}\end{equation}

이므로 

 \begin{equation}\int d\theta=\int \dfrac{c\cdot \csc^2{\phi}}{\sqrt{1-c^2\csc^2{\phi}}}d\phi=\theta=\int \dfrac{c\cdot \csc^2{\phi}}{\sqrt{1-c^2}\sqrt{1-(c^2/1-c^2)(\cot^2{\phi})}}d\phi\end{equation}

 

여기서 $(c/\sqrt{1-c^2})\cot{\phi}=t$로 치환하면, 식 $(12)$는

 

 

 \begin{equation}\int \frac{-t}{\sqrt{1-t^2}}dt=-\sin^{-1}t+\gamma=-\sin^{-1}{((c/\sqrt{1-c^2})\cot{\phi})}+\gamma=-sin^{-1}{\dfrac{\cot{\phi}}{\alpha}}+\gamma\end{equation}

 가 되므로 따라서,
 \begin{equation}\cot{\phi}=\alpha\sin{(\gamma-\theta)}\end{equation}
 전개하고 정리하면

 

 

 

 \begin{equation}\cos{\phi}=\alpha\sin{\phi}({\sin{\gamma}\cos{\theta}-\sin{\theta}\cos{\gamma})}\end{equation}

양변에 반지름 $a$를 곱하고

\begin{equation}a\cos{\phi}=a\alpha\sin{\phi}({\sin{\gamma}\cos{\theta}-\sin{\theta}\cos{\gamma})}\end{equation}

구면좌표계와 직교좌표계의 관계식을 이용하면,

\begin{equation}z=\alpha\sin{\gamma}x-\alpha\cos{\gamma}y\end{equation}

로 원점을 지나는 평면의 방정식을 얻어 최단경로가 대원이라는 결론을 얻습니다.