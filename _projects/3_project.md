---
layout: page
title: Parallel Matrix Multiply HTTP Server
description: 
img: assets/img/Screenshot from 2023-09-02 17-46-08.png
importance: 3
category: 
---

In this project, I have developed a robust HTTP server designed to handle matrix multiplication requests efficiently. The key features and components of the project are as follows:

**Server**:

The server exposes an HTTP API that accepts two matrices as input.
Upon startup, the server launches a configurable number of Worker processes to perform matrix multiplication tasks concurrently.
The server uses Inter-Process Communication (IPC) mechanisms to facilitate communication between the main server and Worker processes.
Tasks are distributed among Worker processes using semaphores, ensuring efficient task management.
The server collects the results from Worker processes and returns the resultant matrix to the client.

**Mutex Locks (Mutex)**:

Mutex locks are implemented to guarantee that only one Worker process can access a specific cell of the result matrix at any given time. This ensures data consistency and prevents race conditions.

**Semaphores (Semaphore)**:

Semaphores are used to manage the distribution of work among Worker processes. Each Worker process signals its task completion, and the server waits until a Worker becomes available to maximize parallelism.

**Work Distribution**:

The server intelligently distributes the rows of the first matrix and the columns of the second matrix among Worker processes for multiplication.
Each Worker is responsible for calculating the dot product of the 10th row of the first matrix and the 10th column of the second matrix, achieving parallelism in matrix multiplication.
Dynamic Worker Allocation:

The project includes an API that allows runtime adjustment of the number of Worker processes.
The server dynamically allocates matrix multiplication tasks among the available Workers, optimizing resource utilization.
