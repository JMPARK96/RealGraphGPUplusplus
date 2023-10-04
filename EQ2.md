# EQ2. Comparison of RealGraph family

We compare the final performances (i.e., execution times) of different versions of RealGraph: RealGraph<sup>GPU++</sup>, RealGraph<sup>GPU</sup>, and RealGraph. We conducted experiments with all algorithms and all datasets introduced in the experimental setup on R750 with dual NVMe SSDs (RAID-0).

RealGraph GPU++ shows execution times much smaller in all cases. Specifically, RealGraph<sup>GPU++</sup> provides execution time about 28%/72% on average and up to 45%/86% smaller than RealGraph<sup>GPU</sup>/RealGraph;
this indicates that it provides about 44%/350% on average and up to 82%/700% higher performance in speed than RealGraph<sup>GPU</sup>/RealGraph, respectively.
