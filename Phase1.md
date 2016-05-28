#Phase 1


1: Decouple ScopInfo object from pass and create two passes. One region pass to preserve compatibility with existing Polly transformation passes, other will be a function pass to be used by PolyhedralInfo pass as mentioned below.

2: Decouple DependenceInfo object from pass and create two passes. Same as above.

3: Create the interface PolyhedralInfo, which will extract Memory Access wise dependence information from Polly and provide few simple interfaces like isParallel(), isVectorizable(), tripCount(Loop&)


#First Week- 23 May 2016 to 30 May 2016

1. Completed decoupling ScopInfo for the pass logic.
2. All Unit test passed.
3. Sent a patch to polly-dev mailing list.
4. Johannes asked to run lnt with polly. Also asked few changes.
5. Created a review in reviews.llvm.org after making necessary changes. D#
6. Lnt is failing on my local server.
a. With -polly-process-unprofitable
FAIL: MultiSource/Applications/sqlite3/sqlite3.compile_time (1 of 1992)
FAIL: MultiSource/Benchmarks/ASCI_Purple/SMG2000/smg2000.compile_time (2 of 1992)
FAIL: MultiSource/Benchmarks/tramp3d-v4/tramp3d-v4.compile_time (3 of 1992)

b. With -polly-process-unprofitable -polly-position=before-vectorizer
FAIL: MultiSource/Applications/sqlite3/sqlite3.compile_time (1 of 1992)
FAIL: MultiSource/Benchmarks/7zip/7zip-benchmark.compile_time (2 of 1992)
FAIL: MultiSource/Benchmarks/tramp3d-v4/tramp3d-v4.compile_time (3 of 1992)
FAIL: MultiSource/Applications/sqlite3/sqlite3.execution_time (499 of 1992)
FAIL: MultiSource/Benchmarks/tramp3d-v4/tramp3d-v4.execution_time (500 of 1992)
