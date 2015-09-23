CSOR W4246 - Fall, 2015 - Daniel M. Sheehan (dms2203)
<center>
#HW1 - Theoretical partOut: Thursday, September 17, 2015Due: 8pm, Monday, September 28, 2015</center>Please keep your answers clear and concise. For all algorithms you suggest, you must give the best upper bound that you can for the running time. You should always describe your algorithm clearly in English. You are encouraged to write pseudocode for all your algorithms.You are encouraged to brainstorm with a small number of your classmates. However collaboration is limitedto discussion of ideas only and you should write up the solutions entirely on your own. You should list your collaborators on your write-up. If you do not type your solutions, be sure that your hand-writing is legible, your scan is high-quality (if applicable) and your name is clearly written on your homework.If you submit your assignment electronically, please submit a .pdf file. Other file formats (such as .jpg, .doc, .c, or .py) will not be graded, and will automatically receive a score of 0.
#1. 
(10 points)Certificate Students may skip. I'm a certificate student. Skipping.

#2. 
(20 points) 
Use the Master theorem to give tight asymptotic bounds for the following recurrences.

* $ T(n) = 4T(n/2) + n^2 $

* $ T(n) = 8T(n/2) + n^3 $ 

* $ T(n) = 11T(n/4) + n^2 $
* $ T(n) = 7T(n/3) + n $

#3.
(20 points) 
Consider the following recursive algorithm. On input a list of distinct numbers, the algorithm runs in three phases.

* In the **first** phase; the first $2/3$ elements of the list are sorted (recursively). 
* In the second phase, the **last** $2/3$ elements are sorted (recursively).* Finally, in the third phase, the **first** $2/3$ elements are sorted (recursively) again. 

---

* Derive a recurrence describing the running time of the algorithm and use the recurrence to bound its asymptotic running time. 

* Would you use this algorithm in your next application?

#4. 
(30 points) 
In the table below, indicate the relationship between functions $f$ and $g$ for each pair $(f,g)$ by writing **yes** or **no** in each box. For example, if $f = O(g)$ then write **yes** in the first box.

| $f$ | $g$ | $O$  | $o$ | $ \Omega $ | $ \omega $ | $ \theta $ |
|-----|-----|-----|-----|-----|-----|-----|
|$ 10 log n         $|$ log^3 n          $|-|-|-|-|-|
|$ n log (2n)       $|$ n log n          $|-|-|-|-|-|
|$ \sqrt{log n}     $|$ log log n        $|-|-|-|-|-||$ 10n^2 + log n    $|$ n^2 + 11 log^3 n $|-|-|-|-|-|
|$ \sqrt{n} + log n $|$ n^{2/3} + 10     $|-|-|-|-|-|
|$ n^2 2^n          $|$ 3^n              $|-|-|-|-|-||$ n^{1/3}          $|$ (log n)^2        $|-|-|-|-|-|
|$ n log n          $|$ n^2 \over logn   $|-|-|-|-|-||$ n!               $|$ n^n              $|-|-|-|-|-||$ log n!           $|$ log n^n          $|-|-|-|-|-|

