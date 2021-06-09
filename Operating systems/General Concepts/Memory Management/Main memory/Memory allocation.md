   

# Memory allocation

One of the simplest methods to allocate memory is to assign processes to variably sized partitions in memory where each partition may contain exacly one process. This is called variable-partition scheme. OS keeps a table indicating which parts of memory are available and which are occupied.

-   Memory allocation strategies

-   Best fit - Allocate to the smallest hole that is big enough. Produces the smallest leftover. Must search whole list or the memory must be sorted
-   First fit - Allocate process to the first hole in memory which meets expectations
-   Worst fit - Allocate the largest hole. Search entile list or sort it. Produses the largest leftover which may be more useful than the smallest leftover.

Tests show that that both first fit and best fit are better than worst fit in terms of decreasing time and storage utilization. It is not clear if best fit or first fit is better in terms of storage utilization but first fit is FASTER.