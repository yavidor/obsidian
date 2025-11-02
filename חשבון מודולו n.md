# הגדרה
עבור $a,n \in \mathbb{N}$ נגדיר 
השארית בחלוקת $a$ ב$n$ = $a(mod~n)$
$17\equiv 2\left( mod~3 \right)$
$2013 \equiv 1\left( mod~4 \right)$
# הגדרה כשדה
$\mathbb{Z}_{n}=\left\{ 0,1,2,\dots,n-1 \right\}$ שהן כל השאריות האפשריות בחלוקה ב-$n$ כ[[קבוצה]] (נשים לב שהקבוצה לא סגורה לחיבור וכפל הסטנדרטים שאנחנו מכירים)
על מנת להוכיח שאפשר להגדיר את $\mathbb{Z}_{n}$ כ[[שדה]] נבדוק שהקבוצה עונה על כל הדרישות
1. הקבוצה סגורה תחת חיבור וכפל מודולו n
2. אסוציאטיביות וקומוטטיביות
3. 0 אדיש חיבורי
4. קיים נגדי: לכל$0 \neq a \in Z_{n}$ מתרחש $a+(n-a)=0\left( mod~n \right)$, לגבי 0 הנגדי שלו הוא 0
5. 1 אדיש כפלי
6. קיום הופכי - **לא תמיד**
ולכן $\mathbb{Z}_{n}$ שדה $forall 0\neq a \in \mathbb{Z}_{n} \iff$ 
# דוגמה
$17(mod~3)=2$ כי $17=3 \cdot 5+2$
# משפטים
1.
$$
\begin{gather}
a,b \in \mathbb{N} \\
(a+b)\left( mod~n  \right) =(a\left( mod~n \right) +b\left( mod~n \right))\left( mod~n \right)
\end{gather}
$$
2.
$$
\begin{gather}
a,b \in \mathbb{N} \\
\left( a \cdot b \right) \left( mod~n \right) =\left( a \left( mod~n \right)  \right) \left( b\left( mod~n \right)  \right) \left( mod~n \right) 
\end{gather}
$$
## הוכחה
נסמן $a \left( mod~n \right)=r_{1}$ ו$b\left( mod~n \right)=r_{2}$
שקיימים $q_{1},q_{2} \in \mathbb{N}$ (או אפס) כך ש$a=q_{1} \cdot n + r_{1}$ ו$b=q_{2}\cdot n+r_{2}$
ניתן לכתוב ש$\left( a+b \right)=\left( q_{1}+q_{2} \right)n+r_{1}+r_{2}$
ואם נעשה על שני החלקים $mod~n$ נקבל ש$\left( a+b \right)=\left( r_{1}+r_{2} \right)\left( mod~n \right)$

> [!NOTE] נשים לב
> הסיבה ש$\left( q_{1}+q_{2} \right)n$ נעלם היא שמדובר בכפולה של $n$ ולכן המודולו של הביטוי הזה הוא 0

עם אותן הגדרות ראשונות נכתוב גם $\left( a \cdot b \right)= q_{1}q_{2}n^{2}+q_{1}nr_{2}+r_{1}q_{2}n+r_{1}r_{2}$
גם כאן אם נפעיל $mod~n$ על שני הצדדים כל ביטוי שכולל כפולה ב$n$ יעלם ויצא לנו
$\left( a \cdot b \right)=r_{1}r_{2}$