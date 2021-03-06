---
id: 512
title: '원형막의 진동 &#8211; 극좌표계에서의 변수분리형 미분방정식 (Helmholtz)'
date: 2016-03-28T12:04:42+00:00
author: Abraxas Academy
layout: post
tags: Physics
---
헬름홀츠 방정식은 원통좌표계에서 변수분리를 이용하여 문제를 풀때 등장하는 미분방정식입니다. 예시를 드는게 빠르겠군요. 원형막이 진동하는 상황을 생각해 봅시다.

 

파동방정식을 세우면,

 

 

 \begin{equation}
 \nabla^2 z= \frac{1}{v^2}{ \partial^2 z \over \partial t^2 }
 \end{equation}

 

막의 각 지점의 변위함수 $z(r,\theta,t)$를 $F(r,\theta)T(t)$로 다시 씁시다.

그럼 다음과 같이 변형 가능합니다. 

 

 

 \begin{equation}
 \begin{split}
 &\nabla^2 F\cdot T=\frac{1}{v^2}{ \partial^2 F\cdot T \over \partial t^2 }\\ \Rightarrow \qquad T&\nabla^2 F=\frac{1}{v^2}F\frac{d^2T}{dt^2}\\ \Rightarrow \qquad \frac{1}{F}&\nabla^2 F=\frac{1}{v^2}\frac{1}{T}\frac{d^2T}{dt^2}
 \end{split}
 \end{equation}

 

 

이렇게 된다면, 좌변은 모두 $F$에 관한 식이고, 우변은 $T$에 관한 식이므로 양변이 상수가 되어야 합니다. 그 상수를 $-k^2$이라고 두면, 다음 두 식을 얻습니다. (여기서 $F$의 미분방정식이 바로 Helmholtz 방정식입니다.)

 \begin{equation}
 \nabla^2F+k^2 F=0,\quad \ddot{T}+k^2v^2T=0
 \end{equation}

 이제 다시 $ F = R(r) \Theta (\theta )$로 놓고 극좌표에서의 Laplacian 을 이용하면,

 \begin{equation}
 \begin{split}
 &\frac{1}{r}\frac{\partial}{\partial r}\Big(r\frac{\partial R\Theta}{\partial r}\Big)+\frac{1}{r^2}\frac{\partial^2 R\Theta}{\partial \theta^2}=0\\
 \Rightarrow\qquad &\frac{r}{R}\frac{d}{dr}\Big(r\frac{dR}{dr}\Big)+\frac{1}{\Theta}\frac{d^2 \Theta}{d \theta^2}+k^2r^2=0
 \end{split}
 \end{equation} 

 

식 (3)을 만들 때와 같은 방법을 사용하면, ($n$은 자명히 $n\in\mathbb{N}\cup\{0\}$입니다. 한 시간과 한 지점에서 $z$의 값은 하나여야 하기 때문입니다.) 

\begin{equation}
 \frac{d^2 \Theta}{d \theta^2}=-n^2 \Theta,\quad \therefore \Theta=\sin n\theta
 \end{equation}

(물론 일반해는 아닙니다만, 중요하지 않으므로 넘어갑시다.)

 

 그렇다면 이제 풀어야하는 미분방정식은 

\begin{equation}
 r\frac{d}{dr}\Big(r\frac{dR}{dr}\Big)+(k^2r^2-n^2)R=r\frac{dR}{dr}+r^2\frac{d^2R}{dr^2}+(k^2r^2-n^2)R=0
 \end{equation}
 Mathematica를 이용해봅시다.

```mathematica
Dsolve[x*y'[x]+x^2*y''[x]+(k^2*x^2-n^2)y[x]==0,y[x],x]
```

다음과 같이 출력됩니다.

```mathematica
BesselJ[n,kx]C[1]+BesselY[n,kx]C[2]
```

따라서 미분 방정식의 해가 다음과 같음을 알 수 있습니다.
 \begin{equation}
 R(r)=c_1J_n(kx)+c_2Y_n(kx)
 \end{equation}

여기서 $J_n(x)$는 제 1종 베셀함수, $Y_n(x)$는 제 2종 베셀 함수입니다. 여기서는 이 두 함수가 Helmholtz 방정식의 해가 된다는 것 정도만 알고 넘어갑시다. 다음과 같이 정의됩니다.\begin{equation}
 J_n(x)=\sum_{s=0}^{\infty}\frac{(-1)^s}{s!\Gamma(n+s+1)}\Big(\frac{x}{2}\Big)^{n+2s}
 \end{equation} 

 \begin{equation}
 Y_n(x)=\lim_{\nu \to n}\frac{J_\nu(x)\cos \nu\pi-J_{-\nu}(x)}{\sin{\nu\pi}}
 \end{equation} 

이제 남은 일은 적절하게 경계조건에 맞추어 상수를 결정하는 일 뿐입니다. 이 포스팅에서는 생략하도록 하겠습니다. (많은 경우에서 $\displaystyle \lim_{n \rightarrow \infty}=-\infty$ 임을 이용하면, $c_2=0$임을 알 수 있습니다.)

가능한 해 중 몇가지의 그래프를 아래에 첨부합니다 (당연하지만 $t$가 고정입니다.)

![](https://farm5.staticflickr.com/4710/39731182462_8245e10e96_z.jpg)

![](https://farm5.staticflickr.com/4611/39731182222_646aee053e_z.jpg)

![](https://farm5.staticflickr.com/4668/39731182052_c3943e77e9_z.jpg)

![](https://farm5.staticflickr.com/4612/38864189995_20a42e62bd_z.jpg)





