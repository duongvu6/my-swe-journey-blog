---
title: "Threading Fundamentals"
datePublished: Wed Jun 18 2025 12:25:12 GMT+0000 (Coordinated Universal Time)
cuid: cmc1xdaru00290ajt0ba0hlct
slug: threading-fundamentals
tags: java-thread, swejourneynewbie-java-multithreading1

---

# Thread Creation

## First way to create thread - using Runable interface

```java
package org.example.thread_creation;

public class Main1 {
    public static void main(String[] args) throws InterruptedException {
        Thread thread = new Thread(new Runnable() {
            @Override
            public void run() {
                System.out.println("We are now in thread " + Thread.currentThread().getName());
                System.out.println("Current thread priority is " + Thread.currentThread().getPriority());
                throw new RuntimeException("Intentional Exception");
            }
        });
        thread.setName("New Worker Thread");
        thread.setPriority(Thread.MAX_PRIORITY);
        System.out.println("We are in thread: " + Thread.currentThread().getName() + " before starting a new thread");
        thread.setUncaughtExceptionHandler(new Thread.UncaughtExceptionHandler() {
            @Override
            public void uncaughtException(Thread t, Throwable e) {
                System.out.println("A critical error happened in thread " + t.getName() + ", the error is " + e.getMessage());
            }
        });
        thread.start();
        System.out.println("We are in thread: " + Thread.currentThread().getName() + " after starting a new thread");

        Thread.sleep(10000);

    }
}
```

## Second way to create thread using Thread Class

```java
package org.example.thread_creation.thread_inheritance;

public class Main {
    public static void main(String[] args) {
        Thread thread = new NewThread();
        thread.start();
    }
    public static class NewThread extends Thread{
        @Override
        public void run() {
            System.out.println("Hello from " + this.getName());
        }
    }
}
```

### Case study exercises

```java
package org.example.thread_creation.thread_inheritance;

import java.util.ArrayList;
import java.util.List;
import java.util.Random;

public class CaseStudy {
    public static final int MAX_PASSWORD = 9999;

    public static void main(String[] args) {
        Random random = new Random();

        Vault vault = new Vault(random.nextInt(MAX_PASSWORD));

        List<Thread> threads = new ArrayList<>();

        threads.add(new AscendingHackerThread(vault));
        threads.add(new DescendingHackerThread(vault));
        threads.add(new PoliceThread());

        for (Thread thread : threads) {
            thread.start();
        }
    }

    private static class Vault {
        private int password;

        public Vault(int password) {
            this.password = password;
        }

        public boolean isCorrectPassword(int guess) {
            try {
                Thread.sleep(5);
            } catch (InterruptedException e) {
            }
            return this.password == guess;
        }
    }

    private static abstract class HackerThread extends Thread {
        protected Vault vault;

        public HackerThread(Vault vault) {
            this.vault = vault;
            this.setName(this.getClass().getSimpleName());
            this.setPriority(Thread.MAX_PRIORITY);
        }

        @Override
        public void start() {
            System.out.println("Starting thread " + this.getName());
            super.start();
        }
    }

    private static class AscendingHackerThread extends HackerThread {

        public AscendingHackerThread(Vault vault) {
            super(vault);
        }

        @Override
        public void run() {
            for (int guess = 0; guess < MAX_PASSWORD; guess++) {
                if (vault.isCorrectPassword(guess)) {
                    System.out.println(this.getName() + " guessed the password " + guess);
                    System.exit(0);
                }
            }
        }
    }

    private static class DescendingHackerThread extends HackerThread {

        public DescendingHackerThread(Vault vault) {
            super(vault);
        }

        @Override
        public void run() {
            for (int guess = MAX_PASSWORD; guess >= 0; guess--) {
                if (vault.isCorrectPassword(guess)) {
                    System.out.println(this.getName() + " guessed the password " + guess);
                    System.exit(0);
                }
            }
        }
    }

    private static class PoliceThread extends Thread {
        @Override
        public void run() {
            for (int i = 10; i > 0; i--) {
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                }
                System.out.println(i);
            }

            System.out.println("Game over for you hackers");
            System.exit(0);
        }
    }
}
```

# Coding assignment: **Thread Creation - MultiExecutor**
## Instructions
In this exercise, we are going to implement a  MultiExecutor .

The client of this class will create a list of Runnable tasks and provide that list into MultiExecutor's constructor.

When the client runs the  executeAll(),  the MultiExecutor,  will execute all the given tasks.

To take full advantage of our multicore CPU, we would like the MultiExecutor to execute all the tasks in parallel by passing each task to a different thread.



Please implement the MultiExecutor below

### Test(s)
#### Test 1
```java
import org.junit.Test;
import org.junit.Assert;
import com.udemy.ucp.*;
import java.util.List;
import java.util.Arrays;

public class Evaluate {
IOHelper helper = new IOHelper();

    @Test
    public void testExercise() throws InterruptedException{
        helper.resetStdOut(); // clean stdout
        
        String string1 = "Cutting carrots";
        String string2 = "Cooking eggs";
        String string3 = "Washing dishes";
        
        Runnable task1 = () -> System.out.println(string1);
        Runnable task2 = () -> System.out.println(string2);
        Runnable task3 = () -> System.out.println(string3);
        
        List tasks = Arrays.asList(task1, task2, task3);
        
        MultiExecutor multiExecutor = new MultiExecutor(tasks);
        
        multiExecutor.executeAll();
        
        Thread.sleep(1000);
        
        String output = helper.getOutput();
        
        Assert.assertTrue("The task "+ string1 +" is not executed", output.contains(string1));
        Assert.assertTrue("The task "+ string2 +" is not executed", output.contains(string2));
        Assert.assertTrue("The task "+ string3 +" is not executed", output.contains(string3));
    }
}
```
## Solution

```java
import java.util.ArrayList;
import java.util.List;

public class MultiExecutor {
    
    private final List tasks;

    /*
     * @param tasks to executed concurrently
     */
    public MultiExecutor(List tasks) {
        this.tasks = tasks;
    }

    /**
     * Starts and executes all the tasks concurrently
     */
    public void executeAll() {
        List threads = new ArrayList<>(tasks.size());
        
        for (Runnable task : tasks) {
            Thread thread = new Thread(task);
            threads.add(thread);
        }
        
        for(Thread thread : threads) {
            thread.start();
        }
    }
}
```