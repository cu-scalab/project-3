# Creating a Write back Cache

1. You should take an input file specifying cache configuration (Number of sets, associativity, line size), and then a list of Reads/Writes and addresses. 
Values don't matter for writes. 

2. You should track all relevant info for the access, including if it is a miss or hit and requires a mem access. 

3. Also create a summary stats (hits/misses/accesses/ratios) and print it. 

4. Sample Input File looks like below

    sets:256\
    set_size:4\
    line_size:4\
    W:160\
    R:15\
    R:430\
    W:430

    Here "sets, set_size, and line_size" are ordered params. Meaning the string before ":" does not matter.

5. Number of sets should be a power of 2 - otherwise catch this as an error. 

6. Number of sets will be at most 2^13 - otherwise catch this as an error.

7. Line size should also be power of 2 and at least 4 (bytes) - otherwise catch this as an error.

8. It should use an LRU (Least Recently Used) eviction policy.


# Note
1. This project can be pretty easy if you use good object-oriented style.
2. You can work on group of 2.

# Deadline - November 30, 2019

# References
Please refer to the cache.png for more details on output format and call.
