   

# Fragmenatnion

First fit AND Best fit suffer EXTERNAL FRAGMENTATION. As processes are loaded and removed from memory, the free memory space is broken into little pieces. No matter which algorithm is used, external fragmentation will occur and will be a problem.

Memory is divided into FIXED SIZE blocks to avoid holes of 2bytes or so. Because of that, memory allocated might be larger that memory of the process. The difference between allocated memory and the memory required by a process is called INTERNAL FRAGMENTATION

-   Internal fragmentation - Difference between allocated memory and the memory required by a process.
-   External fragmentation - exists when there is enough total memory space to satisfy a request but the available spaces are not contigouous. Memory is fragmented into a large number of small holes. According to 50%, even one-third of memory can be WASTED.
-   50% rule says that for each N blocks alocated, 0.5 N blocks are lost due to fragmentation.

Solutions to EXTERNAL Fragmentations:

-   Compaction - shuffle the memory contents so all free memory is in one block. It is NOT ALWAYS POSSIBLE. It is not possible if address binding happens in load time and compile time. This is only possible when relocation happens in run-time.The strategy is to move all processes to towards the end of memory (top or bot) so the available memory takes contigous space.
-    Permiting the logical address space to be noncontiguous so the process would be allocated in physical memory wherever such memory is available. This is called PAGING - the most common memory-management technique for computer systems.