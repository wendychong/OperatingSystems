# OperatingSystems

Program: mergesort468.c

Consider a mergesort program merge468.c that’s included with this homework.  The numbers to be sorted are N integers in an array “a[ ]”, and for simplicity it’s assumed that N is a power of 2.

Rewrite merge468.c so that the merging is done with threads using pthreads.  For example if there are N = 16 elements in the array a[ ] then the program will operate as follows:

1.	Create 8 threads where each thread merges two elements into a subarray of size 2, where these 8 threads could be run in parallel
2.	Wait until all the threads are done.
3.	Create 4 threads where each thread merges two subarrays of size 2 into a subarray of size 4, where these 4 threads could be run in parallel
4.	Wait until all the threads are done
5.	Create 2 threads where each thread merges two subarrays of size 4 into a subarray of size 8, where these 2 threads can be run in parallel
6.	Wait until all the threads are done
7.	Create 1 thread which merges two subarrays of size 8 into an array of size 16

