---
title: "Introduction and motivation"
datePublished: Wed Jun 18 2025 09:08:22 GMT+0000 (Coordinated Universal Time)
cuid: cmc1qc66r000a02kv51zx9ndd
slug: introduction-and-motivation
tags: multithreading

---

1. Motivation - why do we need threads?
    
    a. Responsiveness
    

* cỉtical in applications with UI - lots of people can use it at one time
    
* Responsiveness can be achieved through multiple threads, each thread for each task
    
* generally very hard to achieve otherwise
    
* multitasking = concurrency
    
* we don’t need multiple cores to achieve concurrency
    

b. performance - parrallelism

* complete a complex task much faster
    
* finish more work in the same period of time
    
* for high scale service:
    
    * fewer machines
        
    * less money spent on hardware
        

! Multithreading caveat

* multithreaded programming is fundamentally different from single threaded programming
    

2. what threads are
    

* operating system is loaded from the hard drive, the os takes the program from the disk and create instance in a memory. That instance is a process or context of application. Each process is completely isolated from any other processes that run in the system. process contains metadata (process id, files the os reading, the code or instruction, the heap) and at least one main thread.
    
* in multithreaded application, each thread come with its own stack and its own instruction pointer.
    
* Stack is a region in memory, where local variables are stored and passed into function
    
* instruction pointer - address of the next instruction to execute