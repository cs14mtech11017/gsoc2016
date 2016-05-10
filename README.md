#Polly as an Analysis Pass in LLVM - GSoC 2016

Abstract:  
The Polyhedral framework provides an exact dependence analysis, which is more powerful than conventional dependence testing algorithms [5, 6]. Currently, LLVM mainline lacks a powerful dependence analysis framework, and at the same time, Polly’s (a high level data locality optimizer based on polyhedral framework) dependence analysis is suitable for many transformation passes in LLVM like Loop Vectorization, Loop Versioning, Modulo Scheduling, Loop Nest Optimizations, etc. I propose to provide an API for Polly such that its precise dependence analysis can be used as an Analysis pass within LLVM's transformation passes.  

References:  
[1] https://docs.google.com/document/d/1QyUzL3OOwJSI91lDqr7VsvqUsFyTY9FlpAwbGSipUtw/edit  
[2] https://groups.google.com/forum/#!topic/llvm-dev/_3IabeSMFxE  
[3] https://groups.google.com/forum/#!topic/polly-dev/DuRxNmKfEnM
