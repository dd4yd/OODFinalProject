# Multithreading

## Java
1. Threads or thread-like abilities
  * Threads are created as new, not running, Threads
  * The threads are started and become runnable
  * They run through full execution
  * Threads can be forced to wait to complete
  * Threads die at the end of execution
2. How is multitasking accomplished?
  * Threads can be created by implementing Runnable
  * Threads can also be created by extending Thread and overriding the run method
  * In both circumstances, the thread is started by calling the start method of the threads

## Swift
1. Threads or thread-like abilities
  * NSThread objects are first initialized
  * NSThreads are then started
  * They are then in the executing started
  * They can be cancelled or paused
  * After complete execution they are finished
2. How is multitasking accomplished?
  * NSThreads are created using the init function
  * They are started using the start function
  * Functions like isExecuting, isFinished, and is Cancelled can be used to determine the state of the Thread
