# EQ4. Comparison with state-of-the-art distributed-system-based graph engines

We also compare RealGraph<sup>GPU++</sup> with four state-of-the-art distributed-system-based graph engines: `PowerGraph`[^Gon12], `GraphLab`[^Low12], `GraphX`[^Gon14], and `Giraph`[^Ave11].
We quote their results for comparison, since it is infeasible in practice to build the distributed systems identical to them. 
We ran WCC and PR with our RealGraph<sup>GPU++</sup> on R750 because the four graph engines commonly reported the performances only for those two algorithms only on the Twitter dataset. 
Table 2 presents the performance of each graph engine and its system environment where Machine indicates the number and type of machines; for each machine, #Cores, Mem.Size, and Storage indicate the number of cores, the size of memory, and the type of storage, respectively.
The hyphen (-) means that no result is available in the respective papers. RealGraph<sup>GPU++</sup> running on a single machine outperforms all of them by up to 10.6 times compared to `PowerGraph`, the best performer among them, running on 64 machines. 
This superiority of RealGraph<sup>GPU++</sup> shows well the power of the single-machine-based graph engine that does not suffer from the significant overhead for communications among distributed machines.

In summary, we conclude RealGraph<sup>GPU++</sup> achieves significantly better performance than RealGraph<sup>GPU++</sup> as well as other existing graph engines, using much smaller computing resources in a single machine.

<p align="center">
  <img src="https://github.com/JMPARK96/RealGraphGPUplusplus/assets/101683134/d1933297-37c5-46bf-b815-7de0c148d766" />
</p>

[^Gon12]: Powergraph: Distributed graph-parallel computation on natural graphs, Joseph E Gonzalez et al, USENIX OSDI 2012
[^Low12]: Distributed GraphLab: A Framework for Machine Learning and Data Mining in the Cloud, Yucheng Low et al, In VLDB Endowment, 2012
[^Gon14]: Graphx: Graph processing in a distributed dataflow framework, Joseph E Gonzalez et al, USENIX OSDI, 2014
[^Ave11]: Giraph: Large-scale graph processing infrastructure on hadoop, Ching Avery, Proceedings of the Hadoop Summit. Santa Clara, 2011
