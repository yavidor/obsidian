Bla bla this code
```c
void f2(int n) {
	double i = 2;
	while (n >= i) {
		i *= i*i;
		i = sqrt(i);
	}
}
```
Assume that the time complexity of `sqrt` is
$$
\begin{gather}
sqrt(n)=\Theta \left( \log n \right)  \\
\end{gather}
$$
And that the space complexity of `sqrt`
$$
sqrt(n) = \Theta \left( 1 \right) 
$$
Find the space and time complexity of `f2` in regards to $n$

# Solution
Since the function is using a constant number of variable, and every call to `sqrt` has constant memory consumption as well, the memory complexity of `f2` is $\Theta \left( 1 \right)$

We'll notice that at the end of each iteration we get $i_{t+1}=i_{t^{\frac{3}{2}}}$ (translator note: Maybe it's $i_{t+1}=i_{t}^{\frac{3}{2}}$ It is unclear from what they wrote, and I'm not sure what the meaning is anyways). There fore in the $t$-th iteration we get $i=2^{\frac{3}{2}^{t}}$
The run ends when $i_{t}>n$, we'll find $t$:
$$
\begin{gather}
2^{\frac{3}{2}^{t}}>n & /\log() \\
\frac{3}{2}^{t}\cancel{\log \left( 2 \right) }>\log \left( n \right) \\
t\cdot \log \left( \frac{3}{2} \right)  > \log \left( \log \left( n \right)  \right) 
\end{gather}
$$
Because we are looking for the smallest $t$ that meets this condition, we'll get
$$
\begin{gather}
\frac{3}{2}^{t}=\Theta \left( \log n \right)  \\
t=\Theta \left( \log \log n \right) 
\end{gather}
$$
At every iteration there is a call to `sqrt` that we know gives $\Theta \left( \log \left( i \right) \right)$ runtime. Therefore the total runtime is
$$
\log \left( 2^{\frac{3}{2}^{0}} \right)+\log \left( 2^{\frac{3}{2}^{1}} \right)  +\ldots+\log \left( 2^{\frac{3}{2}^{t}} \right) =\sum_{i=0}^{t} \log \left( 2^{\frac{3}{2}^{i}} \right) = \sum_{i=0}^{t} \frac{3}{2}^{i} \cancel{\log \left( 2 \right) }
$$
This is the sum of a geometric series
$$
\frac{\frac{3}{2}^{t}-1}{\frac{3}{2}-1}=\Theta \left( \frac{3}{2}^{t} \right) =\Theta \left( \log n \right) 
$$