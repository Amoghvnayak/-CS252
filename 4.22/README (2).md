
# Question 4.22 - Chapter 4 Threads & Concurrency

## Statement

<p>Write a multithreaded program that outputs prime numbers. This program
should work as follows: The user will run the program and will
enter a number on the command line. The program will then create a
separate thread that outputs all the prime numbers less than or equal to
the number entered by the user.

## Source Code

[4.22](https://github.com/Amoghvnayak/-CS252/blob/main/4.22(new).c)

### Instructions

-   Download/Clone the Github repo.

```sh
git clone https://github.com/Amoghvnayak/-CS252.git
```

```sh
cd -CS252/4.23/
```

-   Compile the program

```sh
gcc 4.22.c -lpthread
```

-   Run the compiled program and enter the data

```sh
./a.out {data...}
```


The following thread fuctions and declarations were used:

1. ` pthread_t {thread name }`

    - Used to declare a thread.
    - store the thread ID of the new thread.
    - example : `pthread_t t1;`

2. `int pthread_create(pthread_t *thread, pthread_attr_t *attr, void *(*start_routine) (void *arg), void *arg);`

    - thread: location where the thread ID is stored
    - attr: structure that specifies the attributes of the new thread.
    - start_routine: routine where the thread begins.
    - arg : arguments to pass to start_routine.
    - example : `pthread_create(&t1,NULL,&avg,NULL);`

3. `int pthread_join(pthread_t thread, void **status);`

    - Used to wait for the termination of a thread
    - example : `pthread_join(t1,NULL);`
    ## Credits

-   [(https://stackoverflow.com/questions/26090901/find-prime-numbers-in-a-separate-thread)]