# EQ2. Comparison of RealGraph family

We compare the final performances (i.e., execution times) of different versions of RealGraph: RealGraph<sup>GPU++</sup>, RealGraph<sup>GPU</sup>, and RealGraph. We conducted experiments with all algorithms and all datasets introduced in the experimental setup on R750 with dual NVMe SSDs (RAID-0).

RealGraph GPU++ shows execution times much smaller in all cases. Specifically, RealGraph<sup>GPU++</sup> provides execution time about 56%/81% on average and up to 66%/92% smaller than RealGraph<sup>GPU</sup>/RealGraph;
this indicates that it provides about 170%/573% on average and up to 462%/1132% higher performance in speed than RealGraph<sup>GPU</sup>/RealGraph, respectively.


<p align="center">
  <img src="https://github.com/JMPARK96/RealGraphGPUplusplus/assets/101683134/a8871e1e-5401-4070-8f82-16dba8b42e5a" />
</p>
