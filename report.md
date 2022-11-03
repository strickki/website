##### Bitonic Sort Pseudocode
- measure performance of a sequential sort
  - Increasing input sizes & constant input sizes

- measure performance of MPI sort:
  - Increase the number of processors & keep problem size constant
  - Increase problem size & increase number of processors 

- measure performance of CUDA sort:
  - Increase number of threads with a constant problem size
  - Increase number of threads with increasing problem size 

###### Bitonic Sort Pseudocode
**Step1:**
- Create bitonic sequence from input
  - Bitonic sequence: a sequence that starts increasing then becomes strictly decreasing 

**Step2:**
- Now have a bitonically sorted input where the first half of the input is in increasing order while the second half is in decreasing order

**Step3:**
- Loop through and:
  - Compare first element of the first half of the bitonic sequence with the first element of the second half of the bitonic sequence
   - If element(firstHalf.at(i)) < element(secondHalf.at(i)) ⇒ swap(firstHalf.at(i), secondHalf.at(i))
**Step 4:**
- We will now have two bitonic sequences of size n/2 where all the elements in the first half are smaller than the elements in the second half
  - Repeat steps 3 and 4 until you have n bitonic sequences of size 1
**Step 5:**
- Return Sorted Sequence
