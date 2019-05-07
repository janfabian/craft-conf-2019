# Introduction
William Kennedy (Ardan Labs)

Cost of engineering decisions, 

mechanical sympathy

goroutine 
    - states
        - running
        - runnable
        - waiting
    - small stack size (2kb)
    - tasks
        - execute main
            - reserve memory 
        - data transformation
            - if you don't understand the data, you don't understand the problem
    

- pointer semantic
    - mutation the world object outside scope
    - cost: side effects
- value semantic
    - every function copy the values and works in isolated state
    - cost: inefficient 

- escape analysis 
    - call a function
        - takes a stack
        - after the call clean it
    - if function returns pointer, compiler includes the value of the pointer on the heap

Garbage collector
    - non-generational
    - mark-and-sweep
    - concurrent

    - steps
        1. stop the world
            - when go routines 
        2. mark
        3. take 25% of all available cpus
        4. there is a delta between marking and marking done phase
        5. 

Slice

Methods
    - data driven development
    - methods 
    - value receiver function assignment caused copying the value
        `f1 := d.func`, then `d` is copied

Interfaces
    - valueless
    - work only with values which fulfill the interface description
    - once pointer semantic the interface 

Embedding
    - is not an inheritance

QUESTIONS
- slices why length and capacity, instead of just single length attr

TO READ
https://blog.golang.org/ismmkeynote
https://www.ardanlabs.com/blog/2014/05/methods-interfaces-and-embedded-types.html
https://learning.oreilly.com/videos/ultimate-go-programming/9780135261651

TO REMEMBER
- when working with built-in types, then minimize heap allocation
- decoupling (interfaces, methods etc.) to minimize needed changes when problem(=data structure) changes
- pointer receiver can't be mixed with value receiver, value receiver on the other side can be in some cases mixed with pointer receiver