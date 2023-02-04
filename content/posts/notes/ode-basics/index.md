---
title: "ODE Basics"
date: 2023-01-30T23:48:46+08:00
draft: false
tags: ["Math", "Mathematical Analysis", "ODE" ]
---

# 常微分方程初步(ODE)
---

[ ![](ode-basics.png "Flowchart of solving simple ODE equations") ](ode-basics.png)
Flowchart of solving simple ODE equations

### [^1]

这里的齐次方程指可以化为$\frac{dy}{dx}=\phi\left({y \over x}\right)$的一阶微分方程, 而”一阶线性齐次方程”是在线性的基础上，没有仅为x的函数的项，二者含义不同。

### [^2]

对于二阶线性齐次微分方程

 

$$
\begin{equation}
y''+p(x)y'+q(x)y=0,
\end{equation}
$$

可以发现

$$
\frac{\mathrm d}{\mathrm d x}W(x)=-p(x)W(x),
$$

所以有

$$
W(x)=W(x_0)\mathrm{e}^{-\int_{x_0}^x p(x)\,\mathrm{d}x}.
$$

若已知 $y_1 (x)$, 则

$$
\frac{\mathrm d}{\mathrm d x}\left(\frac{y_2(x)}{y_1(x)}\right)=\frac{W(x)}{y_1^2(x)}=\frac{W(x_0)\mathrm{e}^{-\int_{x_0}^x p(x)\,\mathrm{d}x}}{y_1^2(x)},
$$

两侧积分得 $\frac{y_2}{y_1}$, 进而可得 $y_2$

### [^3]

已知齐次方程的基本解组 $y_1(x),\,y_2(x)$, 设非齐次方程有通解

$$
y_0(x)=C_1(x)y_1(x)+C_2(x)y_2(x),
$$

$$
y_0'(x)=C_1y_1'+C_2y_2'+C_1'y_2+C_2'y_2
$$

为了求二阶导时避免出现 $C_1, C_2$的高阶导数, 不妨令

 

$$
\begin{equation}C_1’y_1+C_2’y_2=0\end{equation}
$$

则

$$
y_0'(x)=C_1y_1'+C_2y_2'
$$

$$
y_0''(x)=C_1y_1''+C_2y_2''+C_1'y_1'+C_2'y_2'
$$

将它们代入齐次方程, 得

$$
\begin{equation}C_1'y_1'+C_2'y_2'=f(x).\end{equation}
$$

联立式(2), (3)即可求得 $C_1,C_2$.