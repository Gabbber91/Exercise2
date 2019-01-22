# Mutex and Channel basics

### What is an atomic operation?
> An atomic operation is an operation were other tasks (if for instance we have multiple tasks running in parallel) are barred reading or writing to the memory until the atomic operation has completed. An atomic/indivisible operation either runs until it completes or it dont run at all. 
### What is a semaphore?
> A semaphore can be as simple as a variable that is used to limit the number of tasks that can access a certain resource at one time. It can for example be implemented as increment/decrement variable and be used as to keep count on how many units of the resource is availeble for use at all times.  

### What is a mutex?
> Sometimes in multi threaded programs, more than one thread might want access to the same resource. A mutex (mutual exclusive) is used to ensure that only one thread can access the resource at the time. When a thread signals the OS that it wants the resource it will either be given it right away if there is no enabled mutex, or if some other thread is using the resource, it has to wait until this thread is done and the mutex is released before it is given access.  

### What is the difference between a mutex and a binary semaphore?
> A mutex functions as a lock. When a thread acquires the mutex, it has "ownership" over the resource that the mutex is locking. Only when the current thread (that is using the resource and has ownership of the mutex) releases the mutex, another thread can get ownership and access to the resource. In contrast a binary semaphore does not protect the resource in the same way the mutex does. A binary semaphore is more of a signal that tells other threads that the resource they are waiting for is available 

### What is a critical section?
> A critical sections is a part of the program that accesses a shared variable, protected by a mutex.

### What is the difference between race conditions and data races?
 > A data race happens when for example two threads try to access the same memory location at the same time, and both of them are not read operations. A race condition is a flaw that occurs in the timing or sequences of events that affects the programs correctnes, leading to faulty behaviour. 

### List some advantages of using message passing over lock-based synchronization primitives.
> *Your answer here*

### List some advantages of using lock-based synchronization primitives over message passing.
> *Your answer here*
