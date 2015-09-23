###Notes: from 
#INTRODUCTION to ALGORITHMS 3RD EDITION

---

#1 The Role of Algorithms in Computing
##1.1 Algorithms
* An algorithm is a sequence of computational steps that transform the input into the output.
* We can also view an algorithm as a tool for solving a well-specified computational
* In general, an instance of a problem

###Data structures
* A data structure is a way to store

###Parallelism

#2 Getting Started
##2.1 Insertion sort
* insertion sort, which is an efficient algorithm for sorting a small number of elements. Insertion sort works the way many people sort a hand of

###Objects and attributes
* We typically organize compound data into **objects**, which are composed of **attributes**. We access a particular attribute using the syntax found in many object-oriented programming languages: the object name, followed by a dot, followed by the attribute name. For example, we treat an array as an object with the attribute length indicating how many elements it contains. To specify the number of elements in an array A, we write 

		A.length


##2.2 Analyzing algorithms

* Analyzing an algorithm has come to mean predicting the resources that the algorithm requires. Occasionally, resources such as;
	* **memory**, 
	* **communication bandwidth**, or 
	* **computer hardware** are of primary concern, but most often it is 
	* **computational time** that we want to measure.

* Generally, by analyzing several candidate

###Analysis of insertion sort
* In general, the time taken by an algorithm grows with the size of the input, so it is traditional to describe the running time of a program as a function of the size of its input.

* **Input size** depends on the problem being studied. For many problems, such as sorting or computing discrete Fourier transforms, the most natural

* **Running time** of an algorithm on a particular input is the number of primitive operations or “steps” executed. 

* One line may take a different amount of time than another line, but we shall assume that each execution of the i th line takes time ci, where ci is a constant. This viewpoint is in keeping with the RAM model, and it also reflects how the pseudocode would be implemented on most actual computers.

* **Worst-case running time**, that is, the longest running time for any input of size n.

* The **worst-case running time** of an algorithm gives us an upper bound on the running time for any input. Knowing it provides a guarantee that the algorithm will never take any longer. We need not make some educated guess about the running time and hope that it never gets much worse.

* For some algorithms, the **worst case** occurs fairly often. For example, in searching a database for a particular piece of information, the searching algorithm’s worst case will often occur when the information is not present in the database.In some applications, searches for absent information may be frequent.

* The **“average case”** is often roughly as bad as the worst case.

* In some particular cases, we shall be interested in the **average-case** running time of an algorithm; we shall see the technique of **probabilistic analysis** applied to various algorithms throughout this book. The scope of average-case analysis is limited, because it may not be apparent what constitutes an “average” input for a particular problem. Often, we shall assume that all inputs of a given size are equally likely. In practice, this assumption may be violated, but we can sometimes use a **randomized algorithm**, which makes random choices, to allow a probabilistic analysis and yield an expected running time. 

###Order of growth

* We shall now make one more simplifying abstraction: it is the **rate of growth**, or **order of growth**, of the running time that really interests us. We therefore consider only the leading term of a formula (e.g., an2), since the lower-order terms are

* We usually consider one algorithm to be more efficient than another if its worstcase

##2.3 Designing algorithms

* We’ll use **divide-and-conquer** to design a sorting algorithm whose worst-case running time is muchless than that of *insertion sort*.

* One advantage of **divide-and-conquer** algorithms is that their running times are often easily determined.

###2.3.1 The divide-and-conquer approach

* Many useful algorithms are **recursive** in structure: to solve a given problem, they call themselves recursively one or more times to deal with closely related subproblems.

	* These algorithms typically follow a **divide-and-conquer** approach: they break the problem into several subproblems that are similar to the original problem but smaller in size, solve the subproblems recursively, and then combine these solutions to create a solution to the original problem.

* The **divide-and-conquer** paradigm involves three steps at each level of the recursion: 

	* **Divide** the problem into a number of subproblems that are smaller instances of the

	* **Conquer** the subproblems by solving them recursively. If the subproblem sizes are

	* **Combine** the solutions to the subproblems into the solution for the original problem.
	
* The **merge sort** algorithm closely follows the divide-and-conquer paradigm. Intuitively,

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