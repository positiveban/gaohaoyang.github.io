---
layout: post
title: "Controllability"
categories: 수학
tags: Linear-algebra
excerpt: "Controllable, Reachable."
---

controllability 혹은 reachability란 어떤 system에 입력을 가해서 초기 state x0로 부터 터미널 state xf 로 보낼 수 있는지에 대한 것이다.  

System의 dynamic equation으로부터 state transition matrix를 얻을 수 있는데, 보통 controllability (reachability)의 증명은 이 state transition의 관계식으로부터 시작된다.

예를들어 Linear system의 경우 dynamic equation은 아래와 같이 나타낸다.
 
$$
\\dot{x}=Ax+Bu
$$
(x: state, u: input, A,B: system matrices)

이를 적분하면, 터미널시간 tf의 state는 아래와 같이 얻어질 수 있다.

$$
x(t\_f)=e^{At}x(t\_0)+\\int\_{t\_0}^{t\_f}{e^{At}B(\\alpha)u(\\alpha)}d\\alpha
$$

위 수식 우변항에 있는 x(t0) term을 좌변항으로 넘기면,
$$
x(t\_f)-e^{At}x(t\_0)=\\int\_{t\_0}^{t\_f}{e^{At}B(\\alpha)u(\\alpha)}d\\alpha
$$

따라서 위 조건을 만족시키는 u가 존재하는지에 대한 해석이 controllability(or reachability) 이다.

Linear time invariant(LTI) system에서는 쉽게 해석이 되지만, LTV system에서는 해석이 복잡하며, 새로운 유형의 system이 제안될 때마다 controllability issue는 필연적으로 일어나게 된다.