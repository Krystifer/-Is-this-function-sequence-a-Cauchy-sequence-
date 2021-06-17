# <center>¿Is this function sequence a Cauchy sequence?</center>

 Given the metric space C([-1,1]) (continuous functions on the closed interval [-1,1]) with the metric defined by:
 
 <center><img src="https://latex.codecogs.com/gif.latex?||x||=\max_{t\in&space;[-1,1]}&space;|x(t)|" title="||x||=\max_{t\in [-1,1]} |x(t)|" /></center>

 This code checks with the help of a color map, if a given function sequence is or not a Cauchy sequence in C([-1,1]), (See [1](https://en.wikipedia.org/wiki/Cauchy_sequence)), where this function sequence is defined recursively, that is
 
 <img src="https://latex.codecogs.com/gif.latex?x_{n&plus;1}(t)&space;=&space;T(x_n(t))" title="x_{n+1}(t) = T(x_n(t))" />
 
Here T is the 'rule' of the sequence, given an initial function <a href="https://www.codecogs.com/eqnedit.php?latex=x_0" target="_blank"><img src="https://latex.codecogs.com/gif.latex?x_0" title="x_0" /></a> we can compute any other term of the sequence. In this code, the initial condition must be a user-defined function, 'initial_func'. The composition process is computed by 'comp_func' using recursion.
 
In order to determining if the term  

<a href="https://www.codecogs.com/eqnedit.php?latex=||x_{n}(t)-x_{m}(t)||" target="_blank"><img src="https://latex.codecogs.com/gif.latex?||x_{n}(t)-x_{m}(t)||" title="||x_{n}(t)-x_{m}(t)||" /></a> 

is as small as possible whenever n,m>N for N>>0, we need to determine the maximum (due to the way the norm is defined) of

<img src="https://latex.codecogs.com/gif.latex?f(t)=|x_{n}(t)-x_{m}(t)|" title="f(t)=|x_{n}(t)-x_{m}(t)|" /> 

for t in [-1,1], this is accomplished by the 'norm' function, minimizing -f(t).

The result is a color map and it must be interpreted as:
- If colors for n and m being big numbers does fit zero, then T is likely to be a Cauchy sequence.
- If colors for n and m being big numbers doesn't fit zero, then T isn't likely to be a Cauchy sequence.

The given example shows that 

<img src="https://latex.codecogs.com/gif.latex?(Tx)(t)=\sin(\pi&space;x(t))" title="(Tx)(t)=\sin(\pi x(t))" />

Isn't likely to be a Cauchy sequence. 
