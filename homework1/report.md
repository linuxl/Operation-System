---
title: "homework 1"
output: "homework_1"
---

# Operating System homework 1

-------

## platform

| CPU information | memory size | kernel version | machine type |
| :-----: | :----: | :----: | :----: |
| Intel(R) Core(TM) i7-5500U CPU @ 2.40GHz<br>Core: 2<br>Logic processor: 4   | 12G | 4.15.0-29-generic |physical machine |

## The measurement result

I generate random arrays of integers of different lengths. The execution times of the query elements measured under single process and single thread conditions were used as a control group to measure the execution times under different process and thread conditions. 
使用 taskset -c 0,1,2,3 绑定到所有CPU上执行

The parameters are listed in the table below.
|   information   |            |
----------        | -------------
|Array length     |256, 262144, 2097152, 4194304 |
Number of processes | 2, 4,  8
Number of threads |   2, 4, 8

The following list shows the execution times for different array sizes

* **Array length: 256**
   Single process execution time: 0.003 (ms). the element number is: 1
  * multi-process and multi-threads execution time table list:

    Number of processes/threads | Used times (ms)<br> (process) | Used times (ms)<br> (thread with mutex) | Used times (ms)<br> (thread without mutex) |
    :---:|:---:| :---: | :---: |
    2  | 0.726 |0.271 |  0.467
    4  | 0.91 |0.23 | 0.178
    8  | 1.517 |0.421 | 0.575
  

* **Array length: 262144**
    Single process execution time: 0.773 (ms) the element number is: 10753.
  * multi-process and multi-threads execution time table list:

    Number of processes/threads | Used times (ms)<br> (process) | Used times (ms)<br> (thread with mutex) | Used times (ms)<br> (thread without mutex) |
    :---:|:---:| :---: | :---: |
    2  | 0.829 | 0.615 | 0.479
    4  | 1.766 | 0.491 | 0.31
    8  | 0.924 | 0.495 | 0.40

* **Array length: 2097152**
  Single process execution time: 6.291 (ms) the element number is: 10753.
  * multi-process and multi-threads execution time table list:

    Number of processes/threads | Used times (ms)<br> (process) | Used times (ms)<br> (thread with mutex) | Used times (ms)<br> (thread without mutex) |
    :---:|:---:| :---: | :---: |
    2  | 5.327 | 4.591 | 3.323
    4  | 5.498 | 4.333 | 4.022
    8  | 4.551 | 4.013 | 2.413

* **Array length: 4194304**
  Single process execution time: 12.48 (ms) the element number is: 20941.
  * multi-process and multi-threads execution time table list:

    Number of processes/threads | Used times (ms)<br> (process) | Used times (ms)<br> (thread with mutex) | Used times (ms)<br> (thread without mutex) |
    :---:|:---:| :---: | :---: |
    2  | 9.214 | 8.75 | 8.26
    4  | 5.961 | 7.162 | 4.263
    8  | 8.746 | 7.472 | 5.249




## 结论：


