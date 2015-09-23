CSOR W4246 - Fall, 2015 - Daniel M. Sheehan (dms2203)

#HW1 - Theoretical part

(10 points)

#2. 
(20 points) 
Use the Master theorem to give tight asymptotic bounds for the following recurrences.

* $ T(n) = 4T(n/2) + n^2 $

* $ T(n) = 8T(n/2) + n^3 $ 

* $ T(n) = 11T(n/4) + n^2 $


#3.
(20 points) 
Consider the following recursive algorithm. On input a list of distinct numbers, the algorithm runs in three phases.

* In the **first** phase; the first $2/3$ elements of the list are sorted (recursively). 
* In the second phase, the **last** $2/3$ elements are sorted (recursively).

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
|$ \sqrt{log n}     $|$ log log n        $|-|-|-|-|-|
|$ \sqrt{n} + log n $|$ n^{2/3} + 10     $|-|-|-|-|-|
|$ n^2 2^n          $|$ 3^n              $|-|-|-|-|-|
|$ n log n          $|$ n^2 \over logn   $|-|-|-|-|-|
