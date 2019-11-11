# Creating a Write back Cache

1. You should take an input file specifying cache configuration (# sets, associativity, line size), and then a list of Reads/Writes and addresses. 
Values don't matter for writes. 

2. You should track all relevant info for the access, including if it is a miss or hit and requires a mem access. 
(The trick is that you can get multiple memory refs if you are evicted while line is dirty)

3. Also summary stats (hits/misses/accesses/ratios). 

4. Sample Input File looks like below

sets:256

set_size:4

line_size:4

W:160

R:15

R:430

W:430 

Here "sets, set_size, and line_size" are ordered params. Meaning the string before ":" does not matter.

5. #sets should be a power of 2. #sets will be at most 2^13.

6. Line size should also be power of 2 and at least 4 (bytes).

7. It should use an LRU eviction policy.


# Note
This project can be pretty easy if you use good object-oriented style.

# References
Please refer to the demo.png for more details on output format and call.
