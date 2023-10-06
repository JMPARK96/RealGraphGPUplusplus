# EQ1. IO improvement of RealGraph<sup>GPU++</sup>

We show the superiority of RealGraph<sup>GPU++</sup> (RG-GPU++) to RealGraphGPU (RG-GPU) in terms of IO time and IO-BW. We ran experiments on R750 with a single NVMe SSD and dual NVMe SSDs (RAID-0), which provide the maximum IO-BW of 7GB/s and 14GB/s, respectively. We performed PageRank, a graph algorithm that requires to access all graph data in every iteration, on the Yahoo dataset by using RealGraph<sup>GPU</sup> and RealGraph<sup>GPU++</sup>. Figure 6 shows the results of measuring the time required to transfer the graph data from storage to DM and the time for GPU processing in RealGraph<sup>GPU</sup> and RealGraph<sup>GPU++</sup>. The IO time of RealGraph<sup>GPU++</sup> is reduced by 40% and 63% compared to that of RealGraph<sup>GPU</sup> on a single SSD and RAID-0, respectively. This reduction is obtained because the direct storage-to-DM IO with RealGraph<sup>GPU++</sup> eliminates the extra data copies occurring in MM with RealGraph<sup>GPU</sup>. In the case of RAID-0, the time to load blocks from storage is reduced to a half because its IO-BW becomes doubled, compared to a single SSD. 

<p align="center">
<img src="https://github.com/JMPARK96/RealGraphGPUplusplus/assets/101683134/6743d418-b0ac-49ba-bf03-079b131aa589" />
</p>

Figure 7 shows the results of measuring the IO-BW when performing PageRank in RealGraph<sup>GPU</sup> and RealGraph<sup>GPU++</sup>. We see that RealGraph<sup>GPU++</sup> provides 1.5 and 3.2 times higher IO-BW than RealGraphGPU on a single SSD and RAID-0, respectively , nearly fully utilizing the IO-BW provided by storage. This is because the block processing cycles of RealGraph<sup>GPU++</sup> are pipelined, thanks to the asynchronous processing of CPU threads (mentioned in Section
3.2), producing more-frequent storage-to-DM IOs in storage. 

<p align="center">
<img src="https://github.com/JMPARK96/RealGraphGPUplusplus/assets/101683134/55bee8a8-b66e-4dd0-bc27-fbdf385d58a9" />
</p>
