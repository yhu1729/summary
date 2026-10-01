# 2026OFL

## ChatGPT (July 2026)

### Summary

This paper adapts B-trees to embedded devices with single-threaded processors, roughly $4$--$64\,\mathrm{KB}$ of RAM, and flash storage that may lack a file system or flash translation layer. Its VMTree uses a small memory-resident table of virtual page redirects so updated nodes can be written sequentially without propagating physical-address changes from leaf to root. VMTree-OW instead exploits NOR or DataFlash page-overwrite constraints with an append-within-page layout, eliminating the mapping table. Both designs include free-space management and recovery, and can combine a small operation log with batched insertion. Experiments on 16-bit PIC and 32-bit ARM boards compare NAND, DataFlash, and SD cards using random, environmental, and wearable-sensor data. VMTree runs efficiently on raw NAND using about $3$--$4\,\mathrm{KB}$ of memory; overwrite-aware pages deliver roughly $4\times$ speedup on DataFlash. One-page write buffers improve clustered sensor insertion by $3$--$5\times$ overall and by up to $9\times$ in a reported platform/data combination. Results also show when conventional B-trees remain preferable and how scarce RAM should be divided between path caching and write buffering.

### Contributions

1. Introduced bounded virtual page mappings that suppress B-tree write amplification on raw flash without a full translation layer.
2. Developed VMTree for sequential writes to raw NAND and VMTree-OW for overwrite-capable flash pages.
3. Supplied low-memory free-space management and recovery mechanisms for embedded deployments.
4. Evaluated storage-specific variants on two microcontroller platforms, three storage types, and multiple data distributions.
5. Quantified how page buffers and operation write buffers should share scarce RAM for read and insertion performance.
