# BloomFilter

## TERMINOLOGY

### Probabilistic Data Structure
A NO is a NO, but a yes might not be a yes.
Probabilistic data structures are a group of data structures that are extremely useful
for big data and streaming applications. These data structures use hash functions to
randomize and compactly represent a set of items
### Cardinality
The term "cardinality" is used to mean the number of distinct elements in a data
stream with repeated elements. However, in the theory of multisets the term refers
to the sum of multiplicities of each member of a multiset. 

## INTRODUCTION

### BLOOM FILTER:

Bloom Filter is a probabilistic data structure which is used to search an element within
a large set of elements in constant time that is O(K) where K is the number of hash
functions being used in Bloom Filter. This is useful in cases where:

- [x] The data to be searched is large

- [x] The memory available on the system is limited/ low

- [x] Bloom Filter is memory efficient than a Hash Map with the same performance. Theonly thing to note is that this is a probabilistic data structure so for a small number of cases, it may give wrong results (which can be limited).


### HYPER LOGLOG:
- [x] Hyper Loglog is an algorithm for the count-distinct problem, approximating the number of distinct elements in a multiset. Calculating the exact cardinality of a multiset requires an amount of memory proportional to the cardinality, which is impractical for very large data sets.
- [x] The basis of the Hyper Loglog algorithm is the observation that the cardinality of a multiset of uniformly distributed random numbers can be estimated by calculating the maximum number of leading zeros in the binary representation of each number in the set. If the maximum number of leading zeros observed is n, an estimate for the number of distinct elements in the set is 2n
