Christopher K. Tarango
malloc lab
October 29, 2017

Tasks Accoplished:
1. rewrote resizeRegion function to borrrow from the following memory blocks using a coalesceNext function. This function borrows heavily from the findFirstAlloc function in how it splits memory into a used and unused sliver. If sliver is too small to hold an 8 byte memory allocation, a prefix, and a suffix it will simply coalesce the entire region. 
2. wrote a nextFitAlloc function, it is basically the firstFitAlloc function with a global variable nextReg which is a pointer to the following prefix so that its next invocation starts from that point rather than the beginning of the arena. Completes the 10000 malloc test very quickly.
3. Updated header files to accomadate added functionality
4. added tests to myAllocatorTest1 to test resizeRegion, directly uses both my rewritten reSizeRegion, and nextFitAllocator, all indications are both functions work as intended. 