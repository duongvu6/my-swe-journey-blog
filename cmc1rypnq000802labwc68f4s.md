---
title: "Operating system fundamentals"
datePublished: Wed Jun 18 2025 09:53:53 GMT+0000 (Coordinated Universal Time)
cuid: cmc1rypnq000802labwc68f4s
slug: operating-system-fundamentals
tags: operating-system, swejourneynewbie-java-multithreading1

---

1. context switch
    

* each instance of the application runs independently
    
* the act of stopping one thread and schedule thread out, schedule thread in and start another thread is context switch
    
* context switch is not cheap, and is the price of multitasking(concurrency)
    
* same as we humans when we multitask - takes time to focus
    
* each thread consumes resources in the cpu and memory
    
* when we switch to a different thread:
    
    * store data for one thread
        
    * restore data for one thread
        
* when too many threads - thrashing, spe nding more time in management than real productive work
    
* thread consume less resources than processes
    
* context switching between threads from the same process is cheaper than context switching between different processes
    

2. thread scheduling
    

* os divides the time to equally sized - epochs
    
* dynamic priority = static priority + bonus
    
* static priority is set by the developer, bonus is adjusted by the os in every epoch, for each thread
    
* using dynamic priority, the os will give preference for interactive threads(UI interface)
    
* os will give preference to threads that did not complete in the last epochs, or did not get enough time to run to prevent starvation
    

3. when to prefer multithread architecture
    

* prefer if the tasks share a lot of data
    
* threads are much faster to create and destroy
    
* switching between threads of the same process is faster (shorter context switches)
    
* security and stability are of higher importance
    
* tasks are unrelated to each other