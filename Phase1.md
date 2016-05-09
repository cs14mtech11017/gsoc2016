#Phase 1


1: Decouple ScopInfo object from pass and create two passes. One region pass to preserve compatibility with existing Polly transformation passes, other will be a function pass to be used by PolyhedralInfo pass as mentioned below.

2: Decouple DependenceInfo object from pass and create two passes. Same as above.

3: Create the interface PolyhedralInfo, which will extract Memory Access wise dependence information from Polly and provide few simple interfaces like isParallel(), isVectorizable(), tripCount(Loop&)
