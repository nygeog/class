###Notes: from 
#INTRODUCTION to ALGORITHMS 3RD EDITION

---

#1 The Role of Algorithms in Computing
##1.1 Algorithms
* An algorithm is a sequence of computational steps that transform the input into the output.
* We can also view an algorithm as a tool for solving a well-specified computationalproblem.
* In general, an instance of a problemconsists of the input (satisfying whatever constraints are imposed in the problemstatement) needed to compute a solution to the problem

###Data structures
* A data structure is a way to storeand organize data in order to facilitate access and modifications.

###Parallelism* For many years, we could count on processor clock speeds increasing at a steady rate. Physical limitations present a fundamental roadblock to ever-increasing clock speeds, however: because power density increases superlinearly with clock speed,chips run the risk of melting once their clock speeds become high enough. In order to perform more computations per second, therefore, chips are being designed to contain not just one but several processing “cores.” We can liken these multicorecomputers to several sequential computers on a single chip; in other words, they are a type of “parallel computer.” In order to elicit the best performance from multicore computers, we need to design algorithms with parallelism in mind.

#2 Getting Started
##2.1 Insertion sort
* insertion sort, which is an efficient algorithm for sorting a small number of elements. Insertion sort works the way many people sort a hand ofplaying cards. We start with an empty left hand and the cards face down on the table. We then remove one card at a time from the table and insert it into thecorrect position in the left hand. To find the correct position for a card, we compare it with each of the cards already in the hand, from right to left. 

###Objects and attributes
* We typically organize compound data into **objects**, which are composed of **attributes**. We access a particular attribute using the syntax found in many object-oriented programming languages: the object name, followed by a dot, followed by the attribute name. For example, we treat an array as an object with the attribute length indicating how many elements it contains. To specify the number of elements in an array A, we write 

		A.length


##2.2 Analyzing algorithms

* Analyzing an algorithm has come to mean predicting the resources that the algorithm requires. Occasionally, resources such as;
	* **memory**, 
	* **communication bandwidth**, or 
	* **computer hardware** are of primary concern, but most often it is 
	* **computational time** that we want to measure.

* Generally, by analyzing several candidatealgorithms for a problem, we can identify a most efficient one. Such analysis may indicate more than one viable. 

###Analysis of insertion sort
* In general, the time taken by an algorithm grows with the size of the input, so it is traditional to describe the running time of a program as a function of the size of its input.

* **Input size** depends on the problem being studied. For many problems, such as sorting or computing discrete Fourier transforms, the most naturalmeasure is the number of items in the input—for example, the array size *n* for sorting. For many other problems, such as multiplying two integers, the best measure of input size is the total number of bits needed to represent the input in ordinary binary notation. Sometimes, it is more appropriate to describe the size of the input with two numbers rather than one. For instance, if the input to an algorithmis a graph, the input size can be described by the numbers of vertices and edges in the graph. We shall indicate which input size measure is being used witheach problem we study.

* **Running time** of an algorithm on a particular input is the number of primitive operations or “steps” executed. 

* One line may take a different amount of time than another line, but we shall assume that each execution of the i th line takes time ci, where ci is a constant. This viewpoint is in keeping with the RAM model, and it also reflects how the pseudocode would be implemented on most actual computers.

* **Worst-case running time**, that is, the longest running time for any input of size n.

* The **worst-case running time** of an algorithm gives us an upper bound on the running time for any input. Knowing it provides a guarantee that the algorithm will never take any longer. We need not make some educated guess about the running time and hope that it never gets much worse.

* For some algorithms, the **worst case** occurs fairly often. For example, in searching a database for a particular piece of information, the searching algorithm’s worst case will often occur when the information is not present in the database.In some applications, searches for absent information may be frequent.

* The **“average case”** is often roughly as bad as the worst case.

* In some particular cases, we shall be interested in the **average-case** running time of an algorithm; we shall see the technique of **probabilistic analysis** applied to various algorithms throughout this book. The scope of average-case analysis is limited, because it may not be apparent what constitutes an “average” input for a particular problem. Often, we shall assume that all inputs of a given size are equally likely. In practice, this assumption may be violated, but we can sometimes use a **randomized algorithm**, which makes random choices, to allow a probabilistic analysis and yield an expected running time. 

###Order of growth

* We shall now make one more simplifying abstraction: it is the **rate of growth**, or **order of growth**, of the running time that really interests us. We therefore consider only the leading term of a formula (e.g., an2), since the lower-order terms arerelatively insignificant for large values of n. We also ignore the leading term’s constant coefficient, since constant factors are less significant than the rate of growth in determining computational efficiency for large inputs. For insertion sort, whenwe ignore the lower-order terms and the leading term’s constant coefficient, we are left with the factor of $n^2$ from the leading term. We write that insertion sort has a worst-case running time of $ \theta (n^2) $ (pronounced “theta of n-squared”). We shall use $ \theta $ notation informally in this chapter, and we will define it precisely in Chapter 3.

* We usually consider one algorithm to be more efficient than another if its worstcaserunning time has a lower order of growth. Due to constant factors and lowerorderterms, an algorithm whose running time has a higher order of growth might take less time for small inputs than an algorithm whose running time has a lower order of growth. But for large enough inputs, a $ \theta (n^2) $ algorithm, for example, willrun more quickly in the worst case than a $\theta (n^3)$ algorithm.

##2.3 Designing algorithms

* We’ll use **divide-and-conquer** to design a sorting algorithm whose worst-case running time is muchless than that of *insertion sort*.

* One advantage of **divide-and-conquer** algorithms is that their running times are often easily determined.

###2.3.1 The divide-and-conquer approach

* Many useful algorithms are **recursive** in structure: to solve a given problem, they call themselves recursively one or more times to deal with closely related subproblems.

	* These algorithms typically follow a **divide-and-conquer** approach: they break the problem into several subproblems that are similar to the original problem but smaller in size, solve the subproblems recursively, and then combine these solutions to create a solution to the original problem.

* The **divide-and-conquer** paradigm involves three steps at each level of the recursion: 

	* **Divide** the problem into a number of subproblems that are smaller instances of thesame problem. 

	* **Conquer** the subproblems by solving them recursively. If the subproblem sizes aresmall enough, however, just solve the subproblems in a straightforward manner.

	* **Combine** the solutions to the subproblems into the solution for the original problem.
	
* The **merge sort** algorithm closely follows the divide-and-conquer paradigm. Intuitively,it operates as follows.

	* **Divide:** Divide the n-element sequence to be sorted into two subsequences of $n/2$ elements each.

	* **Conquer:** Sort the two subsequences recursively using merge sort.

	* **Combine:** Merge the two sorted subsequences to produce the sorted answer.

	
###2.3.2 Analyzing divide-and-conquer algorithms
* When an algorithm contains a recursive call to itself, we can often describe its running time by a **recurrence equation** or **recurrence**, which describes the overall running time on a problem of size $n$ in terms of the running time on smaller inputs.
* We can then use mathematical tools to solve the recurrence and provide bounds on the performance of the algorithm.


#Left-off page 35.

##Resources
* [LaTeX/Mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics)

##Reading Assignments:
###To Do: 

* 20150910: 3.1, 2.3, 4.0, 4.4 (optional), 4.5
* 20150915: 4.2, 10.2 (pp. 236-238)

###Complete 

* 20150910: 
* 20150908: 1.1, 2.1, 2.2