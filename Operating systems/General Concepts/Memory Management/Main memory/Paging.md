# Paging 
[[Main memory]]
### Basic method
   
Basic Paging method:

-   Break phisical memory into fixed-sized blocks called FRAMES
-   Break logical memory into blocks of the same size as FRAMES called PAGES
-   When process is executed, the PAGES of the PROCESS are loaded into ANY AVAILABLE FRAMES from their source (filesystem or the backing store)
-   The backing store is divided into fixed-sized blocks that are the same size as the memory frames of clusters of multiple frames.
-   Thanks to that LOGICAL ADDRESS SPACE is totally separate from PHYSICAL ADDRESS SPACE.

### Protection 
### Shared pages

[[Page Table]]