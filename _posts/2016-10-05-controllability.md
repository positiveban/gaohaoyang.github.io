---
layout: post
title: "Controllability"
categories: 수학
tags: Linear-algebra
excerpt: "Controllable, Reachable."
---

controllability 혹은 reachability란 어떤 system에 입력을 가해서 초기 state x0로 부터 터미널 state xf 로 보낼 수 있는지에 대한 것이다.  

System의 dynamic equation으로부터 state transition matrix를 얻을 수 있는데, 보통 controllability (reachability)의 증명은 이 state transition matrix로부터 시작된다.

예를들어 Linear system의 경우 dynamic eqaution을 보통 아래와 같이 나타낼 수 있다.

 
$$
\\dot{x}=Ax+Bu
$$

이를 적분하면, 터미널시간 tf의 state는 아래와 같이 얻어질 수 있다.

$$
x(t\_f)=e^{At}x(t\_0)+\\int\_{t\_0}^{t\_f}{e^{At}B(\\alpha)u(\\alpha)}d\\alpha
$$