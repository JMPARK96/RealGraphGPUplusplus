# EQ3. Comparison with single-machine-based graph engines

We compare RealGraph<sup>GPU++</sup> with 5 state-of-the-art single-machinebased graph engines: `GraphChi`[^Kyr12], `X-Stream`[^Roy13], `TurboGraph`[^Han13], `GridGraph`[^Zhu15], and `FlashGraph`[^Zhe15]. We ran all algorithms and all datasets with all graph engines on the PC, which is because the code for 5 competitors is executable only on the PC [8]. Figure 8 shows the execution times of RealGraph<sup>GPU++</sup> and existing single-machine-based graph engines, where "O.O.M" and "O.O.T" denote the results of out-of-memory and out-of-time (i.e., exceeding 24 hours). We observe that RealGraph GPU++ provides performance dramatically better than existing graph engines, by up to 114× better than TurboGraph which is the best performer among competitors. This is because RealGraph<sup>GPU++</sup> substantially improves its IO processing while maintaining the excellent workload balancing capability of RealGraph and the outstanding GPU processing capability of RealGraph<sup>GPU</sup>.

[^Kyr12]: GraphChi: Large-scale graph computation on just a pc, Aapo Kyrola et al, USENIX OSDI, 2012
[^Roy13]: X-Stream: Edge-centric graph processing using streaming partitions, Amitabha Roy et al, ACM SOSP, 2013
[^Han13]: TurboGraph: A fast parallel graph engine handling billion-scale graphs in a single PC, Wook-Shin Han et al, ACM KDD, 2013
[^Zhu15]: Gridgraph: Large-scale graph processing on a single machine using 2-level hierarchical partitioning, Xiaowei Zhu et al, USENIX ATC, 2015
[^Zhe15]: FlashGraph: Processing billion-node graphs on an array of commodity SSDs, Da Zheng et al, USENIX FAST, 2015
