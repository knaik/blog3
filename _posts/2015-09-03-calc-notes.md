---
layout: post
title:  "Calc 2 Notes"
date:   2015-09-08 10:20:00
categories: Calculus
---
#Day 2

Area under a curve could be anything, negative or positive
Area between two curves will always be positive

Even function has symmetry across y-axis
Odd function has symmetry across 	origin

even
\\( f(-x) = f(x) \\)

odd
\\( f(-x) = -f(x) \\)

6.1 problem 32
sketch region closed by 
\\( y = \frac{x}{x^2 + 1} \quad and \quad y = \frac{x}{5} \\)



![graph 1](https://raw.githubusercontent.com/knaik/knaik.github.io/master/images/graph1.gif)
![graph 2](https://raw.githubusercontent.com/knaik/knaik.github.io/master/images/graph2.gif)

We we integrate w/ respect to x axis because one function is always top and another is always bottom
we shouldn't with y because towards the top of the function, the outer function is it's own top and bottom

\\(top \quad - \quad bottom \quad  Area = 2 \int_0^2 \frac{x}{x^2 + 1} - \frac{x}{5} dx \\\
u = x^2 + 1 \quad du = 2xdx \quad make sure to switch boundries u(x) \\\
A = \int_1^5 1/u du - 2/5 \int_0^2 xdx \\\
ln u |_1^5 - (\frac{x^2}{5}) |_0^2 = ln5-4/5 \\)

Volume		y
_________|__b_________
|				 |						|
|				 |						| 
|------------|-----------------|	<--- slice 
|------------|-----------------|				delta y
|				 |						|
|				 |	a					|
----------------------------------------x

\\(V_slice = A_cross-section * A_y \\\
V_solid = \int_a^b A(y) dy \\\
Pyramid \quad A_pyr = 1/3 A_base height \\)

Sample Problem
Volume of pyramid with height 12 and square base of length 4
![pyramid 1](https://raw.githubusercontent.com/knaik94/knaik94.github.io/master/images/pyr1.gif)



12    /  |  \					a
      /	   |    \
    /___|___\				    b
  /		   |	   \
/_____|_____\			    c
0			x

a -> b = 12 - y
b -> c = y
similar triangles
12x = 24 - 2y
x = 2 - 1/6y

Area of slice 
\\( = (2x)^2 = (2(2 = 1/6 y ))^2 = (4 - 1/3 y)^2 \\\
V = \int_0^12 (4 - 1/3 y)^2 dy \\\
u = 4 - 1/3 y \quad du = 1/3 dy \\\
-3 \int_{u(0) = 4}^{u(12) = 0} u^2 du = -3 \frac{u^3}{3} |_4^0  = 64 \\)

An integral is an application of a reimann sum

Neighbourhoods are all equal density circles, find population

population density function

\\( population \quad density \quad function \quad p(r)  circle O \\\
|----|-\Delta r-|-------R \\\
take tiny ring, with tiny width, find numb of people living in ring\\\
width is \Delta r \\\
Area = \pi r^2 \\\
Area = 2 \pi r \Delta r * p(r) \\\
\int_0^R 2 \pi r p(r) dr \\)

Problem number 29, 6.2
Find population, if population density is given as
\\( p(r) = 4 (1+r^2) ^ {1/3} \\\ R = 10 \quad pop =? \\\
Population = 2 \pi \int_0^10  4 (1+r^2) ^ {1/3} dr \\\
u = 1 + r^2 \quad du = 2 r dr \\\
4 \pi \int_1^101 u^{1/3} du \\)

Average Value theorem
\\(A = \int_a^b f(x) dx = f(c) * (b-a) \\\
f(c) = \frac{1}{b - a} \int_a^b f(x) dx \\)
Assuming function is continuous, gives approximate value, as if it was rectangular











#Day 1

Two midterms and one final
first is  integration
second is series
final is cumulative
quizes and workshps

missed quiz = 0

Review

Indefinite integrals
\\( \int f(x) dx = F(x) + c \\) no limits

Definite integral
\\( \int_a^b f(x) dx \quad = A_1 - A_2 \quad (signed) \; area \; under \; graph \\\
\int_a^a f(x) dx = 0 \quad \quad \int_a^b f(x) dx = \int_a^c f(x) dx + \int_c^b f(x) dx \\\ 
\int_a^b f(x) dx = - \int_b^a f(x) dx \\)

A1 is area above x-axis (positive), A2 is area below x-axis (negative)

Fudamental Theorm of Calc

I.
\\( \int_a^b f(x) dx = F(x) |_a^b = F(b) - F(a) \\)

II.
\\( \frac{d}{dx} \int_a^x f(t) dt  = f(x) \\)

piece wise

```
2	| y1/\   y2
	|   /   \
	|_/___\_______
	| /1 3   4
-1	|/
	
```
geometry
calc

(3,2) , (0,-1)

m= y2 - y1 = 2 - -1
		------------------ = 1
		x2 - x1 = 3 - 0

y - 2 = x - 3
y = x - 1

so x intercept is 1

(1,0)
triangle

\\( \frac{b h}{2} = \frac{3 * 2}{ 2} = 3 = positive \quad Area \\\
\frac{b h}{2} = (1 * 1) / 2 \\\
3 - .5 = 2.5 \\)

\\(y_1 = x - 1 \quad y_2 = -2x+8\\)

integration, need to split, negative doesn't matter
\\(\int_0^3 y_1(x) dx + \int_3^4y_2(x) dx = 1.5 + 1 = 2.5 \\)

diff									int

\\( (e^x)' = e^x \quad \quad \int e^x dx = e^x +c \\\
sinx' = cosx						\int cosx = sinx + c \\\
cosx = -sinx						sinx = -cosx  +c \\\
tanx = sec^2 x 					sec^2 x = tanx + c\\\
x^n ' = nx^{n-1}				x^n = x^n+1/n+1 + c \\\
lnx' = 1/x 						1/x  = ln|x| + c\\\
b^x ' = b^x ln(b) \\\
arctan x'  = 1 / 1 + x^2 \\\
chain \quad rule \\\
\frac{d}{dx} [f(u)] = f'(u) *  u' \\\
subsitution
\int f'(u) * u' du = f(u) + c\\\
\\)

\\(
1. \int x sqrt{x^2 +9} dx \\\
2. \int_2^7 \\)







