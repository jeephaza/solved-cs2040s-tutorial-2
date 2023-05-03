Download Link: https://assignmentchef.com/product/solved-cs2040s-tutorial-2
<br>
<h1>Problem 1.           Sorting Review</h1>

<ul>

 <li>How would you implement insertion sort recursively? Analyse the time complexity by formulating a recurrence relation.</li>

 <li>Suppose that the pivot choice is the median of the first, middle and last keys, can you find a bad input for QuickSort?</li>

 <li>Are any of the partitioning algorithms we have seen for QuickSort stable? Can you design a stable partitioning algorithm? Would it be efficient?</li>

 <li>Consider a QuickSort implementation that uses the 3-way partitioning scheme (i.e. elements equal to the pivot are partitioned into their own segment).</li>

</ul>

<ol>

 <li>i) If an input array of size <em>n </em>contains all identical keys, what is the asymptotic bound for QuickSort?</li>

</ol>

For example, you are sorting the array [3<em>,</em>3<em>,</em>3<em>,</em>3<em>,</em>3<em>,</em>3] ii) If an input array of size <em>n </em>contains <em>k &lt; n </em>distinct keys, what is the asymptotic bound for QuickSort?

For example, with <em>n </em>= 6<em>,k </em>= 3, sort the array [<em>a,b,a,c,b,c</em>]

<ul>

 <li>Consider an array of pairs (a,b). Your goal is to sort them by ascending a first, and then by ascending b. For example, (1,3), (1,4), (2,1)…. You are given 2 sorting functions. One that does a mergesort and one that does a quicksort.You can use each one at most once. How would you sort the pairs? Assume you can only sort one field at a time.</li>

</ul>

<h1>Problem 2.            Queues and Stacks Review</h1>

Recall the Stack and Queue Abstract Data Types (ADTs) that we have seen in CS1101S. Just a quick recap, a Stack is a “LIFO” (Last In First Out) collection of elements that supports the following operations:

<ul>

 <li><strong>push</strong>: Adds an element to the stack</li>

 <li><strong>pop</strong>: Removes the <strong>last </strong>element that was added to the stack</li>

 <li><strong>peek</strong>: Returns the last element added to the stack (without removing).</li>

</ul>

And a Queue is a “FIFO” (First In First Out) collection of elements that supports these operations:

<ul>

 <li><strong>enqueue</strong>: Adds an element to the queue</li>

 <li><strong>dequeue</strong>: Removes the <strong>first </strong>element that was added to the queue</li>

 <li><strong>peek</strong>: Returns the next item to be dequeued.</li>

 <li>How would you implement a stack and queue with a fixed-size array in Java? (Assume that the number of items in the collections never exceed the array’s capacity.)</li>

 <li>A Deque (double-ended queue) is an extension of a queue, which allows enqueueing and dequeueing from both ends of the queue. So the operations it would suppport are <em>enqueue </em><em>front</em>, <em>dequeue front</em>, <em>enqueue back</em>, <em>dequeue </em><em>back</em>. How can we implement a Deque with a fixed-size array in Java? (Again, assume that the number of items in the collections never exceed the array’s capacity.)</li>

 <li>What sorts of error handling would we need, and how can we best handle these situations?</li>

 <li>A set of parentheses is said to be balanced as long as every opening parenthesis “(” is closed by a closing parenthesis “)”. So for example, the strings “()()” and “(())” are balanced but the strings “)(())(” and “((” are not. Using a stack, determine whether a string of parentheses are balanced.</li>

 <li>(Optional) Sort a queue using another queue with <em>O</em>(1) additional space.</li>

</ul>

<strong>Problem 3.           Moar Pivots!</strong>

Quicksort is pretty fast. But that was with one pivot. Can we improve it by using two pivots? What about <em>k </em>pivots? What would the asymptotic running time be? (That is, the algorithm is to choose the pivots at random — or perhaps, imagine that you have a magic black box that gives you perfect pivots — then sort the pivots, partition the data among the pivots, and recurse on each part. You may assume whichever gives you a better performance)

<h1>Problem 4.           Child Jumble</h1>

Your aunt and uncle recently asked you to help out with your cousin’s birthday party. Alas, your cousin is three years old. That means spending several hours with twenty rambunctious three year olds as they race back and forth, covering the floors with paint and hitting each other with plastic beach balls. Finally, it is over. You are now left with twenty toddlers that each need to find their shoes. And you have a pile of shoes that all look about the same. The toddlers are not helpful. (Between exhaustion, too much sugar, and being hit on the head too many times, they are only semi-conscious.)

Luckily, their feet (and shoes) are all of slightly different sizes. Unfortunately, they are all very similar, and it is very hard to compare two pairs of shoes or two pairs of feet to decide which is bigger. (Have you ever tried asking a grumpy and tired toddler to line up their feet carefully with another toddler to determine who has bigger feet?) As such, you cannot compare shoes to shoes or feet to feet.

The only thing you can do is to have a toddler try on a pair of shoes. When you do this, you can figure out whether the shoes fit, or if they are too big, or too small. That is the only operation you can perform.

Come up with an efficient algorithm to match each child to their shoes. Give the time complexity of your algorithm in terms of the number of children.