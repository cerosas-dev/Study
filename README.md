<p align="center">
<img alt="AndroidInterviewQuestions" src="https://raw.githubusercontent.com/MindorksOpenSource/android-interview-questions/master/assets/android_interview_questions.png">
</p>


# Android Interview Questions
[![Mindorks](https://img.shields.io/badge/mindorks-opensource-blue.svg)](https://mindorks.com/open-source-projects)
[![Mindorks Community](https://img.shields.io/badge/join-community-blue.svg)](https://mindorks.com/join-community)
[![Mindorks Android Store](https://img.shields.io/badge/Mindorks%20Android%20Store-Android%20Interview%20Questions-blue.svg?style=flat)](https://mindorks.com/android/store)

> Android Interview Questions - Your Cheat Sheet For Android Interview

## We will be adding answers to the more questions on our [Mindorks website](https://mindorks.com).

## Prepared and maintained by [Amit Shekhar](https://github.com/amitshekhariitbhu) who is having experience of taking interviews of many Android developers and cracking interviews of top companies.

## Contents

* [Data Structures And Algorithms](#data-structures-and-algorithms)

* [Core Java](#core-java)

* [Core Android](#core-android)

* [Architecture](#architecture)

* [Design Problem](#design-problem)

* [Tools And Technologies](#tools-and-technologies)

* [Android Test Driven Development](#android-test-driven-development)

* [Others](#others)


### Data Structures And Algorithms

> The level of questions asked on the topic of Data Structures And Algorithms totally depends on the company for which you are applying.

* Array
    - An Array consists of a group of elements of the same data type. It is stored contiguously in memory and by using its' index, you can find the underlying data. Arrays can be one dimensional and multi-dimensional. One dimensional array is the simplest data structure, and also most commonly used. It is worth noting that in Java language multi-dimensional array are implemented as arrays of arrays. For example, `int[10][5]` is actually one array with its' cells pointing to ten 5-element arrays.    

        | Algorithm | Average | Worst Case |
        |:---------:|:-------:|:----------:|
        | Space     | Θ(n)    | O(n)       |    
        | Search    | Θ(n)    | O(n)       |
        | Insert    | Θ(n)    | O(n)       |
        | Delete    | Θ(n)    | O(n)       |

* LinkedList
    - A LinkedList, just like a tree and unlike an array, consists of a group of nodes which 
    together represent a sequence. Each node contains data and a pointer. The data in a node can be 
    anything, but the pointer is a reference to the next item in the LinkedList. A LinkedList 
    contains both a head and a tail. The "Head" is the first item in the LinkedList, while the "Tail" is 
    the last item. It is not a circular data structure, therefore the tail does not have its' 
    pointer pointing at the Head - the pointer is just `null`. The run time complexity for each of 
    the base methods are as follows:

        | Algorithm | Average | Worst Case |
        |:---------:|:-------:|:----------:|
        | Space     | Θ(n)    | O(n)       |
        | Search    | Θ(n)    | O(n)       |
        | Insert    | Θ(1)    | O(1)       |
        | Delete    | Θ(1)    | O(1)       |

* DoublyLinkedList
   - A DoublyLinkedList is based on a LinkedList, but there is two pointers in each node, "previous" pointer holds reference to the previous node and "next" pointer holds reference to the next node. It also has a Head node, head node's next pointer references the first node in this DoublyLinkedList. The last node's "next" reference points to `null`, but if last node's next pointer points to the first node, such DoublyLinkedList is called "Circular DoublyLinkedList". This data structure is very convenient if you need to be able to traverse stored elements in both directions. 
  
       ![DoublyLinkedList](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Doubly-linked-list.svg/610px-Doubly-linked-list.svg.png)
            
        | Algorithm | Average | Worst Case |
        |:---------:|:-------:|:----------:|
        | Space     | Θ(n)    | O(n)       |
        | Search    | Θ(n)    | O(n)       |
        | Insert    | Θ(1)    | O(1)       |
        | Delete    | Θ(1)    | O(1)       |

* Stack
   - A Stack is a basic data structure with a "Last-in-First-out" (LIFO) semantics. This means that 
    the last item that was added to the stack is the first item that comes out of the stack. A 
    Stack is like a stack of books in that in order to get to the first book that was added in the stack 
    (the bottom book), all of the books that were added after need to be removed first. Adding to a 
    Stack is called "Push", removing from a stack is called "Pop", and getting the last item 
    inserted into the stack without removing it is called "Top". The most common way to implement a
     stack is by using a LinkedList, but there is also StackArray (implemented with an array) 
     which does not replace null entries, and there is also a Vector implementation that does 
     replace `null` entries. [Wikipedia](https://en.wikibooks.org/wiki/Data_Structures/Stacks_and_Queues#Performance_Analysis)
        <table>
            <tr>
                <th>Algorithm</th>
                <th>Average</th>
                <th>Worst Case</th>
                <th>Image representation</th>
            </tr>
            <tr>
                <td>Space</td>
                <td>Θ(n)</td>
                <td>O(n)</td>
                <td rowspan="5">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Data_stack.svg/250px-Data_stack.svg.png"/>
                </td>
            </tr>
            <tr>
                <td>Search</td>
                <td>Θ(n)</td>
                <td>O(n)</td>
            </tr>
            <tr>
                <td>Insert (Push)</td>
                <td>Θ(1)</td>
                <td>O(1)</td>
            </tr>
            <tr>
                <td>Delete (Pop)</td>
                <td>Θ(1)</td>
                <td>O(1)</td>
            </tr>
            <tr>
              <td>Top</td>
              <td>Θ(1)</td>
              <td>O(1)</td>
            </tr>
        </table>

* Queue
	- Queue is an abstract data structure, somewhat similar to Stacks. Unlike stacks, a queue is open at both its ends. One end is always used to insert data (enqueue) and the other is used to remove data (dequeue). Queue follows First-In-First-Out methodology, i.e., the data item stored first will be accessed first.

* Priority Queue
	- A priority queue is different from a "normal" queue, because instead of being a "first-in-first-out" data structure, values come out in order by priority. 

* Binary Tree [Wikipedia](https://en.wikipedia.org/wiki/Binary_tree)
	- A binary tree is made of nodes, where each node contains a "left" reference, a "right" reference, and a data element. The topmost node in the tree is called the root. Every node (excluding a root) in a tree is connected by a directed edge from exactly one other node. This node is called a parent. On the other hand, each node can be connected to arbitrary number of nodes, called children. Nodes with no children are called leaves, or external nodes. Nodes which are not leaves are called internal nodes. Nodes with the same parent are called siblings.

* Binary Search Tree
	- A Binary Search Tree (BST) is a tree in which all the nodes follow the below-mentioned properties:
		- The left sub-tree of a node has a key less than or equal to its parent node's key.
		- The right sub-tree of a node has a key greater than to its parent node's key.
	- BST is a collection of nodes arranged in a way where they maintain BST properties. Each node has a key and an associated value. While searching, the desired key is compared to the keys in BST and if found, the associated value is retrieved.

	- Operations :

		- Search 

		```java
		public Node search(Node root, int key) {
		    // Base Cases: root is null or key is present at root
		    if (root==null || root.key==key)
		        return root;
		    // val is greater than root's key
		    if (root.key > key)
		        return search(root.left, key);
		    // val is less than root's key
		    return search(root.right, key);
		}
		```
	
		- Insert

		```java
		// This method mainly calls insertRec()
	    void insert(int key) {
	       root = insertRec(root, key);
	    }
	     
	    /* A recursive function to insert a new key in BST */
	    Node insertRec(Node root, int key) {
	        /* If the tree is empty, return a new node */
	        if (root == null) {
	            root = new Node(key);
	            return root;
	        }
	        /* Otherwise, recur down the tree */
	        if (key < root.key)
	            root.left = insertRec(root.left, key);
	        else if (key > root.key)
	            root.right = insertRec(root.right, key);
	 
	        /* return the (unchanged) node pointer */
	        return root;
	    }
		```
	
		- Delete

		```java
		// This method mainly calls deleteRec()
		void deleteKey(int key) {
			root = deleteRec(root, key);
		}
	 
	    /* A recursive function to insert a new key in BST */
	    Node deleteRec(Node root, int key) {
	        /* Base Case: If the tree is empty */
	        if (root == null)  return root;
	        /* Otherwise, recur down the tree */
	        if (key < root.key)
	            root.left = deleteRec(root.left, key);
	        else if (key > root.key)
	            root.right = deleteRec(root.right, key);
	            // if key is same as root's key, then This is 
	            // the node to be deleted
	        else {
	            // node with only one child or no child
	            if (root.left == null)
	                return root.right;
	            else if (root.right == null)
	                return root.left;
                // node with two children: Get the inorder
                // successor (smallest in the right subtree)
	            root.key = minValue(root.right);
	            // Delete the inorder successor
	            root.right = deleteRec(root.right, root.key);
	        }
	        return root;
	    }
	    ```

		- Pre Order traversal :
		
		```java
		void printPreorder(Node node) {
	        if (node == null)
	            return;
	        /* then print the data of node */
	        System.out.print(node.key + " ");
	        /* first recur on left child */
	        printPreorder(node.left);
	        /* now recur on right child */
	        printPreorder(node.right);
	    }
		```
	
		- In Order traversal :
		
		```java
		void printInorder(Node node) {
	        if (node == null)
	            return;
	        /* first recur on left child */
	        printInorder(node.left);
	        /* then print the data of node */
	        System.out.print(node.key + " ");
	        /* now recur on right child */
	        printInorder(node.right);
	    }
		```
		
		- Post Order traversal :
		
		```java
		void printPostorder(Node node) {
	        if (node == null)
	            return;
	        /* first recur on left child */
	        printPostorder(node.left);
	        /* now recur on right child */
	        printPostorder(node.right);
	        /* then print the data of node */
	        System.out.print(node.key + " ");
	    }
		```

* Hash Table or Hash Map
	- A Hash Table is a data structure that implements an associative array abstract data type, a structure that can map keys to values. A hash table uses a hash function to compute an index into an array of buckets or slots, from which the desired value can be found. Ideally, the hash function will assign each key to a unique bucket, but most hash table designs employ an imperfect hash function, which might cause hash collisions where the hash function generates the same index for more than one key. Such collisions must be accommodated in some way.
	- In a well-dimensioned hash table, the average cost (number of instructions) for each lookup is independent of the number of elements stored in the table. Many hash table designs also allow arbitrary insertions and deletions of key-value pairs, at (amortized) constant average cost per operation. In many situations, hash tables turn out to be on average more efficient than search trees or any other table lookup structure. For this reason, they are widely used in many kinds of computer software, particularly for associative arrays, database indexing, caches, and sets.

* Sorting Algorithms [Wikipedia](https://en.wikipedia.org/wiki/Sorting_algorithm?oldformat=true)
    - Using the most efficient sorting algorithm (and correct data structures that implement it) is vital for any program, because data manipulation can be one of the most significant bottlenecks in case of performance and the main purpose of spending time, determining the best algorithm for the job, is to drastically improve said performance. The efficiency of an algorithm is measured in its' "Big O" ([StackOverflow](https://stackoverflow.com/questions/487258/what-is-a-plain-english-explanation-of-big-o-notation)) score. Really good algorithms perform important actions in O(n log n) or even O(log n) time and some of them can even perform certain actions in O(1) time (HashTable insertion, for example). But there is always a trade-off - if some algorithm is really good at adding a new element to a data structure, it is, most certainly, much worse at data access than some other algorithm. If you are proficient with math, you may notice that "Big O" notation has many similarities with "limits", and you would be right - it measures best, worst and average performances of an algorithm in question, by looking at its' function limit. It should be noted that, when we are speaking about O(1) - constant time - we are not saying that this algorithm performs an action in one operation, rather that it can perform this action with the same number of operations (roughly), regrardless of the amount of elements it has to take into account. Thankfully, a lot of "Big O" scores have been already calculated, so you don't have to guess, which algorithm or data structure will perform better in your project. ["Big O" cheat sheet](http://bigocheatsheet.com/)

	    <table class="table table-bordered table-striped"><tbody>
		    <tr>
		      <th>Algorithm</th>
		      <th colspan="3">Time Complexity</th>
		      <th>Space Complexity</th>
		    </tr>
		    <tr>
		      <th></th>
		      <th>Best</th>
		      <th>Average</th>
		      <th>Worst</th>
		      <th>Worst</th>
		    </tr>
		    <tr>
		      <td><a href="http://en.wikipedia.org/wiki/Quicksort">Quicksort</a></td>
		      <td><code class="orange">Ω(n log(n))</code></td>
		      <td><code class="orange">Θ(n log(n))</code></td>
		      <td><code class="red">O(n^2)</code></td>
		      <td><code class="yellow-green">O(log(n))</code></td>
		    </tr>
		    <tr>
		      <td><a href="http://en.wikipedia.org/wiki/Merge_sort">Mergesort</a></td>
		      <td><code class="orange">Ω(n log(n))</code></td>
		      <td><code class="orange">Θ(n log(n))</code></td>
		      <td><code class="orange">O(n log(n))</code></td>
		      <td><code class="yellow">O(n)</code></td>
		    </tr>
		    <tr>
		      <td><a href="http://en.wikipedia.org/wiki/Timsort">Timsort</a></td>
		      <td><code class="yellow">Ω(n)</code></td>
		      <td><code class="orange">Θ(n log(n))</code></td>
		      <td><code class="orange">O(n log(n))</code></td>
		      <td><code class="yellow">O(n)</code></td>
		    </tr>
		    <tr>
		      <td><a href="http://en.wikipedia.org/wiki/Heapsort">Heapsort</a></td>
		      <td><code class="orange">Ω(n log(n))</code></td>
		      <td><code class="orange">Θ(n log(n))</code></td>
		      <td><code class="orange">O(n log(n))</code></td>
		      <td><code class="green">O(1)</code></td>
		    </tr>
		    <tr>
		      <td><a href="http://en.wikipedia.org/wiki/Bubble_sort">Bubble Sort</a></td>
		      <td><code class="yellow">Ω(n)</code></td>
		      <td><code class="red">Θ(n^2)</code></td>
		      <td><code class="red">O(n^2)</code></td>
		      <td><code class="green">O(1)</code></td>
		    </tr>
		    <tr>
		      <td><a href="http://en.wikipedia.org/wiki/Insertion_sort">Insertion Sort</a></td>
		      <td><code class="yellow">Ω(n)</code></td>
		      <td><code class="red">Θ(n^2)</code></td>
		      <td><code class="red">O(n^2)</code></td>
		      <td><code class="green">O(1)</code></td>
		    </tr>
		    <tr>
		      <td><a href="http://en.wikipedia.org/wiki/Selection_sort">Selection Sort</a></td>
		      <td><code class="red">Ω(n^2)</code></td>
		      <td><code class="red">Θ(n^2)</code></td>
		      <td><code class="red">O(n^2)</code></td>
		      <td><code class="green">O(1)</code></td>
		    </tr>
		    <tr>
		      <td><a href="https://en.wikipedia.org/wiki/Tree_sort">Tree Sort</a></td>
		      <td><code class="orange">Ω(n log(n))</code></td>
		      <td><code class="orange">Θ(n log(n))</code></td>
		      <td><code class="red">O(n^2)</code></td>
		      <td><code class="yellow">O(n)</code></td>
		    </tr>
		    <tr>
		      <td><a href="http://en.wikipedia.org/wiki/Shellsort">Shell Sort</a></td>
		      <td><code class="orange">Ω(n log(n))</code></td>
		      <td><code class="red">Θ(n(log(n))^2)</code></td>
		      <td><code class="red">O(n(log(n))^2)</code></td>
		      <td><code class="green">O(1)</code></td>
		    </tr>
		    <tr>
		      <td><a rel="tooltip" title="Only for integers. k is a number of buckets" href="http://en.wikipedia.org/wiki/Bucket_sort">Bucket Sort</a></td>
		      <td><code class="green">Ω(n+k)</code></td>
		      <td><code class="green">Θ(n+k)</code></td>
		      <td><code class="red">O(n^2)</code></td>
		      <td><code class="yellow">O(n)</code></td>
		    </tr>
		    <tr>
		      <td><a rel="tooltip" title="Constant number of digits 'k'" href="http://en.wikipedia.org/wiki/Radix_sort">Radix Sort</a></td>
		      <td><code class="green">Ω(nk)</code></td>
		      <td><code class="green">Θ(nk)</code></td>
		      <td><code class="green">O(nk)</code></td>
		      <td><code class="yellow">O(n+k)</code></td>
		    </tr>
		    <tr>
		      <td><a rel="tooltip" title="Difference between maximum and minimum number 'k'" href="https://en.wikipedia.org/wiki/Counting_sort">Counting Sort</a></td>
		      <td><code class="green">Ω(n+k)</code></td>
		      <td><code class="green">Θ(n+k)</code></td>
		      <td><code class="green">O(n+k)</code></td>
		      <td><code class="yellow">O(k)</code></td>
		    </tr>
		    <tr>
		      <td><a href="https://en.wikipedia.org/wiki/Cubesort">Cubesort</a></td>
		      <td><code class="yellow">Ω(n)</code></td>
		      <td><code class="orange">Θ(n log(n))</code></td>
		      <td><code class="orange">O(n log(n))</code></td>
		      <td><code class="yellow">O(n)</code></td>
		   </tr>
		</tbody></table>

    - Bubble sort [Wikipedia](https://en.wikipedia.org/wiki/Bubble_sort?oldformat=true) 
        - Bubble sort is one of the simplest sorting algorithms. It just compares neighbouring elements and if the one that precedes the other is smaller - it changes their places. So over one iteration over the data list, it is guaranteed that **at least** one element will be in its' correct place (the biggest/smallest one - depending on the direction of sorting). This is not a very efficient algorithm, as highly unordered arrays will require a lot of reordering (upto O(n^2)), but one of the advantages of this algorithm is its' space complexity - only two elements are compared at once and there is no need to allocate more memory, than those two will occupy. 
            <table>
                <tr>
                    <th colspan="3" align="center">Time Complexity</th>
                    <th align="center">Space Complexity</th>
                </tr>
                <tr>
                    <th align="center">Best</th>
                    <th align="center">Average</th>
                    <th align="center">Worst</th>
                    <th align="center">Worst</th>
                </tr>
                <tr>
                    <td align="center">Ω(n)</td>
                    <td align="center">Θ(n^2)</td>
                    <td align="center">O(n^2)</td>
                    <td align="center">O(1)</td>
                </tr>
            </table>
            
	```java
	static void bubbleSort(int[] arr) {
        int n = arr.length;
        int temp = 0;
        for (int i = 0; i < n; i++) {
            for (int j = 1; j < (n - i); j++) {
                if (arr[j - 1] > arr[j]) {
                    // swap elements
                    temp = arr[j - 1];
                    arr[j - 1] = arr[j];
                    arr[j] = temp;
                }
            }
        }
    }
	```
	
    - Selection sort [Wikipedia](https://www.wikiwand.com/en/Selection_sort) 
        - Firstly, selection sort assumes that the first element of the array to be sorted is the smallest, but to confirm this, it iterates over all other elements to check, and if it finds one, it gets defined as the smallest one. When the data ends, the element, that is currently found to be the smallest, is put in the beginning of the array. This sorting algorithm is quite straightforward, but still not that efficient on larger data sets, because to assign just one element to its' place, it needs to go over all data.
            <table>
            <tr>
                <th colspan="3" align="center">Time Complexity</th>
                <th align="center">Space Complexity</th>
            </tr>
            <tr>
                <th align="center">Best</th>
                <th align="center">Average</th>
                <th align="center">Worst</th>
                <th align="center">Worst</th>
            </tr>
            <tr>
                <td align="center">Ω(n^2)</td>
                <td align="center">Θ(n^2)</td>
                <td align="center">O(n^2)</td>
                <td align="center">O(1)</td>
            </tr>
            </table>
            
	```java
	public static void selectionSort(int[] arr) {
        for (int i = 0; i < arr.length - 1; i++) {
            int index = i;
            for (int j = i + 1; j < arr.length; j++) {
                if (arr[j] < arr[index]) {
                    index = j;//searching for lowest index
                }
            }
            int smallerNumber = arr[index];
            arr[index] = arr[i];
            arr[i] = smallerNumber;
        }
    }
	```
	
    - Insertion sort [Wikipedia](https://en.wikipedia.org/wiki/Insertion_sort?oldformat=true)
        - Insertion sort is another example of an algorithm, that is not that difficult to implement, but is also not that efficient. To do its' job, it "grows" sorted portion of data, by "inserting" new encountered elements into already (innerly) sorted part of the array, which consists of previously encountered elements. This means that in best case (data is already sorted) it can confirm that its' job is done in Ω(n) operations, while, if all encountered elements are not in their required order as many as O(n^2) operations may be needed.
            <table>
            <tr>
                <th colspan="3" align="center">Time Complexity</th>
                <th align="center">Space Complexity</th>
            </tr>
            <tr>
                <th align="center">Best</th>
                <th align="center">Average</th>
                <th align="center">Worst</th>
                <th align="center">Worst</th>
            </tr>
            <tr>
                <td align="center">Ω(n)</td>
                <td align="center">Θ(n^2)</td>
                <td align="center">O(n^2)</td>
                <td align="center">O(1)</td>
            </tr>
            </table>
            
	```java
	public static void insertionSort(int array[]) {  
        int n = array.length;  
        for (int j = 1; j < n; j++) {  
            int key = array[j];  
            int i = j - 1;  
            while ((i > -1) && ( array [i] > key )) {  
                array [i+1] = array [i];  
                i--;  
            }  
            array[i+1] = key;  
        }  
    }
	```
    - Merge sort [Wikipedia](https://en.wikipedia.org/wiki/Merge_sort?oldformat=true)
        - This is a "divide and conquer" algorithm, meaning it recursively "divides" given array in to smaller parts (up to 1 element) and then sorts those parts, combining them with each other. This approach allows merge sort to achieve very high speed, while  doubling required space, of course, but today memory space is more available than it was a couple of years ago, so this trade-off is considered acceptable.   
                <table>
            <tr>
                <th colspan="3" align="center">Time Complexity</th>
                <th align="center">Space Complexity</th>
            </tr>
            <tr>
                <th align="center">Best</th>
                <th align="center">Average</th>
                <th align="center">Worst</th>
                <th align="center">Worst</th>
            </tr>
            <tr>
                <td align="center">Ω(n log(n))</td>
                <td align="center">Θ(n log(n))</td>
                <td align="center">O(n log(n))</td>
                <td align="center">O(n)</td>
            </tr>
            </table>
            
	```java
	public static void merge(int arr[], int beg, int mid, int end) {
        int l = mid - beg + 1;
        int r = end - mid;
        int leftArray[] = new int[l];
        int rightArray[] = new int[r];
        for (int i = 0; i < l; ++i)
            leftArray[i] = arr[beg + i];
        for (int j = 0; j < r; ++j)
            rightArray[j] = arr[mid + 1 + j];
        int i = 0, j = 0;
        int k = beg;
        while (i < l && j < r) {
            if (leftArray[i] <= rightArray[j]) {
                arr[k] = leftArray[i];
                i++;
            } else  {
                arr[k] = rightArray[j];
                j++;
            }
            k++;
        }
        while (i < l) {
            arr[k] = leftArray[i];
            i++;
            k++;
        }
        while (j < r) {
            arr[k] = rightArray[j];
            j++;
            k++;
        }
    }

    public static void sort(int arr[], int beg, int end) {
        if (beg < end) {
            int mid = (beg + end) / 2;
            sort(arr, beg, mid);
            sort(arr, mid + 1, end);
            merge(arr, beg, mid, end);
        }
    }
	```

    - Quicksort [Wikipedia](https://en.wikipedia.org/wiki/Quicksort?oldformat=true)
        - Quicksort is considered, well, quite quick. When implemented correctly, it can be a significant number of times faster than its' main competitors. This algorithm is also of "divide and conquer" family and its' first step is to choose a "pivot" element (choosing it randomly, statistically, minimizes the chance to get the worst performance), then by comparing elements to this pivot, moving it closer and closer to its' final place. During this process, the elements that are bigger are moved to the right side of it and smaller elements to the left. After this is done, quicksort repeats this process for subarrays on each side of placed pivot (does first step recursively), until the array is sorted.
                <table>
                <tr>
                    <th colspan="3" align="center">Time Complexity</th>
                    <th align="center">Space Complexity</th>
                </tr>
                <tr>
                    <th align="center">Best</th>
                    <th align="center">Average</th>
                    <th align="center">Worst</th>
                    <th align="center">Worst</th>
                </tr>
                <tr>
                    <td align="center">Ω(n log(n))</td>
                    <td align="center">Θ(n log(n))</td>
                    <td align="center">O(n^2)</td>
                    <td align="center">O(1)</td>
                </tr>
                </table>  
                
	```java
	public static int partition(int a[], int beg, int end) {
        int left, right, temp, loc, flag;
        loc = left = beg;
        right = end;
        flag = 0;
        while (flag != 1) {
            while ((a[loc] <= a[right]) && (loc != right))
                right--;
            if (loc == right)
                flag = 1;
            else if (a[loc] > a[right]) {
                temp = a[loc];
                a[loc] = a[right];
                a[right] = temp;
                loc = right;
            }
            if (flag != 1) {
                while ((a[loc] >= a[left]) && (loc != left))
                    left++;
                if (loc == left)
                    flag = 1;
                else if (a[loc] < a[left]) {
                    temp = a[loc];
                    a[loc] = a[left];
                    a[left] = temp;
                    loc = left;
                }
            }
        }
        return loc;
    }

    static void quickSort(int a[], int beg, int end) {
        int loc;
        if (beg < end) {
            loc = partition(a, beg, end);
            quickSort(a, beg, loc - 1);
            quickSort(a, loc + 1, end);
        }
    }
	```
                
    - There are, of course, more sorting algorithms and their modifications. We strongly recommend all readers to familiarize themselves with a couple more, because knowing algorithms is very important quality of a candidate, applying for a job and it shows understanding of what is happening "under the hood".

* Dynamic Programming

* Greedy Algorithm

* String Manipulation

	- Get all possible permutations of a String

	```java
	private static void permutation(String prefix, String str) {
		int n = str.length();
		if (n == 0) System.out.println(prefix);
		else {
			for (int i = 0; i < n; i++) {
				String _prefix = prefix + str.charAt(i);
				String _string = str.substring(0, i);
				_string += str.substring(i + 1, n);
				permutation(_prefix, _string);
			}
		}
	}
	```

	- The longest common subsequence (LCS) problem is the problem of finding the longest subsequence common to all sequences in a set of sequences (often just two sequences). It differs from the longest common substring problem: unlike substrings, subsequences are not required to occupy consecutive positions within the original sequences.

	```java
	static int lcs(String s1, String s2) {
		int size_1 = s1.length();
		int size_2 = s2.length();
		int[][] cmn = new int[size_1][size_2];
		for (int y = 0; y < size_1; y++) {
			for (int x = 0; x < size_2; x++) {
				if (s1.charAt(y) == s2.charAt(x)) {
					int temp = 1;
					if (x > 0 && y > 0)
						temp = cmn[y - 1][x - 1] + 1;
					cmn[y][x] = temp;
				} else {
					int temp_1 = x == 0 ? 0 : cmn[y][x - 1];
					int temp_2 = y == 0 ? 0 : cmn[y - 1][x];
					cmn[y][x] = Math.max(temp_1, temp_2);
				}
			}
		}
		return cmn[size_1 - 1][size_2 - 1];
	}
	```

* Pathfinding algorithms [Wikipedia](https://en.wikipedia.org/wiki/Greedy_algorithm?oldformat=true)
    - Dijkstra algorithm
    - A* algorithm
    - Breadth First Search
		- BFS is a traversing algorithm where you should start traversing from a selected node (source or starting node) and traverse the graph layerwise thus exploring the neighbour nodes (nodes which are directly connected to source node). You must then move towards the next-level neighbour nodes. As the name BFS suggests, you are required to traverse the graph breadthwise as follows:
			- First move horizontally and visit all the nodes of the current layer
			- Move to the next layer
			
			```java
			void BFS(Node root) {
				// BFS uses Queue data structure
				Queue queue = new LinkedList();
				queue.add(root);
				printNode(root);
				rootNode.visited = true;
				while(!queue.isEmpty()) {
					Node node = (Node)queue.remove();
					Node child = null;
					while((child = getUnvisitedChildNode(node)) != null) {
						child.visited = true;
						printNode(child);
						queue.add(child);
					}
				}
				// Clear visited property of nodes
				clearNodes();
		    }
		    ```
    - Depth First Search
	    - DFS is another uninformed graph traversal algorithm which produces a non-optimal solution but can be useful for traversing quickly into deeper search domains. Depth first search is very similar to the BFS. With Depth first search you start at the top most node in a tree and then follow the left most branch until there exists no more leafs in that branch. At that point you will search the nearest ancestor with unexplored nodes until such time as you find the goal node.

			```java
			void DFS(Node root) {
				// DFS uses Dequeue data structure
				Deque deque = new ArrayDeque();
				deque.add(root);
				printNode(root);
				rootNode.visited = true;
				while(!deque.isEmpty()) {
					Node node = (Node)deque.remove();
					Node child = null;
					while((child = getUnvisitedChildNode(node)) != null) {
						child.visited = true;
						printNode(child);
						deque.add(child);
					}
				}
				// Clear visited property of nodes
				clearNodes();
		    }
		    ```

### Core Java

#### OOP

* Explain OOP Concepts.
    - Object-Oriented Programming is a methodology of designing a program using classes, objects, 
    [inheritance](https://en.wikipedia.org/wiki/Inheritance_(object-oriented_programming)),
    [polymorphism](https://en.wikipedia.org/wiki/Polymorphism_(computer_science)),
    [abstraction](https://en.wikipedia.org/wiki/Abstraction_(software_engineering)), and
    [encapsulation](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)).

* Differences between abstract classes and interfaces? [GitHub](https://arjun-sna.github.io/java/2017/02/02/abstractvsinterface/)
    - An abstract class, is a class that contains both concrete and abstract methods 
    (methods without implementations). An abstract method must be implemented by the abstract class
     sub-classes. Abstract classes cannot be instantiated and need to be extended to be used.
    - An interface is like a blueprint/contract of a class (or it may be thought of as a class with methods, but without their implementation). It contains empty methods that 
    represent, what all of its subclasses should have in common. The subclasses provide the 
    implementation for each of these methods. Interfaces are implemented.

* What is the difference between iterator and enumeration in java?

* Do you agree we use composition over inheritance? [Composition vs Inheritance](https://www.journaldev.com/12086/composition-vs-inheritance)

* Difference between method overloading and overriding.
        <p align="center">
        <img alt="Overloading and Overriding" src="https://github.com/codeshef/android-interview-questions/blob/master/assets/overloading-vs-overriding.png?raw=true">
        </p>
    - Overloading happens at compile-time while Overriding happens at runtime: The binding of overloaded method call to its definition has happens at compile-time however binding of overridden method call to its definition happens at runtime.
    More info on static vs. dynamic binding: [StackOverflow](https://stackoverflow.com/questions/19017258/static-vs-dynamic-binding-in-java).
    - Static methods can be overloaded which means a class can have more than one static method of same name. Static methods cannot be overridden, even if you declare a same static method in child class it has nothing to do with the same method of parent class as overridden static methods are chosen by the reference class and not by the class of the object.

    So, for example:
    
    ```java
        public class Animal {
            public static void testClassMethod() {
                System.out.println("The static method in Animal");
            }

            public void testInstanceMethod() {
                System.out.println("The instance method in Animal");
            }
        }

        public class Cat extends Animal {
            public static void testClassMethod() {
                System.out.println("The static method in Cat");
            }

            public void testInstanceMethod() {
                System.out.println("The instance method in Cat");
            }

            public static void main(String[] args) {
                Cat myCat = new Cat();
                myCat.testClassMethod();
                Animal myAnimal = myCat;
                myAnimal.testClassMethod();
                myAnimal.testInstanceMethod();
            }
        }
	```
        
    Will output:
        
	```java
        The static method in Cat    // testClassMethod() is called from "Cat" reference

        The static method in Animal // testClassMethod() is called from "Animal" reference,
                                    // ignoring actual object inside it (Cat)

        The instance method in Cat  // testInstanceMethod() is called from "Animal" reference,
                                    // but from "Cat" object underneath
   ```

    The most basic difference is that overloading is being done in the same class while for overriding base and child classes are required. Overriding is all about giving a specific implementation to the inherited method of parent class.

    Static binding is being used for overloaded methods and dynamic binding is being used for overridden/overriding methods.
        Performance: Overloading gives better performance compared to overriding. The reason is that the binding of overridden methods is being done at runtime.

    Private and final methods can be overloaded but they cannot be overridden. It means a class can have more than one private/final methods of same name but a child class cannot override the private/final methods of their base class.

    Return type of method does not matter in case of method overloading, it can be same or different. However in case of method overriding the overriding method can have more specific return type (meaning if, for example, base method returns an instance of Number class, all overriding methods can return any class that is extended from Number, but not a class that is higher in the hierarchy, like, for example, Object is in this particular case).

    Argument list should be different while doing method overloading. Argument list should be same in method Overriding. It is also a good practice to annotate overridden methods with `@Override` to make the compiler be able to notify you if child is, indeed, overriding parent's class method during compile-time.

* What are the access modifiers you know? What does each one do? <br>
   - There are four access modifiers in Java language (from strictest to the most lenient):
        1. `private` *variables*, *methods*, *constructors* or *inner classes* are only visible to its' containing class and its' methods. This modifier is most commonly used, for example, to allow variable access only through getters and setters or to hide underlying implementation of classes that should not be used by user and therefore maintain encapsulation. Singleton constructor is also marked `private` to avoid unwanted instantiation from outside.
        2. `protected` can be used on *variables*, *methods* and *constructors* therefore allowing access only to subclasses and classes that are inside the same package as protected members' class.
        3. Default (no keyword is used) this modifier can be applied to *classes*, *variables*, *constructors* and *methods* and allows access from classes and methods inside the same package.
        4. `public` modifier is widely-used on *classes*, *variables*, *constructors* and *methods* to grant access from any class and method anywhere. It should not be used everywhere as it implies that data marked with `public` is not sensitive and can not be used to harm the program.

* Can an Interface implement another Interface?
  - Yes, an interface can implement another interface (and more than one), but it needs to use `extends`, rather than `implements` keyword. And while you can not remove methods from parent interface, you can add new ones freely to your subinterface.

* What is Polymorphism? What about Inheritance?
  - Polymorphism in Java has two types: Compile time polymorphism (static binding) and Runtime polymorphism (dynamic binding). Method overloading is an example of static polymorphism, while method overriding is an example of dynamic polymorphism.

	An important example of polymorphism is how a parent class refers to a child class object.  In fact, any object that satisfies more than one IS-A relationship is polymorphic in nature.

	For instance, let’s consider a class `Animal` and let `Cat` be a subclass of `Animal`. So, any cat IS animal. Here, Cat satisfies the IS-A relationship for its own type as well as its super class Animal.
  - Inheritance can be defined as the process where one class acquires the properties (methods and fields) of another. With the use of inheritance the information is made manageable in a hierarchical order.

	The class which inherits the properties of other is known as subclass (derived class, child class) and the class whose properties are inherited is known as superclass (base class, parent class).

	Inheritance uses the keyword `extends` to inherit the properties of a class. Following is the syntax of extends keyword.
	```java
	class Super {
	   .....
	   .....
	}
	class Sub extends Super {
	   .....
	   .....
	}
	```

* Multiple inheritance in Classes and Interfaces in java [Blog](http://codeinventions.blogspot.in/2014/07/can-interface-extend-multiple.html)

* What are the design patterns? [GitHub](https://github.com/iluwatar/java-design-patterns)
    - Creational patterns
        - Builder [Wikipedia](https://en.wikipedia.org/wiki/Builder_pattern?oldformat=true).
        	The intent of the Builder design pattern is to separate the construction of a complex object from its representation. By doing so the same construction process can create different representations. Encapsulate creating and assembling the parts of a complex object in a separate Builder object. A class delegates object creation to a Builder object instead of creating the objects directly.

        - Factory [Wikipedia](https://en.wikipedia.org/wiki/Factory_method_pattern). Creating an object often requires complex processes not appropriate to include within a composing object. The object's creation may lead to a significant duplication of code, may require information not accessible to the composing object, may not provide a sufficient level of abstraction, or may otherwise not be part of the composing object's concerns. The factory method design pattern handles these problems by defining a separate method for creating the objects, which subclasses can then override to specify the derived type of product that will be created. The factory method pattern relies on inheritance, as object creation is delegated to subclasses that implement the factory method to create objects.

        - Singleton [Wikipedia](https://en.wikipedia.org/wiki/Singleton_pattern).
          A singleton is a class that can only be instantiated once. This singleton pattern restricts the instantiation of a class to one object. This is useful when exactly one object is needed to coordinate actions across the system. The concept is sometimes generalized to systems that operate more efficiently when only one object exists, or that restrict the instantiation to a certain number of objects.

    - Structural patterns
        - Adapter [Wikipedia](https://en.wikipedia.org/wiki/Adapter_pattern). The adapter pattern is a software design pattern (also known as wrapper, an alternative naming shared with the decorator pattern) that allows the interface of an existing class to be used as another interface. It is often used to make existing classes work with others without modifying their source code. An example is an adapter that converts the interface of a Document Object Model of an XML document into a tree structure that can be displayed.
        - Decorator [Wikipedia](https://en.wikipedia.org/wiki/Decorator_pattern). The decorator pattern is a design pattern that allows behavior to be added to an individual object, dynamically, without affecting the behavior of other objects from the same class. The decorator pattern is often useful for adhering to the Single Responsibility Principle, as it allows functionality to be divided between classes with unique areas of concern. The decorator pattern is structurally nearly identical to the chain of responsibility pattern, the difference being that in a chain of responsibility, exactly one of the classes handles the request, while for the decorator, all classes handle the request.
        - Facade [Wikipedia](https://en.wikipedia.org/wiki/Facade_pattern). Facade design pattern is commonly used when a system is very complex or difficult to understand because the system has a large number of interdependent classes or because its source code is unavailable. This pattern hides the complexities of the larger system and provides a simpler interface to the client. It typically involves a single wrapper class that contains a set of members required by the client. These members access the system on behalf of the facade client and hide the implementation details.
    - Behavioural patterns
        - Chain of responsibility [Wikipedia](https://en.wikipedia.org/wiki/Chain-of-responsibility_pattern). Is a design pattern consisting of a source of command objects and a series of processing objects. Each processing object contains logic that defines the types of command objects that it can handle; the rest are passed to the next processing object in the chain. A mechanism also exists for adding new processing objects to the end of this chain. Thus, the chain of responsibility is an object oriented version of the if ... else if ... else if ....... else ... endif idiom, with the benefit that the condition–action blocks can be dynamically rearranged and reconfigured at runtime. The chain-of-responsibility pattern is structurally nearly identical to the decorator pattern, the difference being that for the decorator, all classes handle the request, while for the chain of responsibility, exactly one of the classes in the chain handles the request.
        - Iterator [Wikipedia](https://en.wikipedia.org/wiki/Iterator_pattern). The essence of the Iterator Pattern is to "Provide a way to access the elements of an aggregate object sequentially without exposing its underlying representation."
        - Strategy [Wikipedia](https://en.wikipedia.org/wiki/Strategy_pattern). The strategy pattern (also known as the policy pattern) is a behavioral software design pattern that enables selecting an algorithm at runtime. Instead of implementing a single algorithm directly, code receives run-time instructions as to which in a family of algorithms to use. Strategy lets the algorithm vary independently from clients that use it. Strategy is one of the patterns included in the influential book Design Patterns by Gamma et al. that popularized the concept of using design patterns to describe how to design flexible and reusable object-oriented software. Deferring the decision about which algorithm to use until runtime allows the calling code to be more flexible and reusable. 
        - Observer [Wikipedia](https://en.wikipedia.org/wiki/Observer_pattern). The observer pattern is a software design pattern in which an object, called the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods. It is mainly used to implement distributed event handling systems, in "event driven" software. Most modern languages such as C# have built in "event" constructs which implement the observer pattern components, for easy programming and short code.

#### Collections and Generics

* `Arrays` vs `ArrayLists`.

* `HashSet` vs `TreeSet`.

* Explain Generics in Java?
    - Generics were included in Java language to provide stronger type checks, by allowing the programmer to define, which classes can be used with other classes
        > In a nutshell, generics enable types (classes and interfaces) to be parameters when defining classes, interfaces and methods. Much like the more familiar formal parameters used in method declarations, type parameters provide a way for you to re-use the same code with different inputs. The difference is that the inputs to formal parameters are values, while the inputs to type parameters are types. ([Official Java Documentation](https://docs.oracle.com/javase/tutorial/java/generics/why.html))

    - This means that, for example, you can define:
        ```java
        List<Integer> list = new ArrayList<>();
        ```
        And let the compiler take care of noticing, if you put some object, of type other than `Integer` into this list and warn you.
    - It should be noted that standard class hierarchy *does not* apply to generic types. It means that `Integer` in `List<Integer>` is not inherited from `<Number>` - it is actually inherited directly from `<Object>`. You can still put some constraints on what classes can be passed as a parameter into a generic by using [wildcards](https://docs.oracle.com/javase/tutorial/extra/generics/wildcards.html) like `<?>`, `<? extends MyCustomClass>` or `<? super Number>`.
    - While generics are very useful, late inclusion into Java language has put some restraints on their implementation - backward compatibility required them to remain just "syntactic sugar" - they are erased ([type erasure](https://docs.oracle.com/javase/tutorial/java/generics/erasure.html)) during compile-time and replaced with `object` class.

* What is Java `PriorityQueue`?
	- An unbounded priority queue based on a priority heap. The elements of the priority queue are ordered according to their natural ordering, or by a Comparator provided at queue construction time, depending on which constructor is used. A priority queue does not permit null elements. A priority queue relying on natural ordering also does not permit insertion of non-comparable objects (doing so may result in ClassCastException). The head of this queue is the least element with respect to the specified ordering. If multiple elements are tied for least value, the head is one of those elements -- ties are broken arbitrarily. The queue retrieval operations poll, remove, peek, and element access the element at the head of the queue. A priority queue is unbounded, but has an internal capacity governing the size of an array used to store the elements on the queue. It is always at least as large as the queue size. As elements are added to a priority queue, its capacity grows automatically. The details of the growth policy are not specified.

#### Objects and Primitives

#### String

* How is `String` class implemented? Why was it made immutable?
  - There is no primitive variant of `String` class in Java language - all strings are just wrappers around underlying array of characters, which is declared `final`. This means that, once a `String` object is instantiated, it cannot be changed through normal tools of the language (Reflection still can mess things up horribly, because in Java no object is truly immutable). This is why `String` variables in classes are the first candidates to be used, when you want to override `hashCode()` and `equals()` of your class - you can be sure, that all their required contracts will be satisfied.
    > Note: The String class is immutable, so that once it is created a String object cannot be changed. The String class  has a number of methods, some of which will be discussed below, that appear to modify strings. Since strings are  immutable, what these methods really do is create and return a new string that contains the result of the operation. ([Official Java Documentation](https://docs.oracle.com/javase/tutorial/java/data/strings.html))

    This class is also unique in a sense, that, when you create an instance like this:
    ```java
    String helloWorld = "Hello, World!";
    ```
    `"Hello, World!"` is called a *literal* and compiler creates a `String` object with its' value. So
    ```java
    String capital = "Hello, World!".toUpperCase();
    ```
    is a valid statement, that, firstly, will create an object with literal value "Hello, World!" and then will create and return another object with value "HELLO, WORLD!"
  - `String` was made immutable to prevent malicious manipulation of data, when, for example, user login or other sensitive data is being send to a server.

* What does it means to say that a `String` is immutable?
    - It means that once created, `String` object's `char[]` (its' containing value) is declared `final` and, therefore, it can not be changed during runtime.

* What is `String.intern()`? When and why should it be used?
	- String Interning is a method of storing only one copy of each distinct String Value, which must be immutable. By applying String.intern() on a couple of strings will ensure that all strings having same contents share same memory. For example, if a name ‘Amy’ appears 100 times, by interning you ensure only one ‘Amy’ is actually allocated memory. This can be very useful to reduce memory requirements of your program. But be aware that the cache is maintained by JVM in permanent memory pool which is usually limited in size compared to heap so you should not use intern if you don’t have too many duplicate values intern() method : In Java, when we perform any operation using intern() method, it returns a canonical representation for the string object. A pool is managed by String class.
		- When the intern() method is executed then it checks whether the String equals to this String Object is in the pool or not.
		- If it is available, then the string from the pool is returned. Otherwise, this String object is added to the pool and a reference to this String object is returned.
		- It follows that for any two strings s and t, s.intern() == t.intern() is true if and only if s.equals(t) is true.
		- In the java programming language, intern() is a method present in String class which is present in java.lang package. By the help of intern() method, we can get the reference of corresponding String constant pool object of an original object.

* Can you list 8 primitive types in java?

* What is the difference between an Integer and int?
  - `int` is a primitive data type (with `boolean`, `byte`, `char`, `short`, `long`, `float` and `double`), while `Integer` (with `Boolean`, `Byte`, `Character`, `Short`,`Long`, `Float` and `Double`) is a [wrapper](https://docs.oracle.com/javase/tutorial/java/data/numberclasses.html) class that encapsulates primitive data type, while providing useful methods to perform different tasks with it.

* What is Autoboxing and Unboxing?
  - Autoboxing and Unboxing is the process of automatic wrapping (putting in a box) and unwrapping (getting the value out) of primitive data types, that have "wrapper" classes. So `int` and `Integer` can (almost always) be used interchangeably in Java language, meaning a method `void giveMeInt(int i) { ... }` can take `int` as well as `Integer` as a parameter.

* Typecast in Java.
    - In Java, you can use casts to polymorph one class into another, compatible one. For example:
        ```java
            long i = 10l;
            int j = (int) i;
            long k = j;
        ```
        Here we see, that, while narrowing (`long i` -> `int j`) requires an explicit cast to make sure the programmer realizes, that there may be some data or precision loss, widening (`int j` -> `long k`) does not require an explicit cast, because there can be no data loss (`long` can take larger numbers than `int` allows).

* Do objects get passed by reference or value in Java? Elaborate on that.
    - In Java all primitives and objects are passed by value, meaning that their copy will be manipulated in the receiving method. But there is a caveat - when you pass an object reference into a method, a *copy of this reference* is made, so it still points to the same object. This means, that any changes that you make to the insides of this object are retained, when the method exits.

        ```java
        public class Pointer {
            int innerField;
            public Pointer(int a) {
                this.innerField = a;
            }
        }
        ```
        
        ```java
        public class ValueAndReference {

            public static void main(String[] args) {

                Pointer a = new Pointer(0);
                int b = 1;

                print("Before:");
                print("b = " + b);
                print("a.innerField = " + a.innerField);
                exampleMethod(a, b);
                print("After:");
                print("b = " + b);
                print("a.innerField = " + a.innerField);
            }

            static void exampleMethod(Pointer a, int b) {
                a.innerField = 2;
                b = 10;
            }

            static void print(String text) {
                System.out.println(text);
            }
        }
        ```
       Will output:
       
        ```java
            Before:

            b = 1

            a.innerField = 0

            After:

            b = 1        // a new local int variable was created and operated on, so "b" didn't change

            a.innerField = 2 // Pointer a got its' innerField variable changed
                             //  from 0 to 2, because method was operating on
                             //  the same reference to an instance
        ```

* What is the difference between instantiation and initialization of an object?
    - Initialization is the process of the memory allocation, when a new variable is created. Variables should be explicitly given a value, otherwise they may contain a random value that remained from the previous variable that was using the same memory space. To avoid this problem, Java language assigns default (right after initialization) values to some data types:
        * `boolean` defaults to `false`;
        * `byte` defaults to `0`;
        * `short` defaults to `0`;
        * `int` defaults to `0`;
        * `long` defaults to `0L`;
        * `char` defaults to `\u0000`;
        * `float` defaults to `0.0f`;
        * `double` defaults to `0.0d`;
        * `object` defaults to `null`.
    - Instantiation is the process of explicitly assigning definitive value to a declared variable:
        ```java
            int j;  // Initialized variable (int defaults to 0 right after)
            j = 10; // Instantiated variable
        ```

* What the difference between local, instance and class variables?
  - Local variables exist only in methods that created them, they are stored separately in their respected Thread Stack (for more information, see question about Java Memory Model) and cannot have their reference passed outside of the method scope. That also means that they cannot be assigned any access modifier or made `static` - because they only exist during enclosing method's execution and those modifiers just do not make sense, since no other outside method can get them anyway.
  - Instance variables are the ones, that are declared in classes and their value can be different from one instance of the class to another, but they always require that class' instance to exist.
  - Class variables are those, that are marked with `static` keyword in their class' body. They can only have one value across all instances of that class (changing it in one place will change it in their class and, therefore, in all instances) and can even be retrieved without that class' instance (if their access modifier allows it).

#### Java Memory Model and Garbage Collector

* What is garbage collector? How does it work?
  - All objects are allocated on the heap area managed by the JVM.
  As long as an object is being referenced, the JVM considers it alive.
  Once an object is no longer referenced and therefore is not reachable by the application code,
  the garbage collector removes it and reclaims the unused memory.

* What is Java Memory Model? What contracts does it guarantee? How are its' Heap and Stack organized? [Jenkov](http://tutorials.jenkov.com/java-concurrency/java-memory-model.html)

* What is memory leak and how does Java handle it?

* What are strong, soft, weak and phantom references in Java? 
	- Java provides two different types/classes of Reference Objects: strong and weak. Weak Reference Objects can be further divided into soft and phantom. Let's go point by point.
		> Strong Reference Object

		```java
		StringBuilder builder = new StringBuilder();
		```
		
		- This is the default type/class of Reference Object, if not differently specified: builder is a strong Reference Object. This kind of reference makes the referenced object not eligible for GC. That is, whenever an object is referenced by a chain of strong Reference Objects, it cannot be garbage collected.

		> Weak Reference Object

		```java
		WeakReference<StringBuilder> weakBuilder = new WeakReference<StringBuilder>(builder);
		```
		
		- Weak Reference Objects are not the default type/class of Reference Object and to be used they should be explicitly specified like in the above example. This kind of reference makes the reference object eligible for GC. That is, in case the only reference reachable for the StringBuilder object in memory is, actually, the weak reference, then the GC is allowed to garbage collect the StringBuilder object. When an object in memory is reachable only by Weak Reference Objects, it becomes automatically eligible for GC.

		> Levels of Weakness

		- Two different levels of weakness can be enlisted: soft and phantom. A soft Reference Object is basically a weak Reference Object that remains in memory a bit more: normally, it resists GC cycle until memory is available and there is no risk of OutOfMemoryError (in that case, it can be removed).
		- On the other hand, a phantom Reference Object is useful only to know exactly when an object has been effectively removed from memory: normally they are used to fix weird finalize() revival/resurrection behavior, since they actually do not return the object itself but only help in keeping track of their memory presence.
		- Weak Reference Objects are ideal to implement cache modules. In fact, a sort of automatic eviction can be implemented by allowing the GC to clean up memory areas whenever objects/values are no longer reachable by strong references chain. An example is the WeakHashMap retaining weak keys.

#### Concurrency

* What does the keyword `synchronized` mean? [Link](https://stackoverflow.com/a/1085745/2621950)
	- `synchronized` methods enable a simple strategy for preventing thread interference and memory consistency errors: if an object is visible to more than one thread, all reads or writes to that object's variables are done through synchronized methods.

* What is a `ThreadPoolExecutor`? [Mindorks](https://blog.mindorks.com/threadpoolexecutor-in-android-8e9d22330ee3)
	- The `ThreadPoolExecutor` is an implementation of the `ExecutorService` interface. The ThreadPoolExecutor executes the given task (Callable or Runnable) using one of its internally pooled threads. The thread pool contained inside the ThreadPoolExecutor can contain a varying amount of threads. The number of threads in the pool is determined by these variables: `corePoolSize` and  `maximumPoolSize`. If less than corePoolSize threads are created in the the thread pool when a task is delegated to the thread pool, then a new thread is created, even if idle threads exist in the pool. If the internal queue of tasks is full, and corePoolSize threads or more are running, but less than maximumPoolSize threads are running, then a new thread is created to execute the task.

* What is `volatile` modifier? [Jenkov](http://tutorials.jenkov.com/java-concurrency/volatile.html)
	- Declaring a volatile Java variable means: The value of this variable will never be cached thread-locally: all reads and writes will go straight to "main memory"; Access to the variable acts as though it is enclosed in a synchronized block, synchronized on itself.

#### Exceptions

* How does the `try{} catch{} finally{}` works? [Link](http://tutorials.jenkov.com/java-exception-handling/basic-try-catch-finally.html)

#### Others

* What is serialization? How do you implement it?
    - Serialization is the process of converting an object into a stream of bytes in order to store
    an object into memory, so that it can be recreated at a later time, while still keeping the
    object's original state and data. In Android you may use either the Serializable, Externalizable (implements Serializable) or Parcelable interfaces.
    - While Serializable is the easiest to implement, Externalizable may be used if you need to insert custom logic into the process of serialization (although it is almost never used nowadays as it is considered a relic from early versions of Java). But it is highly recommended to use Parcelable in Android instead, as Parcelable was created exclusively for Android and it performs about 10x faster than Serializable, because Serializable uses reflection, which is a slow process and tends to create a lot of temporary objects and it may cause garbage collection to occur more often.
    - To use Serializable all you have to do is implement the interface:

        ```java
        /**
        *  Implementing the Serializeable interface is all that is required
        */
        public class User implements Serializable {

            private String name;
            private String email;

                public User() {
                }

                public String getName() {
                    return name;
                }

                public void setName(final String name) {
                    this.name = name;
                }

                public String getEmail() {
                    return email;
                }

                public void setEmail(final String email) {
                    this.email = email;
                }
            }
        ```
        
    - Parcelable requires a bit more work:

        ```java
            public class User implements Parcelable {

                private String name;
                private String email;

                /**
                 * Interface that must be implemented and provided as a public CREATOR field
                 * that generates instances of your Parcelable class from a Parcel.
                 */
                public static final Creator<User> CREATOR = new Creator<User>() {

                    /**
                     * Creates a new USer object from the Parcel. This is the reason why
                     * the constructor that takes a Parcel is needed.
                     */
                    @Override
                    public User createFromParcel(Parcel in) {
                        return new User(in);
                    }

                    /**
                     * Create a new array of the Parcelable class.
                     * @return an array of the Parcelable class,
                     * with every entry initialized to null.
                     */
                    @Override
                    public User[] newArray(int size) {
                        return new User[size];
                    }
                };

                public User() {
                }

                /**
                 * Parcel overloaded constructor required for
                 * Parcelable implementation used in the CREATOR
                 */
                private User(Parcel in) {
                    name = in.readString();
                    email = in.readString();
                }

                public String getName() {
                    return name;
                }

                public void setName(final String name) {
                    this.name = name;
                }

                public String getEmail() {
                    return email;
                }

                public void setEmail(final String email) {
                    this.email = email;
                }

                @Override
                public int describeContents() {
                    return 0;
                }

                /**
                 * This is where the parcel is performed.
                 */
                @Override
                public void writeToParcel(final Parcel parcel, final int i) {
                    parcel.writeString(name);
                    parcel.writeString(email);
                }
            }
        ```
        Note: For a full explanation of the <b>describeContents()</b> method see [StackOverflow](https://stackoverflow.com/questions/4076946/parcelable-where-when-is-describecontents-used/4914799#4914799).
        In Android Studio, you can have all of the parcelable code auto generated for you, but like with everything else, it is always a good thing to try and understand everything that is happening.

* What is `transient` modifier? [JavaTPoint](https://www.javatpoint.com/transient-keyword) `transient` is a Java keyword which marks a member variable not to be serialized when it is persisted to streams of bytes. When an object is transferred through the network, the object needs to be 'serialized'. Serialization converts the object state to serial bytes.

* What are anonymous classes? [OracleDoc](https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html) It is an inner class without a name and for which only a single object is created. An anonymous inner class can be useful when making an instance of an object with certain “extras” such as overloading methods of a class or interface, without having to actually subclass a class.

* What is the difference between using `==` and `.equals` on an object? [GeeksForGeeks](http://www.geeksforgeeks.org/difference-equals-method-java/) Main difference between .equals() method and == operator is that one is method and other is operator. We can use == operators for reference comparison (address comparison) and .equals() method for content comparison. In simple words, == checks if both objects point to the same memory location whereas .equals() evaluates to the comparison of values in the objects. If a class does not override the equals method, then by default it uses equals(Object o) method of the closest parent class that has overridden this method.

* What is the `hashCode()` and `equals()` used for? In java equals() method is used to compare equality of two Objects. The equality can be compared in two ways:

  - Shallow comparison: The default implementation of equals method is defined in Java.lang.Object class which simply checks if two Object references (say x and y) refer to the same Object. i.e. It checks if x == y. Since Object class has no data members that define its state, it is also known as shallow comparison.
  - Deep Comparison: Suppose a class provides its own implementation of equals() method in order to compare the Objects of that class w.r.t state of the Objects. That means data members (i.e. fields) of Objects are to be compared with one another. Such Comparison based on data members is known as deep comparison.

* Why would you not call abstract method in constructor? Constructors must not invoke overridable methods, directly or indirectly. If you violate this rule, program failure will result. The superclass constructor runs before the subclass constructor, so the overriding method in the subclass will be invoked before the subclass constructor has run. If the overriding method depends on any initialization performed by the subclass constructor, the method will not behave as expected.

* What are anonymous classes? [OracleDoc](https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html) It is an inner class without a name and for which only a single object is created. An anonymous inner class can be useful when making an instance of an object with certain “extras” such as overloading methods of a class or interface, without having to actually subclass a class.

* Can you list 8 primitive types in java?

* When would you make an object value `final`? 

* What are these `final`, `finally` and `finalize` keywords?
  - `final` is a keyword in the java language. It is used to apply restrictions on class, method and variable. Final class can't be inherited, final method can't be overridden and final variable value can't be changed.

	```java
	class FinalExample {
		public static void main(String[] args) {
			final int x=100;
			x=200;//Compile Time Error because x is final
		}
	}
	```
	
  - `finally` is a code block and is used to place important code, it will be executed whether exception is handled or not.

	```java
	class FinallyExample {
		public static void main(String[] args) {
			try {
				int x=300;
			}catch(Exception e) {
				System.out.println(e);
			}
			finally {
				System.out.println("finally block is executed");
			}
		}
	}
	```
	
  - `Finalize` is a method used to perform clean up processing just before object is garbage collected.

	```java
	class FinalizeExample {
		public void finalize() {
			System.out.println("finalize called");
		}

		public static void main(String[] args) {
			FinalizeExample f1=new FinalizeExample();
			FinalizeExample f2=new FinalizeExample();
			f1=null;
			f2=null;
			System.gc();
		}
	}
	```


* What does the `static` word mean in Java?
    - In case of `static` variable it means that this variable (its' value or the object it references) spans across all instances of enclosing class (changing it in one instance affects all others), while in case of `static` methods it means that these methods can be invoked without an instance of their enclosing class. It is useful, for example, when you create util classes that need not be instantiated every time you want to use them.

* Can a `static` method be overridden in Java?
  - While child class can override a static method with another static method with the same signature (return type can be downcasted), it is not truly overridden - it becomes "hidden", but both methods can still be accessed under right circumstances (see question about overloading/overriding above).

* When is a `static` block run?
    - Code inside static block is executed only once: the first time you make an object of that class or the first time you access a static member of that class (even if you never make an object of that class).

* What is reflection? [Jenkov](http://tutorials.jenkov.com/java-reflection/index.html) 
    - Java Reflection makes it possible to inspect classes, interfaces, fields and methods at runtime, without knowing the names of the classes, methods etc. at compile time. It is also possible to instantiate new objects, invoke methods and get/set field values using reflection.

    - Java Reflection is quite powerful and can be very useful. For instance, Java Reflection can be used to map properties in JSON files to getter / setter methods in Java objects, like Jackson, GSON, Boon etc. does. Or, Reflection can be used to map the column names of a JDBC ResultSet to getter / setter methods in a Java object.

* What is Dependency Injection?  Can you name few libraries? Have you used any?
  - Dependency injection is a very powerful technique, where you relay the task of providing object with its' dependencies on instances of other objects (OOP Composition, [Wikipedia](https://en.wikipedia.org/wiki/Object_composition?oldformat=true)) to a separate class. This allows for fewer constructors, setters, factories and builders as all those functions are taken care of by the DI framework that you use. Also, and it may seem as a minor advantage, but if you use DI framework you need not worry about going through the project and changing all of (example names) `YourCustomInterface customInterfaceObject = new YourCustomClass();` to a new implementaion, as long as your new class (in place of `YourCustomClass`) still implements `CustomInterface` - you can just tweak the DI factory class to produce new class and voila - this new class will be automatically instantiated throughout your code. This allows for better maintenence and control over the program. Another example of DI usage is unit-testing - it allows to conveniently inject all needed dependencies and keep the amount of written code at a lower level.
    - One of the most popular libraries for DI for Android is Dagger 2. [Mindorks](https://blog.mindorks.com/a-complete-guide-to-learn-dagger-2-b4c7a570d99c)

* How is a `StringBuilder` implemented to avoid the immutable string allocation problem?

* Difference between `StringBuffer` and `StringBuilder`? [Link](http://www.journaldev.com/137/stringbuffer-vs-stringbuilder)
    1. StringBuffer is the thread safe utility class to perform several operations on Strings. It contains append() and insert() methods that are widely used to perform operation on Strings in a multi-thread environment. If you will check the source code, most of its functions are synchronized for thread safety. Since most of the String operations, for example concatenation happens in a single thread environment, Java 1.5 introduced another utility class StringBuilder to perform similar operations but doesn’t provide thread safety. If you will look into its source code, all the methods are unsynchronized. This is the most important point for StringBuffer vs StringBuilder.
    2. StringBuffer has some extra methods such as substring, length, capacity, trimToSize etc. However these are not required since you have all these present in String too. That’s why these methods were never implemented in StringBuilder class.
	3. StringBuffer was introduced in Java 1.0 whereas StringBuilder class was introduced in Java 1.5 after looking at shortcomings of StringBuffer
    4. StringBuilder is faster than StringBuffer because of no synchronization.

* What’s the difference between an `Enumeration` and an `Iterator`? [Link](http://javaconceptoftheday.com/differences-between-enumeration-vs-iterator-in-java/)
	- Enumeration and Iterator are two interfaces in java.util package which are used to traverse over the elements of a Collection object. Though they perform the same function i.e traversing the Collection object, there are some differences exist between them. Using Enumeration, you can only traverse the Collection object. But using Iterator, you can also remove an element while traversing the Collection. This is the one major difference between Enumeration and Iterator in java. You can say Iterator is some what advanced version of Enumeration. In this post, we will see the differences between Enumeration Vs Iterator In Java.

* What is the difference between fail-fast and fail-safe iterators in Java?
	- Typically, weak consistency (fail-safe) means that if a collection is modified concurrently with an iteration, the guarantees of what the iteration sees are weaker. 
	- "Fail fast" means: it may fail ... and the failure condition is checked aggressively so that the failure condition is (where possible) detected before damage can be done. In Java, a fail-fast iterator fails by throwing a `ConcurrentModificationException`.

* What is Java NIO? [Link](http://tutorials.jenkov.com/java-nio/index.html)

### Core Android

#### Base

* Tell all the Android application components. [Android Official](https://developer.android.com/guide/components/fundamentals.html#Components) 
	- App components are the essential building blocks of an Android app. Each component is an entry point through which the system or a user can enter your app. Some components depend on others. There are four different types of app components:
		- Activities
		- Services
		- Broadcast receivers
		- Content providers
	- Each type serves a distinct purpose and has a distinct lifecycle that defines how the component is created and destroyed.

* What is the structure of an Android Application?
<table class="tablecontent"><tbody><tr><th>Folder Name</th><th>Description</th></tr><tr><td>src</td><td>The 'src' stands for <b>Source Code.</b> It contains the Java Source files.</td></tr><tr><td>gen</td><td>The 'gen' stands for <b>Generated Java Library.</b> This library is for Android internal use only.</td></tr><tr><td>Android 2.2</td><td>The Android Framework Library is stored here.</td></tr><tr><td>assets</td><td>It is used to store raw asset files.</td></tr><tr><td>libs</td><td>It contains private libraries.</td></tr><tr><td>res</td><td>The 'res' stands for <b>Resource file.</b> It can store resource files such as pictures, XML files, etc. It contains some additional folders such as Drawable, Layout and Values.<br><br><b>anim: </b>It is used for XML files that are compiled into animation objects.<br><b>color:</b> It is used for XML files that describe colors.<br><b>drawable:</b> It is used to store various graphics files. In Android project structure,<br><br><b>there are three types of drawable folders,</b><br>1. drawable-mdpi<br>2. drawable-hdpi<br>3. drawable-ldpi<br><br>The above drawable folders are required in order to adapt to different screen resolutions.<br><br><b>layout:</b> It is used for placing the XML layout files, which defines how various Android objects such as textbox, buttons, etc. are organized on the screen.<br><br><b>menu:</b> It is used for defining the XML files in the application menu.<br><br><b>raw:</b> The 'raw' stands for <b>Raw Asset Files.</b> These files are referenced from the application using a resource identifier in the R class.<br><b>For example,</b> good place for media is MP3 or Ogg files.<br><br><b>values:</b> It is used for XML files which stores various string values, such as titles, labels, etc.<br><br><b>xml:</b> It is used for configuring the application components.</td></tr><tr><td>AndroidManifest.xml</td><td>This file indicates the Android definition file. This file contains the information about the Android application such as minimum Android version, permission to access Android device capabilities such as Internet access permission, phone permission etc.</td></tr><tr><td>default.properties</td><td>This file contains the project settings, such as build the target. Do not edit this file manually. It should be maintained in a Source Revision Control System.</td></tr><tr><td>Proguard.cfg</td><td>This file defines how ProGuard optimizes and makes your code unclear.</td></tr><tr><td>MainLayout.xml</td><td>This file describes the layout of the page. So all the components such as textboxes, labels, radio buttons, etc. are displaying on the application screen.</td></tr><tr><td>Activity class</td><td>The application occupies the entire device screen which needs at least one class inherits from the Activity class. OnCreate() method initiates the application and loads the layout page.</td></tr></tbody></table>

* What is `Context`? How is it used? [Medium](https://medium.com/p/understanding-context-in-android-application-330913e32514)
	- It's the context of current state of the application/object. It lets newly-created objects understand what has been going on. Typically you call it to get information regarding another part of your program (activity and package/application). You can get the context by invoking `getApplicationContext()`, `getContext()`, `getBaseContext()` or `this` (when in a class that extends from Context, such as the Application, Activity, Service and IntentService classes).

* What is `AndroidManifest.xml`?
	- Every application must have an AndroidManifest.xml file (with precisely that name) in its root directory. The manifest presents essential information about the application to the Android system, information the system must have before it can run any of the application's code.

* What is `Application` class?
	- The Application class in Android is the base class within an Android app that contains all other components such as activities and services. The Application class, or any subclass of the Application class, is instantiated before any other class when the process for your application/package is created.

		![ApplicationLifeCycle](https://developer.sony.com/reference/docs/sony-addon-sdk/images/smallapp_lifecycle.png)
	
#### Activity

* What is `Activity`? 
	- An activity represents a single screen with a user interface just like window or frame of Java.Android activity is the subclass of ContextThemeWrapper class. 

* Explain `Activity` and `Fragment` lifecycle. (Complete diagram [GitHub](https://github.com/xxv/android-lifecycle), simplified diagram for [Activity](https://developer.android.com/guide/components/activities/activity-lifecycle.html#alc), [Fragment](https://developer.android.com/guide/components/fragments.html#Lifecycle))

![ActivityFragmentLifeCycle](https://i.stack.imgur.com/1llRw.png)

* What are "launch modes"? [Mindorks](https://blog.mindorks.com/android-activity-launchmode-explained-cbc6cf996802)
	- There are four launch modes for activity. They are:
		1. standard. This is the default launch mode of an activity (If not specified). It creates a new instance of an activity in the task from which it was started. Multiple instances of the activity can be created and multiple instances can be added to the same or different tasks. In other words you can create the same activity multiple times in the same task as well as in different tasks.
		2. singleTop. In this launch mode if an instance of activity already exists at the top of the current task, a new instance will not be created and Android system will route the intent information through onNewIntent(). If an instance is not present on top of task then new instance will be created. Using this launch mode you can create multiple instance of the same activity in the same task or in different tasks only if the same instance does not already exist at the top of stack.
		3. singleTask. In this launch mode a new task will always be created and a new instance will be pushed to the task as the root one. If an instance of activity exists on the separate task, a new instance will not be created and Android system routes the intent information through onNewIntent() method. At a time only one instance of activity will exist.
		4. singleInstance. This is very special launch mode and only used in the applications that has only one activity. It is similar to singleTask except that no other activities will be created in the same task. Any other activity started from here will create in a new task.

#### Fragments

* What is `Fragment`?
	- A Fragment represents a behavior or a portion of user interface in a FragmentActivity. You can combine multiple fragments in a single activity to build a multi-pane UI and reuse a fragment in multiple activities. You can think of a fragment as a modular section of an activity, which has its own lifecycle, receives its own input events, and which you can add or remove while the activity is running (sort of like a "sub activity" that you can reuse in different activities). A fragment must always be hosted in an activity and the fragment's lifecycle is directly affected by the host activity's lifecycle.

* What is the difference between a `Fragment` and an `Activity`? Explain the relationship between the two.
	- A fragment has its own layout and its own behavior with its own lifecycle callbacks. You can add or remove fragments in an activity while the activity is running. You can combine multiple fragments in a single activity to build a multi-pane UI. A fragment can implement a behavior that has no user interface component.

* Why is it recommended to use only the default constructor to create a `Fragment`? [StackOverflow](https://stackoverflow.com/a/16042750/2809326)
	- The reason why you should be passing parameters through bundle is because when the system restores a fragment (e.g on config change), it will automatically restore your bundle.

	- The callbacks like onCreate or onCreateView should read the parameters from the bundle - this way you are guaranteed to restore the state of the fragment correctly to the same state the fragment was initialised with (note this state can be different from the onSaveInstanceState bundle that is passed to the onCreate/onCreateView)

	- The recommendation of using the static newInstance() method is just a recommendation. You can use a non default constructor but make sure you populate the initialisation parameters in the bundle inside the body of that constructor. And read those parameters in the onCreate() or onCreateView() methods.

* How would you communicate between two Fragments? [Android Official](https://developer.android.com/training/basics/fragments/communicating.html)

	-  All Fragment-to-Fragment communication is done either through a shared ViewModel or through the associated Activity. Two Fragments should never communicate directly.
	-  ViewModel objects are designed to outlive specific instantiations of views or LifecycleOwners. This design also means you can write tests to cover a ViewModel more easily as it doesn't know about view and Lifecycle objects. ViewModel objects can contain LifecycleObservers, such as LiveData objects. However ViewModel objects must never observe changes to lifecycle-aware observables, such as LiveData objects. If the ViewModel needs the Application context, for example to find a system service, it can extend the AndroidViewModel class and have a constructor that receives the Application in the constructor, since Application class extends Context.

		![ViewModelLifeCycle](https://developer.android.com/images/topic/libraries/architecture/viewmodel-lifecycle.png)
	
* What is retained `Fragment`? [AndroidDesignPatterns](https://www.androiddesignpatterns.com/2013/04/retaining-objects-across-config-changes.html)
	- "retained" means that the fragment will not be destroyed on configuration changes. That is, the Fragment will be retained even if the configuration change causes the underlying Activity to be destroyed.
	- Just like Activitys, Fragments may be destroyed by the system when memory resources are low. Whether you have your fragments retain their instance state across configuration changes will have no effect on whether or not the system will destroy the Fragments once you leave the Activity. If you leave the Activity (i.e. by pressing the home button), the Fragments may or may not be destroyed. If you leave the Activity by pressing the back button (thus, calling finish() and effectively destroying the Activity), all of the Activitys attached Fragments will also be destroyed.
	- Retained fragments can be quite useful for propagating state information — especially thread management — across activity instances. For example, a fragment can serve as a host for an instance of Thread or AsyncTask, managing its operation. In general, I would treat it similarly to using onConfigurationChanged with an Activity... don't use it as a bandaid just because you are too lazy to implement/handle an orientation change correctly. Only use it when you need to.

#### Views and ViewGroups

* What is `View` in Android?
	- View is a basic building block of UI (User Interface) in android. A view is a small rectangular box which responds to user inputs. Eg: EditText , Button , CheckBox , etc.. ViewGroup is a invisible container of other views (child views) and other viewgroups.

		![ViewLifeCycle](https://codentrick.com/content/images/2015/07/android_view_lifecycle.png)
	
* Difference between `View.GONE` and `View.INVISIBLE`?
	- `View.INVISIBLE` This view is invisible, but it still takes up space for layout purposes. `View.GONE` This view is invisible, and it doesn't take any space for layout purposes.

* Can you create custom views? How?
	- If you only need to make small adjustments to an existing widget or layout, you can simply subclass the widget or layout and override its methods. Creating your own View subclasses gives you precise control over the appearance and function of a screen element.

* What are ViewGroups and how they are different from the Views?
	- A ViewGroup is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers. This class also defines the ViewGroup.LayoutParams class which serves as the base class for layouts parameters.

	- View class represents the basic building block for user interface components. A View occupies a rectangular area on the screen and is responsible for drawing and event handling. View is the base class for widgets, which are used to create interactive UI components (buttons, text fields, etc.).

* What is a canvas?
	- The Canvas class holds the "draw" calls. To draw something, you need 4 basic components: A Bitmap to hold the pixels, a Canvas to host the draw calls (writing into the bitmap), a drawing primitive (e.g. Rect, Path, text, Bitmap), and a paint (to describe the colors and styles for the drawing).

* What is a `SurfaceView`?
	- When you create a custom view and override its onDraw() method, all drawing happens on the UI thread. Drawing on the UI thread puts an upper limit on how long or complex your drawing operations can be, because your app has to complete all its work for every screen refresh. One option is to move some of the drawing work to a different thread using a SurfaceView. 
		- All the views in your view hierarchy are rendered onto one Surface in the UI thread.
		- In the context of the Android framework, Surface refers to a lower-level drawing surface whose contents are eventually displayed on the user's screen.
		- A SurfaceView is a view in your view hierarchy that has its own separate Surface, as shown in the diagram below. You can draw to it in a separate thread.
		- To draw, start a thread, lock the SurfaceView's canvas, do your drawing, and post it to the Surface.

* Relative Layout vs Linear Layout.
	- `LinearLayout` adds view linearly either vertical or horizontal by the orientation set by you. It will add views one after another which will depend on the requirement of the design. And `RelativeLayout` adds view related with each other, there is no need to declare orientation in `RelativeLayout`.

* Tell about Constraint Layout [Mindorks](https://blog.mindorks.com/using-constraint-layout-in-android-531e68019cd)
	- Intention of `ConstraintLayout` is to optimize and flatten the view hierarchy of your layouts by applying some rules to each view to avoid nesting. Rules remind you of `RelativeLayout`, for example setting the left to the left of some other view.
```
app:layout_constraintBottom_toBottomOf="@+id/view1"
```
	- Unlike `RelativeLayout`, `ConstraintLayout` offers bias value that is used to position a view in terms of 0% and 100% horizontal and vertical offset relative to the handles (marked with circle). These percentages (and fractions) offer seamless positioning of the view across different screen densities and sizes.
   ```java
	app:layout_constraintHorizontal_bias="0.33" <!-- from 0.0 to 1.0 -->
	app:layout_constraintVertical_bias="0.53" <!-- from 0.0 to 1.0 -->
   ```
	- Baseline handle (long pipe with rounded corners, below the circle handle) is used to align content of the view with another view reference. Square handles (on each corner of the view) are used to resize the view in dps.

* Do you know what is the view tree? How can you optimize its depth?

#### Displaying Lists of Content

* What is the difference between `ListView` and `RecyclerView`?
	- The RecyclerView is much more powerful, flexible and a major enhancement over ListView
		1. ViewHolder Pattern. In a ListView, it was recommended to use the ViewHolder pattern but it was never a compulsion. In case of RecyclerView, this is mandatory using the RecyclerView.ViewHolder class. This is one of the major differences between the ListView and the RecyclerView. It makes things a bit more complex in RecyclerView but a lot of problems that we faced in the ListView are solved efficiently.
		2. LayoutManager. This is another massive enhancement brought to the RecyclerView. In a ListView, the only type of view available is the vertical ListView. There is no official way to even implement a horizontal ListView.
		3. Item Animator. ListViews are lacking in support of good animations, but the RecyclerView brings a whole new dimension to it. Using the RecyclerView.ItemAnimator class, animating the views becomes so much easy and intuitive.
		4. Item Decoration. In case of ListViews, dynamically decorating items like adding borders or dividers was never easy. But in case of RecyclerView, the RecyclerView.ItemDecorator class gives huge control to the developers but makes things a bit more time consuming and complex.
		5. OnItemTouchListener. Intercepting item clicks on a ListView was simple, thanks to its AdapterView.OnItemClickListener interface. But the RecyclerView gives much more power and control to its developers by the RecyclerView.OnItemTouchListener but it complicates things a bit for the developer.

	- In simple words, the RecyclerView is much more customizable than the ListView and gives a lot of control and power to its developers.

* What is the ViewHolder pattern? Why should we use it?
	- The ViewHolder design pattern enables you to access each list item view without the need for the look up, saving valuable processor cycles. Specifically, it avoids frequent call of findViewById() during ListView scrolling, and that will make it smooth.

* What is `SnapHelper`? [Mindorks](https://blog.mindorks.com/using-snaphelper-in-recyclerview-fc616b6833e8)
	- SnapHelper is a helper class that helps in snapping any child view of the RecyclerView. For example, you can snap the firstVisibleItem of the RecyclerView as you must have seen in the play store application that the firstVisibleItem will be always completely visible when scrolling comes to the idle position.

#### Dialogs and Toasts

* What is `Dialog` in Android?
	- A dialog is a small window that prompts the user to make a decision or enter additional information. A dialog does not fill the screen and is normally used for modal events that require users to take an action before they can proceed.

* What is `Toast` in Android?
	- A toast provides simple feedback about an operation in a small popup. It only fills the amount of space required for the message and the current activity remains visible and interactive. Toasts automatically disappear after a timeout.

* What the difference between `Dialog` and `Dialog Fragment`?
	- A DialogFragment is a fragment that displays a dialog window, floating on top of its activity's window. This fragment contains a Dialog object, which it displays as appropriate based on the fragment's state. Control of the dialog (deciding when to show, hide, dismiss it) should be done through the API, not with direct calls on the dialog.

#### Intents and Broadcasting

* What is `Intent`? [StackOverflow](https://stackoverflow.com/questions/6578051/what-is-an-intent-in-android)
	- An Intent is basically a message to say you did or want something to happen. Depending on the intent, apps or the OS might be listening for it and will react accordingly. Think of it as a blast email to a bunch of friends, in which you tell your friend John to do something, or to friends who can do X ("intent filters"), to do X. The other folks will ignore the email, but John (or friends who can do X) will react to it.

* What is an Implicit `Intent`?
	- Is something which is sent from one activity to inbuilt android activity in android. When we work with implicit intents, we generally specify the action which we want to perform and optionally some data required for that action. Data is typically expressed as a Uri which can represent an image in the gallery or person in the contacts database. Implicit Intents do not directly specify the Android components which should be called , it only specifies action to be performed. An Uri can be used with the implicit intent to specify data type.

	```java
	Intent intent = new Intent(ACTION_VIEW, Uri.parse("http://www.google.com");
	```

* What is an Explicit `Intent`?
	- Explicit intents are used in the application itself wherein one activity can switch to other activty.

	```java
	Intent intent = new Intent(this, Target.class); 
	```
	
	- this causes switching of activity from current context to the target activity. Explicit Intents can also be used to pass data to other activity using putExtra method and retrieved by target activity by getIntent().getExtras() methods.

* What is a `ContentProvider`? 

	- They encapsulate data and provide it to applications through the single ContentResolver interface. A content provider is only required if you need to share data between multiple applications. For example, the contacts data is used by multiple applications and must be stored in a content provider. If you don't need to share data amongst multiple applications you can use a database directly via SQLiteDatabase.

	- When a request is made via a ContentResolver the system inspects the authority of the given URI and passes the request to the content provider registered with the authority. The content provider can interpret the rest of the URI however it wants. The UriMatcher class is helpful for parsing URIs.

	- The primary methods that need to be implemented are:

		- `onCreate()` which is called to initialize the provider.
		- `query(Uri, String[], Bundle, CancellationSignal)` which returns data to the caller.
		- `insert(Uri, ContentValues)` which inserts new data into the content provider.
		- `update(Uri, ContentValues, String, String[])` which updates existing data in the content provider.
		- `delete(Uri, String, String[])` which deletes data from the content provider.
		- `getType(Uri)` which returns the MIME type of data in the content provider.

* What is a `BroadcastReceiver`? [StackOverflow](https://stackoverflow.com/questions/5296987/what-is-broadcastreceiver-and-when-we-use-it)
	- A broadcast receiver is a component that responds to system-wide broadcast announcements. Many broadcasts originate from the system—for example, a broadcast announcing that the screen has turned off, the battery is low, or a picture was captured. Applications can also initiate broadcasts—for example, to let other applications know that some data has been downloaded to the device and is available for them to use. Although broadcast receivers don't display a user interface, they may create a status bar notification to alert the user when a broadcast event occurs.

* What is a `LocalBroadcastManager`? [Developer Android](https://developer.android.com/reference/android/support/v4/content/LocalBroadcastManager.html)
	- Helper to register for and send broadcasts of Intents to local objects within your process. This has a number of advantages over sending global broadcasts with `sendBroadcast(Intent)`:
		- You know that the data you are broadcasting won't leave your app, so don't need to worry about leaking private data.
		- It is not possible for other applications to send these broadcasts to your app, so you don't need to worry about having security holes they can exploit.
		- It is more efficient than sending a global broadcast through the system.

* What is the function of an `IntentFilter`?
	- An intent filter is an expression in an app's manifest file that specifies the type of intents that the component would like to receive. `IntentFilter` objects are often created in XML as part of a package's `AndroidManifest.xml` file, using `intent-filter` tags.

	```java
	<intent-filter>
	    <data android:mimeType="image/*" />
	    ...
	</intent-filter>
	```
* What is a Sticky `Intent`? [AndroidInterview](http://www.androidinterview.com/what-is-a-sticky-intent/)
	- Sticky Intent is also a type of Intent which allows a communication between function and a service sendStickyBroadcast() performs a sendBroadcast(Inent) know as sticky,the Intent your are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of registerReceiver(BroadcastReceiver, IntentFilter). In all other ways, this behaves the same as sendBroadcast(Intent).

* Describe how broadcasts and intents work to be able to pass messages around your app?
	- When a broadcast intent is created, it must include an action string in addition to optional data and a category string. As with standard intents, data is added to a broadcast intent using key-value pairs in conjunction with the putExtra() method of the intent object. The optional category string may be assigned to a broadcast intent via a call to the addCategory() method.

	- The action string, which identifies the broadcast event, must be unique and typically uses the application’s Java package name syntax. For example, the following code fragment creates and sends a broadcast intent including a unique action string and data:

	```java
	Intent intent = new Intent();
	intent.setAction("com.example.Broadcast");
	intent.putExtra("HighScore", 1000);
	sendBroadcast(intent);
	```
	- The above code would successfully launch the corresponding broadcast receiver on a device running an Android version earlier than 3.0. On more recent versions of Android, however, the intent would not be received by the broadcast receiver. This is because Android 3.0 introduced a launch control security measure that prevents components of stopped applications from being launched via an intent. An application is considered to be in a stopped state if the application has either just been installed and not previously launched, or been manually stopped by the user using the application manager on the device. To get around this, however, a flag can be added to the intent before it is sent to indicate that the intent is to be allowed to start a component of a stopped application. This flag is FLAG_INCLUDE_STOPPED_PACKAGES and would be used as outlined in the following adaptation of the previous code fragment:

	```java
	Intent intent = new Intent();
	intent.addFlags(Intent.FLAG_INCLUDE_STOPPED_PACKAGES);
	intent.setAction("com.example.Broadcast");
	intent.putExtra("HighScore", 1000);
	sendBroadcast(intent);
	```

* What is a `PendingIntent`?
	- A PendingIntent is a token that you give to a foreign application (e.g. NotificationManager, AlarmManager, Home Screen AppWidgetManager, or other 3rd party applications), which allows the foreign application to use your application's permissions to execute a predefined piece of code.

	- If you give the foreign application an Intent, it will execute your Intent with its own permissions. But if you give the foreign application a PendingIntent, that application will execute your Intent using your application's permission.

* What are the different types of Broadcasts?
	- Normal broadcasts: Normal broadcasts (sent with Context.sendBroadcast) are completely asynchronous. All receivers of the broadcast are run in an undefined order, often at the same time. This is more efficient, but means that receivers cannot use the result or abort APIs included here.

	- Ordered broadcasts: Ordered Broadcast is the type of broadcast which is sent in a synchronous manner i.e. one by one to each listener. Android sendOrderedBroadcast method falls in Context class of Android, the purpose of this method is to broadcast to listening receivers in a serialized manner and receive the result back to the calling activity. 

	- Sticky broadcasts: A Sticky Broadcast is a Broadcast that stays around following the moment it is announced to the system. Most Broadcasts are sent, processed within the system and become quickly inaccessible. However, Sticky Broadcasts announce information that remains accessible beyond the point at which they are processed. A typical example is the battery level Broadcast. Unlike most Broadcasts, the battery level can be retrieved within applications beyond the point at which it was sent through the system. This means that apps can find out whatever the last battery level broadcast was.

#### Services

* What is `Service`?
	- A Service is an application component that can perform long-running operations in the background, and it doesn't provide a user interface. Another application component can start a service, and it continues to run in the background even if the user switches to another application. Additionally, a component can bind to a service to interact with it and even perform interprocess communication (IPC). For example, a service can handle network transactions, play music, perform file I/O, or interact with a content provider, all from the background.

	- These are the three different types of services:

	> Foreground
	
	- A foreground service performs some operation that is noticeable to the user. For example, an audio app would use a foreground service to play an audio track. Foreground services must display a Notification. Foreground services continue running even when the user isn't interacting with the app.

	> Background
	
	- A background service performs an operation that isn't directly noticed by the user. For example, if an app used a service to compact its storage, that would usually be a background service. Note: If your app targets API level 26 or higher, the system imposes restrictions on running background services when the app itself isn't in the foreground. In most cases like this, your app should use a scheduled job instead.

	> Bound
	
	- A service is bound when an application component binds to it by calling bindService(). A bound service offers a client-server interface that allows components to interact with the service, send requests, receive results, and even do so across processes with interprocess communication (IPC). A bound service runs only as long as another application component is bound to it. Multiple components can bind to the service at once, but when all of them unbind, the service is destroyed.

* `Service` vs `IntentService`. [StackOverflow](https://stackoverflow.com/a/15772151/5153275)
	- `Service` is a base class of service implementation. `Service` class is run in the application’s main thread which may reduce the application performance. Thus, `IntentService`, which is a direct subclass of `Service` is borned to make things easier. The `IntentService` is used to perform a certain task in the background. Once done, the instance of `IntentService` terminate itself automatically. Examples for its usage would be to download a certain resources from the Internet.
	- A `Service` is a broader implementation for the developer to set up background operations, while an `IntentService` is useful for “fire and forget” operations, taking care of background Thread creation and cleanup.

* What is a `JobScheduler`? [Vogella](http://www.vogella.com/tutorials/AndroidTaskScheduling/article.html)
	- JobScheduler is the Android framework API for scheduling tasks or work. It first became available in Android 5.0 (API level 21), and remains under active development. Notably, Android 7.0 (API level 24) added the ability to trigger jobs based on ContentProvider changes.

	- JobScheduler is implemented in the platform, which allows it to collect information about jobs that need to run across all apps. This information is used to schedule jobs to run at, or around, the same time. Batching job execution in this fashion allows the device to enter and stay in sleep states longer, preserving battery life.

	- You use JobScheduler by registering jobs, specifying their requirements for network and timing. The system then gracefully schedules the jobs to execute at the appropriate times. At the same time, it also defers job execution as necessary to comply with Doze and App Standby restrictions. JobScheduler provides many methods to define job-execution conditions.

#### Inter-process Communication

* How can two distinct Android apps interact?
	- An Intent can be explicit in order to start a specific component (a specific Activity instance) or implicit in order to start any component that can handle the intended action (such as "capture a photo").

* Is it possible to run an Android app in multiple processes? How?
	- You can specify android:process=":remote" in your manifest to have an activity/service run in a seperate process.

	- The "remote" is just the name of the remote process, and you can call it whatever you want. If you want several activities/services to run in the same process, just give it the same name.

```java
<activity android:name=".RemoteActivity" android:label="@string/app_name" android:process=":RemoteActivityProcess"/>
```

* What is AIDL? Enumerate the steps in creating a bounded service through AIDL.
	- On Android, one process cannot normally access the memory of another process. So to talk, they need to decompose their objects into primitives that the operating system can understand, and marshall the objects across that boundary for you. The code to do that marshalling is tedious to write, so Android handles it for you with AIDL. To create a bounded service using AIDL, follow these steps:

		1. Create the .aidl file. This file defines the programming interface with method signatures.
		2. Implement the interface. The Android SDK tools generate an interface in the Java programming language, based on your .aidl file. This interface has an inner abstract class named Stub that extends Binder and implements methods from your AIDL interface. You must extend the Stub class and implement the methods.
		3. Expose the interface to clients. Implement a Service and override onBind() to return your implementation of the Stub class.

* What can you use for background processing in Android?

* What is a `ContentProvider` and what is it typically used for?
	- A ContentProvider manages access to a structured set of data. It encapsulates the data and provide mechanisms for defining data security. ContentProvider is the standard interface that connects data in one process with code running in another process.


#### Long-running Operations

* How would you perform a long-running operation in an application?
	- AsyncTask. Easy to implement and returns results on the main thread. There are some issues with AsyncTask, for example, they are not aware of the activity or fragment lifecycle and so it is the programmer's responsibility to handle the AsyncTasks behaviour when the activity is destroyed. This means that they are not the best option for long running operations and also, if the app is in the background and the app is terminated by Android, your background processing is also terminated.
	- IntentService. This is the defacto choice for long running processing on Android, a good example would be to upload or download large files. The upload and download may continue even if the user exits the app and you certainly do not want to block the user from being able to use the app while these tasks are going on.
	- Loader. Loaders were introduced in Android Honeycomb and are part of the compatibility library. They are aware of Fragment and Activity lifecycle and can even cache loaded data. I would like to bring attention to AsyncTaskLoaders as they solve a lot of problems that are inherent to AsyncTask.
	- JobScheduler. JobScheduler was released in API 21 and as yet there is not official compatibility version from Google (Evan Tatarka has filled the void with JobSchedulerCompat). It is important to remember that there is no guarantee that your code will be executed as soon as these conditions are met or the order of the execution.
	- CountDownTimer. This is very easy to use however it is context sensitive, so if you exit your Activity or Fragment, you need to clean this up by cancelling it. There really is nothing Asynchronous about CountDownTimer. If you look at it’s source, it simply posts delayed messages on a Handler which means that it will run on whatever thread you launch it from and onTick() and onFinish() will be executed on whatever thread you run the CountDownTimer from so you can do UI updates in it. For this reason, it’s also important to not do any heavy operations onTick() or onFinish(). The reason CountDownTimer is included in the list is because using this class does not block the user from using the app even when the CountDownTimer is initialised from the main thread, effectively giving a asynchronous effect. Also keep in mind, if your update intervals are small and your processing is time consuming, you can have a back-pressure problem which will result in blocking of your execution thread.
	- Java Threads or Android HandlerThread. Java Threads are rather straight forward to implement. However, they are best to avoid in Android. I have seen them used in all sorts of instances however they are limiting as Android doesn’t really allow UI updates on the background thread. A better option may be to use AsyncTask.
	- FutureTask. FutureTask performs asynchronous processing, however, if the result is not ready yet or processing has not complete, calling get() will be block the thread.
	- Java Timer / ScheduledThreadPoolExecutor. An example of using Java Timer to do something after 5 seconds. These can be used to schedule some processing on a background thread. There are other ways to handle the same in Android, you could use a Handler with postDelayed or Handler with sendMessageDelayed() and the handler can run on a background thread as shown above. Also, keep in mind that since this API is not aware of the Android lifecycle, any hard reference to an Activity, Fragment or View in here is a possible memory leak.
* Why should you avoid to run non-ui code on the main thread?
	- Because if that thread hogs it prevents user interaction (for more than 5 seconds), it causes Android to throw up the infamous Android Not Responsive (ANR) error.

* What is ANR? How can the ANR be prevented?
	- When the UI thread of an Android app is blocked for too long (5 seconds), an "Application Not Responding" (ANR) error is triggered. If the app is in the foreground, the system displays a dialog to the user. The ANR dialog gives the user the opportunity to force quit the app. To avoid it, you must identify the places in your code where the app’s main thread is busy for more than 5 seconds. Look for the suspicious use cases in your app and try to reproduce the ANR.

* What is an `AsyncTask`?
	- AsyncTask is an abstract Android class which helps the Android applications to handle the Main UI thread in efficient way. AsyncTask class allows us to perform long lasting tasks/background operations and show the result on the UI thread without affecting the main thread.

* What are the problems in asynctask?
	- When the device configuration changes, the entire Activity is destroyed and recreated. When the Activity is restarted, your AsyncTask’s reference to the Activity is invalid, so onPostExecute() will have no effect on the new Activity.
	- It is a misconception to think that just because the Activity that originally spawned the AsyncTask is dead, the AsyncTask is as well. It will continue running on its merry way even if you exit the entire application. The only way that an AsyncTask finishes early is if it is canceled via `AsyncTask.cancel()`. This means that you have to manage the cancellation of AsyncTasks yourself; otherwise you run the risk of bogging down your app with unnecessary background tasks, or of leaking memory.
	- There’s a misconception about what AsyncTask.cancel() actually does. It does not kill the Thread with no regard for the consequences! All it does is set the AsyncTask to a “cancelled” state. As for mayInterruptIfRunning – all it does is send an interrupt() to the running Thread. In the case that your Thread is uninterruptible, then it won’t stop the Thread at all.

* When would you use java thread instead of an asynctask?
	- Use AsyncTask for:
		- Simple network operations which do not require downloading a lot of data
		- Disk-bound tasks that might take more than a few milliseconds

	- Use Java threads for:
		- Network operations which involve moderate to large amounts of data (either uploading or downloading)
		- High-CPU tasks which need to be run in the background
		- Any task where you want to control the CPU usage relative to the GUI thread

* What is a `Loader`?
	- A `Loader` make it easy to asynchronously load data in an activity or fragment They are available to every Activity and Fragment. They provide asynchronous loading of data. They monitor the source of their data and deliver new results when the content changes. They automatically reconnect to the last loader's cursor when being recreated after a configuration change. Thus, they don't need to re-query their data.

* What is the relationship between the life cycle of an `AsyncTask` and an `Activity`? What problems can this result in? How can these problems be avoided?
	- An `AsyncTask` is not tied to the life cycle of the `Activity` that contains it. So, for example, if you start an `AsyncTask` inside an `Activity` and the user rotates the device, the `Activity` will be destroyed (and a new `Activity` instance will be created) but the `AsyncTask` will not die but instead goes on living until it completes. 
	- Then, when the `AsyncTask` does complete, rather than updating the UI of the new `Activity`, it updates the former instance of the `Activity` (i.e., the one in which it was created but that is not displayed anymore!). This can lead to an Exception (of the type `java.lang.IllegalArgumentException`: View not attached to window manager if you use, for instance, `findViewById` to retrieve a view inside the `Activity`).
	- There’s also the potential for this to result in a memory leak since the AsyncTask maintains a reference to the `Activity`, which prevents the `Activity` from being garbage collected as long as the `AsyncTask` remains alive.

* Explain `Looper`, `Handler` and `HandlerThread`. [Mindorks](https://blog.mindorks.com/android-core-looper-handler-and-handlerthread-bd54d69fe91a)
	- `Looper` is a worker, that serves a `MessageQueue` for a current thread.
	- `Handler` is a class with 2 basic functions: post tasks to the MessageQueue and process them. By default, Handler is implicitly associated with thread it was instantiated from via Looper, but you can tie it to another thread by explicitly providing its Looper at the constructor call as well. 
	- `HandlerThread` is a derivation of `Thread`. The only significant difference between `HandlerThread` and `Thread` you should turn your attention to is that the first one incorporates `Looper`, `Thread` and `MessageQueue`.

	![HandlerThread](https://s.nikitaog.me/android/Looper.png)

#### Working With Multimedia Content

* How do you handle bitmaps in Android as it takes too much memory?
	- A memory cache offers fast access to bitmaps at the cost of taking up valuable application memory. The LruCache class is particularly well suited to the task of caching bitmaps, keeping recently referenced objects in a strong referenced LinkedHashMap and evicting the least recently used member before the cache exceeds its designated size.
	- If you just want to cache bitmaps off the heap, a simpler solution is to use parcel memory. Parcel uses the native malloc heap. The bitmap will be opaque and there is no way to access the data while it is parceled. But if keeping a (few) large bitmap(s) cached away from the heap is your only goal, it's the simplest solution.

* What is the difference between a regular `Bitmap` and a nine-patch image?
	- It is one of a resizable bitmap resource which is being used as backgrounds or other images on the device. The NinePatch class allows drawing a bitmap in nine sections. The four corners are unscaled; the middle of the image is scaled in both axes, the four edges are scaled into one axis.

* Tell about the `Bitmap` pool. [Mindorks](https://blog.mindorks.com/how-to-use-bitmap-pool-in-android-56c71a55533c)
	- From API 11 onwards, you can pass a bitmap to be reused in the BitmapFactory Options. You will need to implement a bitmap pool to make it easy to manage your bitmaps. Pooling currently only works for Bitmaps that are exactly the same size. For this reason you need to be careful when you use it and/or use different pools for different size bitmaps. 
	- It may also be worth while to know the difference between bitmap ARGB_8888 and RGB_565. ARGB_8888 has 32-bit color which also supports alpha transparencies. RGB_565 does not support alpha transparencies and is 16-bit color. 
* How to play sounds in Android? [Vogella](http://www.vogella.com/tutorials/AndroidMedia/article.html)
	- Android gives you a couple of options to do so:
		- The SoundPool is best for short sound clips (notifications sounds, sound effects in games).
		- The MediaPlayer is better suited for larger sound files like songs.

#### Data Saving

* How to persist data in an Android app?
	- It depends on your specific needs, such as how much space your data requires, what kind of data you need to store, and whether the data should be private to your app or accessible to other apps and the user.
		- Internal file storage: Store app-private files on the device file system. Files saved to the internal storage are private to your app, and other apps cannot access them (nor can the user, unless they have root access). 
		- External file storage: Store files on the shared external file system. This is usually for shared user files, such as photos. Files saved to the external storage are world-readable and can be modified by the user when they enable USB mass storage to transfer files on a computer.
		- Shared preferences: Store private primitive data in key-value pairs. The key-value pairs are written to XML files that persist across user sessions, even if your app is killed. You can manually specify a name for the file or use per-activity files to save your data.
		- Databases: Store structured data in a private database. Any database you create is accessible only by your app. However, instead of using SQLite APIs directly, we recommend that you create and interact with your databases with the Room persistence library. The Room library provides an object-mapping abstraction layer that allows fluent database access while harnessing the full power of SQLite.

* What is ORM? How does it work?
	- Object-relational mapping (ORM) is a programming technique in which a metadata descriptor is used to connect object code to a relational database. Object code is written in object-oriented programming (OOP) languages such as Java. ORM converts data between type systems that are unable to coexist within relational databases and OOP languages.
	- Android Room provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. There are 3 major components in Room:
		- Database: Contains the database holder and serves as the main access point for the underlying connection to your app's persisted, relational data. The class that's annotated with @Database should satisfy the following conditions:
			- Be an abstract class that extends RoomDatabase.
			- Include the list of entities associated with the database within the annotation.
			- Contain an abstract method that has 0 arguments and returns the class that is annotated with @Dao. At runtime, you can acquire an instance of Database by calling Room.databaseBuilder() or Room.inMemoryDatabaseBuilder().

        ```java
			@Database(entities = {User.class}, version = 1)
			public abstract class AppDatabase extends RoomDatabase {
			    public abstract UserDao userDao();
			}
        ```
        
		- Entity: Represents a table within the database.

        ```java
			@Entity
			public class User {
			    @PrimaryKey
			    private int uid;
			
			    @ColumnInfo(name = "first_name")
			    private String firstName;
			
			    @ColumnInfo(name = "last_name")
			    private String lastName;
			
			    // Getters and setters are ignored for brevity,
			    // but they're required for Room to work.
			}
        ```
        
		- DAO: Contains the methods used for accessing the database.

        ```java
			@Dao
			public interface UserDao {
			    @Query("SELECT * FROM user")
			    List<User> getAll();
			
			    @Query("SELECT * FROM user WHERE uid IN (:userIds)")
			    List<User> loadAllByIds(int[] userIds);
			
			    @Query("SELECT * FROM user WHERE first_name LIKE :first AND "
			           + "last_name LIKE :last LIMIT 1")
			    User findByName(String first, String last);
			
			    @Insert
			    void insertAll(User... users);
			
			    @Delete
			    void delete(User user);
			}
        ```
	- After creating the files above, you get an instance of the created database using the following code:
	```java
	AppDatabase db = Room.databaseBuilder(getApplicationContext(), AppDatabase.class, "database-name").build();
	```

* How would you preserve `Activity` state during a screen rotation? [StackOverflow](https://stackoverflow.com/questions/3915952/how-to-save-state-during-orientation-change-in-android-if-the-state-is-made-of-m)
	- When orientation changes, Android destroys your current activity and creates a new activity again. And whenever Android destroys and recreates your Activity for orientation change, it calls onSaveInstanceState() before destroying and calls onCreate() after recreating. Whatever you save in the bundle in onSaveInstanceState, you can get back from the onCreate() parameter.
* What are different ways to store data in your Android app?

#### Look and Feel

* What is a `Spannable`?
	- Spannable is a Spanned, adding in the ability to modify the spans (to add or remove formatting), but not to modify the text itself. This is the interface for text to which markup objects can be attached and detached. Not all Spannable classes have mutable text; see Editable for that.

#### Memory Optimizations

* What is the `onTrimMemory()` method?
	- One way of managing memory in response to system events is the onTrimMemory() method. It's called when the operating system has determined that it is a good time for a process to trim unneeded memory from its process. This will happen for example when it goes in the background and there is not enough memory to keep as many background processes running as desired.

* How does the OutOfMemory happens?
	- The reasons why JVM may throw OutOfMemoryError, could be:
		- Java heap space: when trying to allocate an object or an array larger than maximum continuous free block in either of heap generations;
		- GC overhead limit exceeded: when the proportion of time JVM spends doing garbage collection becomes too high (see GCTimeLimit, GCHeapFreeLimit);
		- PermGen space (before Java 8) or Metaspace (since Java 8): when the amount of class metadata exceeds MaxPermSize or MaxMetaspaceSize;
		- Requested array size exceeds VM limit: when trying to allocate an array with length larger than Integer.MAX_VALUE - 2;
		- Unable to create new native thread: when reaching the OS limit of user processes (see ulimit -u) or when there is not enough virtual memory to reserve space for thread stack;
		- Direct buffer memory: when the size of all direct ByteBuffers exceeds MaxDirectMemorySize or when there is no virtual memory available to satisfy direct buffer allocation;
		- When JVM cannot allocate memory for its internal structures, either because run out of available virtual memory or because certain OS limit reached (e.g. maximum number of memory map areas);
		- When JNI code failed to allocate some native resource;
		- Etc. Not to mention that an application can throw OutOfMemoryError itself at any time just because a developer decides so.

* How do you find memory leaks in Android applications? [Mindorks](https://mindorks.com/blog/detecting-and-fixing-memory-leaks-in-android)
	- Android Studio has a handy tool for detecting memory leaks. If you suspect a piece of code in you app might leaks an Activity, you can do this. Dump Java Heap and use the Analyzer Tasks tool from  HPROF Viewer and Analyzer.

#### Battery Life Optimizations

* How to reduce battery usage in an android application? [Mindorks](https://blog.mindorks.com/battery-optimization-for-android-apps-f4ef6170ff70)
	- Tips for improving battery usage in an android application:
		- Reduce network calls as much as you can: Cache your data and retrieve it from the cache when required next time.
		- Avoid wake lock as much as possible: A wake lock is a mechanism to indicate that your application needs to have the device stay on.
		- Use AlarmManager carefully: Wrong use of AlarmManager can easily drain the battery.
Batch the network calls: You should batch the network calls if possible so that you can prevent the device from waking every second.
		- A Different logic for Mobile Data and Wifi: You should write different logic for mobile data and wifi as one logic may be optimized for mobile data and other may be optimized for wifi.
		- Check all background processes: You should check all the background processes.
		- Use GPS carefully: Do not use it frequently, use it only when actually required.
		- Use JobScheduler: This is an API for scheduling various types of jobs against the framework that will be executed in your application’s own process. The framework will be intelligent about when you receive your callbacks and attempt to batch and defer them as much as possible. For backward compatibility use Evernote’s android-job library.

* What is Doze? What about App Standby?
	- Doze reduces battery consumption by deferring background CPU and network activity for apps when the device is unused for long periods of time.
	- App Standby defers background network activity for apps with which the user has not recently interacted.

* What is `overdraw`? [Developer Android](https://developer.android.com/topic/performance/rendering/overdraw.html)
	- An app may draw the same pixel more than once within a single frame, an event called overdraw. Overdraw is usually unnecessary, and best eliminated. It manifests itself as a performance problem by wasting GPU time to render pixels that don't contribute to what the user sees on the screen. Overdraw refers to the system's drawing a pixel on the screen multiple times in a single frame of rendering. For example, if we have a bunch of stacked UI cards, each card hides a portion of the one below it.

#### Supporting Different Screen Sizes

* How did you support different types of resolutions?
	- No matter what hardware profile you want to support first, you need to create a layout that is responsive to even small variations in screen size.
	- For Different screen size, The following is a list of resource directories in an application that provides different layout designs for different screen sizes and different bitmap drawables for small, medium, high, and extra high density screens.


```java
	res/layout/my_layout.xml             // layout for normal screen size ("default")
	res/layout-small/my_layout.xml       // layout for small screen size
	res/layout-large/my_layout.xml       // layout for large screen size
	res/layout-xlarge/my_layout.xml      // layout for extra large screen size
	res/layout-xlarge-land/my_layout.xml // layout for extra large in landscape orientation

	res/drawable-mdpi/my_icon.png        // bitmap for medium density
	res/drawable-hdpi/my_icon.png        // bitmap for high density
	res/drawable-xhdpi/my_icon.png       // bitmap for extra high density
``` 
	- The following code in the Manifest supports all dpis.
```
	<supports-screens android:smallScreens="true" 
          android:normalScreens="true" 
          android:largeScreens="true"
          android:xlargeScreens="true"
          android:anyDensity="true" />
```
#### Permissions

* What are the different protection levels in permission?
	- Android apps must request permission to access sensitive user data (such as contacts and SMS) or certain system features (such as the camera and internet access). Each permission is identified by a unique label. For example, an app that needs to send SMS messages must have the following line in the manifest:
	
	```java
	<manifest ... >
	    <uses-permission android:name="android.permission.SEND_SMS"/>
	    ...
	</manifest>
	```

#### Native Programming

* What is the NDK and why is it useful?
	- The NDK (Native Development Kit) is a tool that allows you to program in C/C++ for Android devices. It's intended to integrate with the SDK (it's described as a "companion tool") and used only for performance-critical portions of a project. The source code is compiled directly into machine code for the CPU (and not into an intermediate language, as with Java) then developers are able to get the best performance. It is also possible to use other developers’ libraries or your own if there is something that you absolutely need to use.

* What is renderscript? [Mindorks](https://blog.mindorks.com/comparing-android-ndk-and-renderscript-1a718c01f6fe)
	- RenderScript is a framework for running computationally intensive tasks at high performance on Android. RenderScript is primarily oriented for use with data-parallel computation, although serial computationally intensive workloads can benefit as well.
	- The RenderScript runtime will parallelize work across all processors available on a device — such as multi-core CPUs and GPUs — allowing you to focus on expressing algorithms rather than scheduling work or load balancing. RenderScript is especially useful for applications performing image processing, computational photography, or computer vision.
	- To begin with RenderScript, there are two main concepts you should understand:
		- High-performance compute kernels are written in a C99-derived language.
		- A Java API is used for managing the lifetime of RenderScript resources and controlling kernel execution.
	- Advantages of NDK over RenderScript:
		- C++ code can be shared between Android and IOS, whereas RenderScript code can be used only in Android.
		- Easy integration with other C++ libraries.
		- No API limitations, while Android provides only few API for renderScript.
		- Debugging is easier.
	- Advantages of RenderScript over NDK :
		- RenderScript can use CPU, GPU, or other processing units, which leads to the huge performance benefit.
		- Android architecture independence across x86, mips, and intel, where as NDK code needs to be compiled for each different architecture.
		- Easier parallel execution.
		- Best for image processing, computational photography, 3D rendering, or computer vision. 

#### Android System Internal

* What is the Dalvik Virtual Machine?
	- Dalvik is a discontinued process virtual machine (VM) in Google's Android operating system (while its bytecode format is still used as a distribution format, but no longer at runtime in newer Android) that executes applications written for Android.

* What is the difference JVM, DVM and ART?
	- The Java virtual machine is a program whose purpose is to execute other programs. The JVM has two primary functions: to allow Java programs to run on any device or operating system (known as the "Write once, run anywhere" principle), and to manage and optimize program memory. 
	- The Dalvik Virtual Machine (DVM) is an android virtual machine optimized for mobile devices. It optimizes the virtual machine for memory, battery life and performance.
	- Android runtime (ART) is the managed runtime used by applications and some system services on Android. ART and its predecessor Dalvik were originally created specifically for the Android project. ART as the runtime executes the Dalvik Executable format and Dex bytecode specification.
	- Benefits of ART :
		- Apps run faster as DEX bytecode translation done during installation.
		- Reduces startup time of applications as native code is directly executed.
		- Improves battery performance as power utilized to interpreted byte codes line by line is saved.
		- Improved garbage collector.
		- Improved developer tool.

* What are the differences between Dalvik and ART?

* What is DEX?
	- Android programs are compiled into .dex (Dalvik Executable) files, which are in turn zipped into a single .apk file on the device. .dex files can be created by automatically translating compiled applications written in the Java programming language.

* Can you manually call the Garbage collector?
	- You can call Garbage collector using:

	```java
	System.gc();
	```
	- But this does not mean that it'll be executed immediately. The JVM decides when to execute it. In general if the JVM is about to throw an OutOfMemoryError, calling System.gc() won't prevent it. Better investigate why you're leaking so much memory and clean it up along the way.

#### Debugging and Programming Tools

* What is ADB?
	- Android Debug Bridge (adb) is a versatile command-line tool that lets you communicate with a device. You can invoke a client from a command-line terminal by issuing an adb command. A daemon (adbd), which runs commands on a device.

* What is DDMS and what can you do with it?
	- Android ships with a debugging tool called the Dalvik Debug Monitor Server (DDMS), which provides port-forwarding services, screen capture on the device, thread and heap information on the device, logcat, process, and radio state information, incoming call and SMS spoofing, location data spoofing, and more.

* What is the StrictMode? [Mindorks](https://blog.mindorks.com/use-strictmode-to-find-things-you-did-by-accident-in-android-development-4cf0e7c8d997)
	- StrictMode (android.os.StrictMode) is a developer tool which detects things you might be doing wrong by accident and brings them to your attention. Best practice in Android says “keeping the disk and network operations off from the main thread makes applications much smoother and more responsive”. So StrictMode is use to catch the coding issues such as disk I/O or network access on the application’s main thread i.e. UI thread.

* What is Lint? What is it used for?
	- The Android lint tool is a static code analysis tool that checks your Android project source files for potential bugs and optimization improvements for correctness, security, performance, usability, accessibility, and internationalization.

#### Others

* Why Bundle class is used for data passing and why cannot we use simple Map data structure
	- All the IPC communication in the Android framework is based upon the concept of Binders. And the main mechanism to allow data marshalling between those processes is based on Parcels. A Parcel is an optimised, non-general purpose serialisation mechanism that Android employs for IPC. Contrary to Serializable objects, you should never use Parcels for any kind of persistence. Whenever you see a Bundle, you’re dealing with a Parcel under the hood.

* How do you troubleshoot a crashing application? 
	- Reading a stack trace. The first step to fix a crash is to identify the place where it happens. You can use the stack trace available in the report details if you are using Play Console or the output of the logcat tool. If you don’t have a stack trace available, you should locally reproduce the crash, either by manually testing the app or by reaching out to affected users, and reproduce it while using logcat.

* Explain Android notification system?
	- A notification is a message that Android displays outside your app's UI to provide the user with reminders, communication from other people, or other timely information from your app. Users can tap the notification to open your app or take an action directly from the notification. 

* What is the difference between Serializable and Parcelable? Which is the best approach in Android?

* Have you developed widgets? Describe. [Mindorks](https://blog.mindorks.com/android-widgets-ad3d166458d3)

* What is AAPT?
	- AAPT stands for Android Asset Packaging Tool. This tool is part of the SDK (and build system) and allows you to view, create, and update Zip-compatible archives (zip, jar, apk). It can also compile resources into binary assets.

* What is the best way to update the screen periodically?

* FlatBuffers vs JSON. [Mindorks](https://blog.mindorks.com/why-consider-flatbuffer-over-json-2e4aa8d4ed07)
	- FlatBuffers are an efficient cross platform serialization library for C++, C#, C, Go, Java, JavaScript, PHP, and Python. They were originally created at Google for game development, and other performance-critical applications.
		- Access to serialized data without parsing/unpacking — What sets FlatBuffers apart is that they represent hierarchical data in a flat binary buffer, in such a way that they can still be accessed directly without parsing and unpacking, while also still supporting data structure evolution (forwards/backwards compatibility).
		- Memory efficiency and speed — The only memory needed to access your data is that of the buffer. It requires zero additional allocations (at least in C++. Other languages may vary). FlatBuffers are also suitable for use with mmap (or streaming), requiring only part of the buffer to be in memory. Access is close to the speed of raw struct access with only one extra indirection (a kind of vtable) to allow for format evolution and optional fields. FlatBuffers are aimed at projects where spending time and space (many memory allocations) to be able to access or construct serialized data is undesirable, such as in games, or any other performance sensitive applications. See the benchmarksfor details.
		- Flexible — Having optional fields mean that not only do you get great forwards and backwards compatibility (increasingly important for long-lived games: you don’t have to update all data with each new version). It also means you have a lot of choice in what data you write and what data you don’t, and how you design data structures.
		- Tiny code footprint — FlatBuffers require only small amounts of generated code, and just a single small header as the minimum dependency, which is very easy to integrate. Again, see the benchmark section for details.
		- Strongly typed — Errors happen at compile time rather than manually having to write repetitive and error prone run-time checks. Useful code can be generated for you.
		- Convenient to use — Generated C++ code allows for terse access and construction code. Then there’s the optional functionality for parsing schemas, and JSON-like text representations at runtime run efficiently if you need them (faster and more memory efficient than other JSON parsers).
		- Cross platform code with no dependencies — C++ code will work with any recent gcc/clang and VS2010. Comes with build files for the tests & samples (Android .mk files, and cmake for all other platforms).

* `HashMap`, `ArrayMap` and `SparseArray` [Mindorks](https://blog.mindorks.com/android-app-optimization-using-arraymap-and-sparsearray-f2b4e2e3dc47)
	- HashMap is basically an Array of HashMap.Entry objects. (Entry is an inner class of HashMap.). When you query the HashMap for the value for a key, it comes in O(1) time.
	- ArrayMap uses 2 arrays. The instance variables used internally are Object[ ] mArray to store the objects and the int[] mHashes to store hashCodes. When you query the ArrayMap the time complexity increases from O(1) to O(logN), but it’s memory efficient.
	- SparseArray can be used to replace HashMap when the key is a primitive type. There are some variants for different key/value types, even though not all of them are publicly available. It's more memory efficient than Hashmap.

* What are Annotations? [Mindorks](https://blog.mindorks.com/creating-custom-annotations-in-android-a855c5b43ed9), [Link](https://blog.mindorks.com/improve-your-android-coding-through-annotations-26b3273c137a)
	- An annotation is a form of syntactic metadata that can be added to Java source code. Classes, methods, variables, parameters and packages may be annotated. Like Javadoc tags, Java annotations can be read from source files. Unlike Javadoc tags, Java annotations can also be embedded in and read from class files generated by the compiler. This allows annotations to be retained by Java VM at run-time and read via reflection.
	
* How to handle multi-touch in android [GitHub](https://arjun-sna.github.io/android/2016/07/20/multi-touch-android/)
	- When multiple pointers touch the screen at the same time, the system generates the following touch events:
		- ACTION_DOWN—For the first pointer that touches the screen. This starts the gesture. The pointer data for this pointer is always at index 0 in the MotionEvent.
		- ACTION_POINTER_DOWN—For extra pointers that enter the screen beyond the first. The pointer data for this pointer is at the index returned by getActionIndex().
		- ACTION_MOVE—A change has happened during a press gesture.
		- ACTION_POINTER_UP—Sent when a non-primary pointer goes up.
		- ACTION_UP—Sent when the last pointer leaves the screen.
	- You keep track of individual pointers within a MotionEvent via each pointer's index and ID:
		- Index: A MotionEvent effectively stores information about each pointer in an array. The index of a pointer is its position within this array. Most of the MotionEvent methods you use to interact with pointers take the pointer index as a parameter, not the pointer ID.
		- ID: Each pointer also has an ID mapping that stays persistent across touch events to allow tracking an individual pointer across the entire gesture.

* How to implement XML namespaces?
	- Namespaces uniquely identify code/libraries. If I write an api that uses all the same names and such as the android api the only way to distinguish between my api and android api is to use the android namespace, or mine.
	- To define an Android namespace. the xmlns:android attribute should always be set to "http://schemas.android.com/apk/res/android" in the XML file.
	
	```java
	"xmlns:android="http://schemas.android.com/apk/res/android"
	```

* What is the support library? Why was it introduced?[MartianCraft](http://martiancraft.com/blog/2015/06/android-support-library/)
	- The Android Support Library was originally released in 2011 as the Android Compatibility Library. It provides newer APIs for older releases. It's indeed a collection of libraries that can roughly be divided into two groups: compatibility and component libraries.

* What is Android Data Binding? [Developer Android](https://developer.android.com/topic/libraries/data-binding/index.html)
	- The Data Binding Library is a support library that allows you to bind UI components in your layouts to data sources in your app using a declarative format rather than programmatically. Layouts are often defined in activities with code that calls UI framework methods. For example, the code below calls findViewById() to find a TextView widget and bind it to the userName property of the viewModel variable:

	```java
	TextView textView = findViewById(R.id.sample_text);
	textView.setText(viewModel.getUserName());
	```
	
	- The following example shows how to use the Data Binding Library to assign text to the widget directly in the layout file. This removes the need to call any of the Java code shown above. Note the use of @{} syntax in the assignment expression:

	```java
	<TextView android:text="@{viewmodel.userName}" />
	```
	
	- Binding components in the layout file lets you remove many UI framework calls in your activities, making them simpler and easier to maintain. This can also improve your app's performance and help prevent memory leaks and null pointer exceptions.

* What are Android Architecture Components? [Developer Android](https://developer.android.com/topic/libraries/architecture/index.html)
	- Android architecture components are part of Android Jetpack. They are a collection of libraries that help you design robust, testable, and maintainable apps. Start with classes for managing your UI component lifecycle and handling data persistence.
		- Manage your app's lifecycle with ease. New lifecycle-aware components help you manage your activity and fragment lifecycles. Survive configuration changes, avoid memory leaks and easily load data into your UI.
		- Use LiveData to build data objects that notify views when the underlying database changes.
		- ViewModel Stores UI-related data that isn't destroyed on app rotations.
		- Room is an a SQLite object mapping library. Use it to Avoid boilerplate code and easily convert SQLite table data to Java objects. Room provides compile time checks of SQLite statements and can return RxJava, Flowable and LiveData observables.

* How to implement search using RxJava operators? [Mindorks](https://blog.mindorks.com/implement-search-using-rxjava-operators-c8882b64fe1d)
	- First of all, you will have to make the SearchView observable. Let’s make the SearchView observable by using the PublishSubject. I am using the Android SearchView. The view can be anything like EditText. It is just that you will have to make that view observable by implementing the text change listener.

	```java
	public class RxSearchObservable {
	
	    public static Observable<String> fromView(SearchView searchView) {
	
	        final PublishSubject<String> subject = PublishSubject.create();
	
	        searchView.setOnQueryTextListener(new SearchView.OnQueryTextListener() {
	            @Override
	            public boolean onQueryTextSubmit(String s) {
	                subject.onComplete();
	                return true;
	            }
	
	            @Override
	            public boolean onQueryTextChange(String text) {
	                subject.onNext(text);
	                return true;
	            }
	        });
	
	        return subject;
	    }
	}
	```

	- Then, on that SearchView observable, you will have to apply all the operators like below:

	```java
		RxSearchObservable.fromView(searchView)
			.debounce(300, TimeUnit.MILLISECONDS)
			.filter(new Predicate<String>() {
				@Override
             public boolean test(String text) throws Exception {
             		if (text.isEmpty()) {
                 	return false;
                 } else {
                 	return true;
                 }
				}
         	})
			.distinctUntilChanged()
			.switchMap(new Function<String, ObservableSource<String>>() {
				@Override
             public ObservableSource<String> apply(String query) throws Exception {
             		return dataFromNetwork(query);
             }
          })
          .subscribeOn(Schedulers.io())
          .observeOn(AndroidSchedulers.mainThread())
          .subscribe(new Consumer<String>() {
          	@Override
             public void accept(String result) throws Exception {
             		textViewResult.setText(result);
				}
			});	
	```

	- Now, it’s time to learn why these operators are being used and how they work in combination.
		- Debounce: Here, the debounce operator is used with a time constant. The debounce operator handles the case when the user types “a”, “ab”, “abc”, in a very short time. So there will be too much network calls. But the user is finally interested in the result of the search “abc”. So, you must discard the results of “a” and “ab”. Ideally, there should be no network calls for “a” and “ab” as the user typed those in very short time. So, the debounce operator comes to the rescue. The debounce will wait for the provided time for doing anything, if any other search query comes in between that time, it will ignore the previous item and start waiting for that time again with the new search query. If nothing new comes in that given constant time, it will proceed with that search query for further processing. So, debounce only emit an item from an Observable if a particular timespan has passed without it emitting an another item.
		- Filter: The filter operator is used to filter the unwanted string like empty string in this case to avoid the unnecessary network call.
		- DistinctUntilChanged: The distinctUntilChanged operator is used to avoid the duplicate network calls. Let say the last on-going search query was “abc” and the user deleted “c” and again typed “c”. So again it’s “abc”. So if the network call is already going on with the search query “abc”, it will not make the duplicate call again with the search query “abc”. So, distinctUntilChanged suppress duplicate consecutive items emitted by the source Observable.
		- SwitchMap: Here, the switchMap operator is used to avoid the network call results which are not needed more for displaying to the user. Let say the last search query was “ab” and there is an ongoing network call for “ab” and the user typed “abc”. Then you are no more interested in the result of “ab”. You are only interested in the result of “abc”. So, the switchMap comes to the rescue. It only provides the result for the last search query(most recent) and ignores the rest.

	> Returns a new Observable by applying a function that you supply to each item emitted by the source Observable that returns an Observable, and then emitting the items emitted by the most recently emitted of these Observables.

### Architecture

* Describe the architecture of your last app.

* Describe MVP. [Mindorks](https://mindorks.com/course/android-mvp-introduction)
	- Model-View-Presenter Pattern. Here are the roles of every component:
		- Model — the data layer. Responsible for handling the business logic and communication with the network and database layers.
		- View — the UI layer. Displays the data and notifies the Presenter about user actions.
		- Presenter — retrieves the data from the Model, applies the UI logic and manages the state of the View, decides what to display and reacts to user input notifications from the View.

		![MVP_DIAGRAM](https://d33ypg4xwx0n86.cloudfront.net/direct?url=https%3A%2F%2Fcdn-images-1.medium.com%2Fmax%2F1600%2F0*VOr9hgXEmoTxyoyz.png&resize=w1408)

* What is presenter?
	- The Presenter and its corresponding View are created by the Activity. References to the View and to the TaskRepository - the Model - are given to the constructor of the Presenter. In the implementation of the constructor, the Presenter will call the setPresenter method of the View. This can be simplified when using a dependency injection framework that allows the injection of the Presenters in the corresponding views, reducing the coupling of the classes.

* What is model?
	- The Model works with the remote and local data sources to get and save the data. This is where the business logic is handled. For example, when requesting the list of Tasks, the Model would try to retrieve them from the local data source. If it is empty, it will query the network, save the response in the local data source and then return the list.

* Describe MVC.
	- Desgin pattern in which both the Controller and the View depend on the Model: the Controller to update the data, the View to get the data. But, most important for the desktop and Web devs at that time: the Model was separated and could be tested independently of the UI. Several variants of MVC appeared.

		- Model — the data layer, responsible for managing the business logic and handling network or database API.
		- View — the UI layer — a visualisation of the data from the Model.
		- Controller — the logic layer, gets notified of the user’s behavior and updates the Model as needed.

		![MVC_DIAGRAM](https://d33ypg4xwx0n86.cloudfront.net/direct?url=https%3A%2F%2Fcdn-images-1.medium.com%2Fmax%2F1600%2F0*HFP--PRKvRXsS7fd.png&resize=w1408)

* What is controller?
	- Controllers process incoming requests, handle user input and interactions, and execute appropriate application logic.

* Describe MVVM. [GitHub](https://github.com/MindorksOpenSource/android-mvvm-architecture)

	- At a first glance, MVVM seems very similar to the Model-View-Presenter pattern, because both of them do a great job in abstracting the view’s state and behavior. The Presentation Model abstracts a View independent from a specific user-interface platform, whereas the MVVM pattern was created to simplify the event driven programming of user interfaces.

	![MVVM_DIAGRAM](https://upday.github.io/images/blog/model_view_viewmodel/mvvm.png)

* Tell something about clean code [Mindorks](https://blog.mindorks.com/every-programmer-should-read-this-book-6755dedec78d)
	- Single Responsibility Principle : It states that every module or class should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class. All its services should be narrowly aligned with that responsibility.
	- Say what you mean. Mean what you say : Your function name should follow this rule.
	- Open Closed Principle : In object-oriented programming, the open/closed principle states that the software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification, that is, such an entity can allow its behaviour to be extended without modifying its source code.
	- Use Descriptive Names : Remember Ward’s principle: “You know you are working on clean code when each routine turns out to be pretty much what you expected.” Half the battle to achieving that principle is choosing good names for small functions that do one thing. The smaller and more focused a function is, the easier it is to choose a descriptive name.
	- DRY(Don’t Repeat Yourself) : The duplication is a problem because it bloats the code and will require four-fold modification when the algorithm need to be changed. It is also a four-fold opportunity for an error of omission. Duplication may be the root of all evil in software. Many principles and practices have been created for the purpose of controlling or eliminating it.
	- Writing software is like any other kind of writing : When you write a paper or an article, you get your thoughts down first, then you massage it until it reads well. The first draft might be clumsy and disorganized, so you wordsmith it and restructure it and refine it until it reads the way you want it to read.
Use Exceptions Rather Than Return Codes : The problem with Return-Code approaches is that they clutter the caller. The caller must check for errors immediately after the call. Unfortunately, it’s easy to forget. For this reason it is better to throw an exception when you encounter an error. The calling code is cleaner. Its logic is not obscured by error handling.
	- Always Provide Context with Exceptions : Each exception that you throw should provide enough context to determine the source and location of an error. In Java, you can get a stack trace from any exception; however, a stack trace can’t tell you the intent of the operation that failed. Create informative error messages and pass them along with your exceptions. Mention the operation that failed and the type of failure. If you are logging in your application, pass along enough information to be able to log the error in your catch.

### Design Problem

* Design Uber App.

* Design Facebook App.

* Design Facebook Near-By Friends App.

* Design WhatsApp.

* Design SnapChat.

* Design problems based on location based app.


### Tools And Technologies

* Git. [GitHub](https://github.com/git-tips/tips)

* RxJava. [Mindorks](https://blog.mindorks.com/a-complete-guide-to-learn-rxjava-b55c0cea3631)

* Dagger 2. [Mindorks](https://blog.mindorks.com/a-complete-guide-to-learn-dagger-2-b4c7a570d99c)

* Android Development Useful Tools. [Mindorks](https://blog.mindorks.com/android-development-useful-tools-fd73283e82e3)

* Firebase. [Firebase.google.com](https://firebase.google.com/)


### Android Test Driven Development

* What is Espresso? [Developer Android](https://developer.android.com/training/testing/ui-testing/espresso-testing.html)
	- The Espresso testing framework, provided by Android Test, provides APIs for writing UI tests to simulate user interactions within a single target app. A key benefit of using Espresso is that it provides automatic synchronization of test actions with the UI of the app you are testing. Espresso detects when the main thread is idle, so it is able to run your test commands at the appropriate time, improving the reliability of your tests. This capability also relieves you from having to add any timing workarounds, such as Thread.sleep() in your test code.

* What is Robolectric? [Robolectric](http://robolectric.org/)
	- Robolectric is a unit test framework that de-fangs the Android SDK jar so you can test-drive the development of your Android app. Robolectric handles inflation of views, resource loading, and lots of other stuff that’s implemented in native C code on Android devices. This allows tests to do most things you could do on a real device. It’s easy to provide our own implementation for specific SDK methods too, so you could simulate error conditions or real-world sensor behavior, for example.

* What is UI-Automator? [Developer Android](https://developer.android.com/training/testing/ui-testing/uiautomator-testing.html)
	- The UI Automator APIs let you interact with visible elements on a device, regardless of which Activity is in focus. Your test can look up a UI component by using convenient descriptors such as the text displayed in that component or its content description.

* Explain unit test.
	- Unit Testing is a level of software testing where individual function/method of a software are tested. The purpose is to validate that each function of the software performs as designed.

* Explain instrumented test.
	- Instrumentation tests run on a device or an emulator. In the background, your app will be installed and then a testing app will also be installed which will control your app, lunching it and running UI tests as needed.

* Have you done unit testing or automatic testing?

* Why Mockito is used? [Official site](http://site.mockito.org/)

* Describe JUnit test.
	- JUnit is an open source framework designed for the purpose of writing and running tests in the Java programming language.


### Others

* Describe how REST APIs work.
	- In a REST-based web API, data and services that act upon data are exposed as, well, simply put: resources with URLs. Those resources can be fetched with HTTP GET, created with HTTP POST, replaced with HTTP PUT, and deleted with HTTP DELETE.

* Describe SQLite.

* Describe database.

* Project Management tool - trello, basecamp, kanban, jira, asana.

* About build System - gradle, maven, ant, buck.

* About multiple apk for android application. [Mindorks](https://mindorks.com/blog/how-to-create-multiple-apk-files-for-android-application)

* Reverse Engineering an APK.

* What is proguard used for?

* What is obfuscation? What is it used for? What about minification?

* How do you build your apps for release?

* How do you control the application version update to specific number of users?

* Can we identify users who have uninstalled our application?

* Implement Search Using RxJava Operators. [Mindorks](https://blog.mindorks.com/implement-search-using-rxjava-operators-c8882b64fe1d)

* APK Size Reduction. [Mindorks](https://blog.mindorks.com/how-to-reduce-apk-size-in-android-2f3713d2d662)

* Android Development Best Practices. [Mindorks](https://blog.mindorks.com/android-development-best-practices-83c94b027fd3)

* Android Code Style And Guidelines. [Mindorks](https://blog.mindorks.com/android-code-style-and-guidelines-d5f80453d5c7)

* Have you tried Kotlin? [Medium](https://medium.com/p/why-you-must-try-kotlin-for-android-development-e14d00c8084b)

* What are the metrics that you should measure continuously while android application development? [Mindorks](https://blog.mindorks.com/android-app-performance-metrics-a1176334186e)


### Found this project useful :heart:

* Support by clicking the :star: button on the upper right of this page. :v:

[Check out Mindorks awesome open source projects here](https://mindorks.com/open-source-projects)


### License
```
   Copyright (C) 2017 MINDORKS NEXTGEN PRIVATE LIMITED

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```

### Contributing to Android Interview Questions
Just make pull request. You are in!
