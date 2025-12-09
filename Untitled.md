$$
\begin{cases}
x+ay+az+aw=b \\
2x+\left( 1+a \right) y+\left( b+2a \right) z+\left( b+2a \right) w=a+2b \\
2x+\left( 1+2a \right) y+3az+\left( a^{2}-b^{2}+b+2a \right) w=a+2b \\
x+ay+az+\left( 2a-2b \right) w=a+b
\end{cases}
$$
$$
\begin{gather}
\left(\begin{array}{cccc|c}
1 & a & a & a & b \\
2 & 1+a & b+2a & b+2a & a+2b \\
2 & 1+2a & 3a & a^{2}-b^{2}+b+2a & a+2b \\
1 & a & a & 2a-2b & a+b
\end{array}\right) \\ \\
\xrightarrow{R_{4}\to R_{4}-R_{1}}\left(\begin{array}{cccc|c}
1 & a & a & a & b \\
2 & 1+a & b+2a & b+2a & a+2b \\
2 & 1+2a & 3a & a^{2}-b^{2}+b+2a & a+2b \\
0 & 0 & 0 & a-2b & a
\end{array}\right) \\ \\
\xrightarrow{R_{3}\to R_{3}-R_{2}}\left(\begin{array}{cccc|c}
1 & a & a & a & b \\
2 & 1+a & b+2a & b+2a & a+2b \\
0 & a &a-b & a^{2}-b^{2} & 0 \\
0 & 0 & 0 & a-2b & a
\end{array}\right) \\ \\
\xrightarrow{R_{2}\to R_{2}-2R{1}}\left(\begin{array}{cccc|c}
1 & a & a & a & b \\
0 & 1-a & b & b & a \\
0 & a &a-b & a^{2}-b^{2} & 0 \\
0 & 0 & 0 & a-2b & a
\end{array}\right) \\
\end{gather}
$$
