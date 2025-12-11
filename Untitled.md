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
\end{array}\right) \\  \\
\xrightarrow{R_{3}\to R_{3}-2R_{1}}\left(\begin{array}{cccc|c}
1 & a & a & a & b \\
2 & 1+a & b+2a & b+2a & a+2b \\
0 & 1 & a & a^{2}-b^{2}+b & a \\
0 & 0 & 0 & a-2b & a
\end{array}\right) \\ \\
\xrightarrow{R_{2}\leftrightarrow R_{3}}\left(\begin{array}{cccc|c}
1 & a & a & a & b \\
0 & 1 & a & a^{2}-b^{2}+b & a \\
2 & 1+a & b+2a & b+2a & a+2b \\
0 & 0 & 0 & a-2b & a
\end{array}\right) \\ \\
\xrightarrow{R_{2} \to R_{2}- 2R_{1}}\left(\begin{array}{cccc|c}
1 & a & a & a & b \\
0 & 1 & a & a^{2}-b^{2}+b & a \\
0 & 1-a & b & b & a \\
0 & 0 & 0 & a-2b & a
\end{array}\right) \\ \\
\xrightarrow{R_{3} \to R_{3}- \left( 1-a \right) R_{2}}\left(\begin{array}{cccc|c}
1 & a & a & a & b \\
0 & 1 & a & a^{2}-b^{2}+b & a \\
0 & 0 & b-a+a^{2} & -a^{2}+b^{2}+a^{3}-ab^{2}+ab &a^{2} \\
0 & 0 & 0 & a-2b & a
\end{array}\right) \\
\end{gather}
$$
Notice that I could multiply by $(1-a)$ since if it is 0 it doesn't matter, I just did nothing
When is one of the following true
$$
\begin{cases}
a-2b=a=0 \\
a=a-b=a^{2}-b^{2}=0 \\
1-a=b=a=0
\end{cases}
$$
when $a=b=0$, then $r\left( A \right)=r\left( A^{*} \right)=2<n$
When $a=2b\neq 0$ $r\left( A \right)\neq r\left( A^* \right)\implies$ No solutions
For everything else, a single solution

$$
\begin{gather}
-a^{2}+\left( a-a^{2} \right)^{2}+a^{3}-a\left( a-a^{2} \right)^{2}+a\left( a-a^{2} \right) \\
=-a^{2}+a^{2}-2a^{3}+a^{4}+a^{3}-a(a^{2}-2a^{3}+a^{4})+a^{2}-a^{3} \\
=-a^{2}+a^{2}-2a^{3}+a^{4}+a^{3}-a^{3}+2a^{4}-a^{4}+a^{2}-a^{3} \\
=
\end{gather}
$$
1. אדיש כפלי
2. אדיש חיבור
3. קומטטיבי חיבור
4. קומוטטיבי כפל
5. אסוציאטיבי חיבור
6. אסוציאטיבי כפל
7. קיום נגדי
8. קיום הופכי
9. סגירות חיבור
10. סגירות כפל
11. דיסטריבוטיביות
12. אפס הוא לא 1
