This a library to use all data stuctures and sorting algorithms

Data structures supported are

1. Stack
2. Queue
3. LinkedList
4. Binary Search Tree
5. Graph
6. Tries
7. Heap

It also supports sorting algorithms like

1. Bubble Sort
2. Selection Sort
3. Insertation Sort
4. Quick Sort
5. Merge Sort
6. Heap Sort

To use this library 

var $d = require('ds.algo');

To get LinkedList object
var ll =  $d(':ll'); or $d.linkedlist();

To get Stack object
var st =  $d(':st'); or $d.stack();

To get Queue object
var qu =  $d(':qu'); or $d.queue();


To get BinarySearchTree object
var bst =  $d(':bst'); or $d.binarySearchTree();

To get Graph object
var graph =  $d(':grp'); or $d.graph();

To get Sorter object
var sorter =  $d(':sorter'); or $d.sorter();

 * sorter.selectionSort(array, comparator);
 * sorter.bubbleSort(array, comparator);
 * sorter.insertationSort(array, comparator);
 * sorter.quickSort(array, comparator);
 * sorter.mergeSort(array, comparator);
 * sorter.heapSort(array, comparator);
 
 **Lets the Explaination**

1 **Linked List**

        To use the linked listlist two option are avaiable
        var lList = $d.linkedlist()
                 OR
        var lList = $d(':ll');
        
         **Supported API's**
        
        /* To add a value at last of LinkedList. */
        lList.addToLast(val);
        
        /* Add a value at start of linkedlist. */
        lList.addAtFirst(val);
        
        /* return an object having next() API. */
        var it = lList.iterator();
        var nextVal = it.next();
        
        /* returns the size of linked list. */
        lList.size();

      
       
2 **Stack**
    
    
            /* comparator is function used for comparison of item.
             its an optional parameter. */
            var stk = $d.stack(comparator);
             or
            var stk = $d(':st', comparator)';
            
             **Supported API's**
             
            /* Push an item to stack. */
            stk.push(item);
            
            /* Removes and return the top item */
            stk.pop();
            
            /* returns the top item without removal */
            stk.peek();
            
            /* Returns the size of stack */
            stk.size();


3 **Queue** 
     
        /* comparator is function used for comparison of item.
           its an optional parameter. */
         var que = $d.queue(comparator);
               or
         var que = $d(':qe', comparator);       

          **Supported API's**
         
         /* Adds the value to the rear of the queue. */
         que.enqueue(val);
         
         /* Removes and return the value from the front of the queue. */
         que.dequeue();
         
         /* Returns an item from the front of the queue without removing it. */
         que.peek();
         
         /* Returns true of the item is part of queue otherwise false.*/
         que.contains(item);
         
         /* Returns the length of the queue. */
         que.size();
         
         
4  **Binary Search Tree**
    
        /* comparator is function used for comparison of item.
           its an optional parameter. */
         var bst = $d.binarySearchTree(comparator);
               or
         var bst = $d(':bst', comparator);       
        
        **Supported API's**
        
         /* Adds a new value to Binary Search Tree. It will be placed in BST based on comparator or comparison. */
         bst.add(val);
         
         /* Removes a node from the binary Search tree. */
         bst.delete();
         
         /* Do inorder traversal of BST and return the array after traversal. */
         bst.inorder();
         
     
5 **Graph**

         /* Comparator is function used for comparison of item.
           its an optional parameter. Two ways to create the graph */
           
         var grp = $d.graph(comparator);
               or
         var grp = $d(':grp', comparator);     

          /* ** Supported API's **  */

          /* Create and return a vertex with passed value. Once vertex is created add to the graph. */
          var vertex = grp.createVertex(val);
          grp.addVertex(vertex);

          /* Create and return a Edge with passed value. Once Edge is created add to the graph.*/
          var edge = grp.createEdge(vert1, vert2);
          grp.addEdge(edge);

          /* Once Vertexes and Edges are created and added to the graph, this API will create the graph.*/
          grp.buildGraph();

          /* This will traverse the graph in breath first order and prints the vertex values/  */
          grp.breathFirstTraversal();

         /* This will traverse the graph in depth first order and prints the vertex values/  */
          grp.depthFirstTraversal();
        

6 **Sorting Algorithms**
  
        /* comparator is function used for comparison of item.
           its an optional parameter. Two ways to create the Sorter. */
           
        var sorter = $d.sorter(comparator);
           or
        var sorter = $d(':sorter', comparator);     
        
        /* Sort using Bubble Sort algorithm and returns the sorted array. */
        ver sortedArray = sorter.bubbleSort(array);
        
        /* Sort using Selection Sort algorithm and returns the sorted array. */
        ver sortedArray = sorter.selectionSort(array);
        
        
        /* Sort using Insertion Sort algorithm and returns the sorted array. */
        ver sortedArray = sorter.insertionSort(array);
        
        /* Sort using Quick Sort algorithm and returns the sorted array.*/
        ver sortedArray = sorter.quickSort(array);
        
        /* Sort using Merge Sort algorithm and returns the sorted array. */
        ver sortedArray = sorter.mergeSort(array);
        
        /* Sort using Heap Sort algorithm and returns the sorted array. */
        ver sortedArray = sorter.heapSort(array);
    
7 **Heap**
        
        /* Comparator is function used for comparison of item.
           its an optional parameter. */
         var heap = $d.heap(comparator);
               or
         var heap = $d(':heap', comparator);     
         
         /* This will build the heap based on passed array values. */
         heap.build(array);
         
        /* This will return and delete the min value. */
         heap.deleteMin();
         
8 **Trie**
   
        
        /* Comparator is function used for comparison of item.
           its an optional parameter. */
         var trie = $d.tries(comparator);
               or
         var trie = $d(':tri', comparator);   
         
        /* Use this API to pass on array of data to be stored in the Trie and then build it.*/
         trie.addData(data)
         
         /* Return true if the passed text is available in Trie otherwise false. */
         trie.find(text);
         
