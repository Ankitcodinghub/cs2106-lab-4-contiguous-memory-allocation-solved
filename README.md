# cs2106-lab-4-contiguous-memory-allocation-solved
**TO GET THIS SOLUTION VISIT:** [CS2106 Lab 4-Contiguous Memory Allocation Solved](https://www.ankitcodinghub.com/product/cs2106-introduction-to-operating-systems-solved-4/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;121440&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS2106 Lab 4-Contiguous Memory Allocation Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Lab 4

Contiguous Memory Allocation

1. Introduction

In this lab we will look at implementing our own version of malloc and free, called “mymalloc” and “myfree”, so that you can explore some of the issues in creating memory allocation algorithms.

There are three parts to this lab:

(1) Bitmap Allocation

In the first part you will implement a bitmap-based memory first-fit allocation algorithm. You will need to implement your own algorithms to scan a bitmap to allocate a suitable stretch of memory.

(2) Linked List Allocation

In the second part you will implement linked-list based first-fit, best-fit and worst-fit memory allocation algorithms. A set of linked-list routines have been provided to you, and you need to implement the allocation algorithms themselves.

(3) Your Telephone Book

Recall that in Lab 1 you created a small telephone book program using binary trees. In this lab you will now adapt your telephone book program to use mymalloc and myfree, your versions of malloc and free.

2. Submissions

3. Bitmap Memory Allocation

In this first section you will be allocating a first-fit memory allocation algorithm using bitmaps. Your bitmap will be stored in an array of unsigned char. Every bit in the bitmap represents one byte of memory to be allocated/freed.

Switch to the “bitmap” directory. You will see the following files:

Filename Purpose

bitmap.h, bitmap.c Header and source code files where you will implement the routines to manage the bitmap.

mymalloc.c, mymalloc.h Header and source code files where you will implement your own versions of malloc and free, called mymalloc and myfree.

testmap.c Test file to check that your bitmap routines work.

testmalloc.c Test file to check that your mymalloc and myfree work.

harness.c Demo file.

Let’s now get right into what you need to do:

3.1 Implement the Bitmap Algorithms

The bitmap.c file contains the following functions. Aside from print_map, allocate_map and free_map, you need to implement the rest of the functions.

Function Name Parameters Description

print_map map: The bitmap declared as an array of unsigned char. Each char is 8 bits, each bit represents 1 byte of memory to be allocated/freed.

len: Length of the array in characters. Implemented for you.

Prints out the bitmap

search_map map: The bitmap

len: Length of the bitmap in characters

num_zeroes: Minimum # of consecutive zeroes we need to find

Returns: Index pointing to start of first series zeroes that is at least “numzeroes” long, or -1 if none found. Searches for a stretch of 0’s that is at least “num_zeroes” long.

Returns the index to the start of the stretch or -1 if none are found. The first bit in the bitmap has index 0, second bit has index 1, etc.

Function Name Parameters Description

set_map map: The bitmap

start: Starting index of first bit to set or clear. length: # of bits to set or clear. value: Non-zero value will set the stretch of bits to 1, and a 0 value will clear the stretch of bits to 0. Sets or clears a stretch of bits starting from index to index + length – 1.

allocate_map map: The bitmap

start: The index of the first bit to set.

length: The number of bits to set. Implemented for you.

Bits index to index + length – 1 will be set to 1.

free_map map: The bitmap

start: The index of the first bit to clear.

length: The number of bits to clear. Implemented for you.

Bits index to index + length – 1 will be set to 0.

Implement search_map and set_map as specified in the descriptions column in the bitmap.c file.

3.2 Testing your Bitmap Routines

To test whether your bitmap routines are written correctly, compile and run using:

gcc testmap.c bitmap.c -o testmap

./testmap

If it is implemented correctly, you will see:

If your implementation is incorrect, testmap will crash:

3.3 Implementing your Memory Manager

If your bitmap routines from 3.2 are working correctly, you can now implement your memory manager!

Question 3.1 (1 mark)

Given a memory size of 64 bytes, how large would your bitmap be in bytes if we allocate in units of 1 byte?

Open the mymalloc.c file and you will see the following routines:

Function Name Parameters Description

get_index ptr: Pointer to a memory region returned by mymalloc. Implemented for you.

Returns an index corresponding to the memory region created by mymalloc.

Used by the test harness but you can also use it in your code if you find it useful.

print_memlist None Call print_map to print the current memory map.

mymalloc size: Number of bytes to allocate Returns a pointer to the allocated memory, or NULL if no suitable memory is found.

Function Name Parameters Description

myfree ptr: Pointer to block of memory to free Frees memory pointed to by ptr. Fails silently if ptr is NULL or does not point

to a memory region created by mymalloc.

(Note: This is different from free which crashes under such

circumstances)

There are also some constants in mymalloc.h that you need to know about:

Constant Description

MEMSIZE Size of memory in bytes. Set at 64 bytes.

You should allocate memory from the heap, simulated in mymalloc.c using an array of char:

char heap[MEMSIZE] = {0};

Question 3.2 (1 mark)

The allocated memory is held in an array for type char. Would it make a difference if the array is of type unsigned char instead? Why or why not?

Implement print_memlist, mymalloc and myfree using the routines in bitmap.c. See Section 4 also on a linked list library (llist.c and llist.h in the linkedlist directory) that you might find useful. You can copy over these files to the bitmap directory to use them.

Question 3.3 (1 mark)

Does your myfree routine need to know how many bytes of memory need to be freed? If so, where will you get this information since you only call “myfree” with a pointer to the memory to be freed with no length information?

3.4 Testing Your Memory Allocation Routines

To test your memory allocation routines, compile and run using:

gcc testmalloc.c mymalloc.c bitmap.c -o testmalloc

./testmalloc

Note: If you use the linked list library from Section 4, compile with:

gcc testmalloc.c mymalloc.c bitmap.c llist.c -o testmalloc

If your mymalloc and myfree are working properly, you should see:

You can also compare with the bitmap.out file provided in the bitmap directory.

Compile your memory manager with harness.c using:

gcc harness.c bitmap.c mymalloc.c -o harness

If you are using the linked list from section 4:

gcc harness.c bitmap.c mymalloc.c llist.c -o harness

./harness

If you’ve done everything correctly the harness will run without crashing.

4. Linked List Memory Allocation

We will now create first-fit, best-fit and worst-fit memory allocation algorithms using linked lists. Open the linkedlist directory and you will see:

Common Files Description

llist.c, llist.h Linked list library

mymalloc.c, mymalloc.h Where you will implement 3 versions of your memory allocation algorithm.

testlist.c Example of how to use llist.c.

testmalloc.c Test mymalloc

You will also see three directories:

Directories Description

bf Contains harness file harness-bf.c for best fit. Implement your best fit algorithm here.

ff Contains harness file harness-ff.c for first fit. Implement your first fit algorithm here.

wf Contains harness file harness-wf.c for worst fit. Implement your worst fit algorithm here.

You can copy llist.*, mymalloc.* and testmalloc.c files to each of these directories to build each version of the allocation algorithm.

4.1 The Linked List Library

The linked list library is available in llist.c and llist.h. All routines have been implemented for you. The basic linked list structure TNode is defined as:

It consists of a key that is used sort the nodes into ascending or descending order, a pointer of type TData (see below) to point to a data node, a prev and next pointer to point to the previous and next nodes, and two pointers trav and tail that are used only by the “succ” and “pred” iterator functions, and to allow reverse traversal of the list.

There is a TData structure that you can use to define the type of data you want to put into the node. It is currently defined as:

You should modify TData to hold the data that you need to manage your memory. Note that you CAN choose to modify TNode directly to put in the data you want to store in the node, instead of using TData.

The following library calls are available in llist.c. Note again that ALL of these have already been implemented for you. See testlist.c for how to use each function.

Function Name Parameters Description

dbprintf Same parameters as printf A debug version of printf that prints to the screen only if the DEBUG macro in llist.h is defined.

make_node key: The key value for sorting the list.

data: Pointer to the data to add to the node. NULL if you are not using this. Creates a new linked list node.

insert_node llist: Pointer to the linked list

node: The node to be inserted created using make_node. dir: Sort direction. ASCENDING or DESCENDING Inserts a new node created by make_node into the linked list in the specified sort order.

delete_node llist: Pointer to the linked list node: The node to delete Deletes node from the linked list.

find_node llist: The linked list key: Value to search for Searches the linked list for key and returns the node holding key. Returns NULL if key is not found.

merge_node llist: The linked list

node: The node to merge dir: PRECEDING or SUCCEEDING

(previous or next) Between the provided node and the PRECEDING or

SUCCEEDING node, the node with the larger key is deleted.

purge_list llist: Pointer to the linked list. Purges the linked list and sets it to NULL.

process_list llist: Linked list

func: Function to call for each node of the linked list. Traverse the linked list and call func for each node.

Function Name Parameters Description

reset_traverser llist: The linked list

where: FRONT or REAR Resets the traverser to the front or rear of the linked list.

succ llist: The linked list Returns the current node and advances the traverser to the next node.

pred llist: The linked list Returns the current node and moves the traverser to the previous node.

You can test the linked list library compiling and running testlist:

gcc llist.c testlist.c -o testlist

./testlist

Hit return to see the numbers inserted in ascending order, do a series of deletes, and purge the list. Hit return again to repeat with the numbers in descending order.

4.2 Implementing the First Fit Allocation Algorithm

As before, mymalloc.c and mymalloc.h consist of get_index, print_memlist, mymalloc, and myfree, of which you need to implement print_memlist, mymalloc and myfree. The mymalloc.h file also contains the MEMSIZE constant which is set to create a heap of 64KB. Just as with the bitmap implementation, mymalloc.c contains a character array called _heap. You will allocate your memory from this array.

Using the linked list library llist.c and llist.h, implement the first-fit allocation algorithm in mymalloc, and the corresponding free in myfree.

Question 4.1 (1 mark)

What additional data did you add to TData (or TNode) to implement your first-fit manager? List down the data you added in the form of &lt;datatype&gt; &lt;fieldname&gt;.

E.g.

int start_addr;

char status;

…

Question 4.2 (1 mark)

Given a total heap size of 64KB, what is the best case and worst case storage requirement for your linked list in bytes, inclusive of all the fields in TNode and TData, if we allocate memory in units of 1 byte?

You can verify your implementation by doing:

gcc mymalloc.c llist.c testmalloc.c -o testmalloc

./testmalloc

If all goes well you will see an output like this:

You can see the full output that you should get in ff.out in the ff directory. If your implementation is correct you will get an identical output.

There is a test harness program called harness-ff.c. Compile the harness using:

gcc harness.c mymalloc.c llist.c -o harness

We will keep this for the demo.

4.3 Implementing the Best Fit Allocation Algorithm

Now switch to the bf directory and implement the best-fit allocation algorithm. You can modify the first-fit algorithm from Section 4.2 or code from a fresh copy of mymalloc.c.

As before you can copy over llist.c and llist.h either from the copy you used for the first-fit algorithm, or start from a fresh copy of llist.c and llist.h. However you should copy over testmalloc.c.

There is also a test harness called harness-bf.c that you should not modify.

Compile testmalloc using:

gcc testmalloc.c llist.c mymalloc.c -o testmalloc

./testmalloc

You can check your output against bf.out.

As before, compile the test harness using:

gcc harness-bf.c mymalloc.c llist.c -o harness-bf

We will keep this aside for the demo.

4.4 Implementing the Worst Fit Allocation Algorithm

Now switch to the wf directory and implement the worst-fit allocation algorithm. You can modify the first-fit or best-fit algorithms from Section 4.2 and 4.3 or code from a fresh copy of mymalloc.c.

As before you can copy over llist.c and llist.h either from the copy you used for the first-fit algorithm, or start from a fresh copy of llist.c and llist.h. However you should copy over testmalloc.c.

There is also a test harness called harness-wf.c that you should not modify.

Compile testmalloc using:

gcc testmalloc.c llist.c mymalloc.c -o testmalloc

./testmalloc

You can check your output against wf.out.

As before, compile the test harness using:

gcc harness-wf.c mymalloc.c llist.c -o harness-wf

Question 4.3 (1 mark)

What are the worst case and best case space requirements to store a bitmap, in bytes, for 64KB of heap space, if we allocate memory in units of 1 byte?

Question 4.4 (1 mark)

Compare your answer in Question 4.3 with Question 4.2, and comment on the relative advantages/disadvantages of bitmaps versus linked-lists for managing memory allocation, in terms of storage requirements and execution time requirements.

The best-fit and worst-fit can be transformed from O(n) algorithms to O(1) algorithms. How, and what disadvantage would you have if you did this?

5. Back to the (Telephone) Books!

In Lab 1 to learn how to use malloc and free you created a binary search tree based telephone book. Today you will use what you did then, but this time you will use your own mymalloc/myfree implementation.

Decide between yourself and your partner whose version of the telephone book you would like to use, and decide whether you’d like to use the first-fit, best-fit or worstfit algorithms.

Modify your program by replacing all malloc and free with calls to mymalloc and myfree.

Compile and run your program using:

gcc llist.c mymalloc.c bintree.c phonebook.c testpb.c -o testpb

./testpb

If everything goes well you should see an output like this:

~ END OF FILE ~
