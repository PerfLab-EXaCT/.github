<!-- -*-Mode: markdown;-*- -->
<!-- $Id$ -->

Performance Lab for EXtreme Computing and daTa
=============================================================================
<!-- https://github.com/PerfLab-EXaCT https://gitlab.com/PerfLab-EXaCT -->
<!-- ~/bin/admin/sync-git-profile ~/1develop -->


## [BigFlow Suite](https://gitlab.com/perflab-exact/bigflow-suite): Performance analysis and scheduling for distributed scientific workflows
<!-- BigFlow Tools -->

* [DataLife](https://github.com/pnnl/datalife):
The combination of ever-growing scientific datasets and distributed workflow complexity creates I/O performance bottlenecks due to data volume, velocity, and variety. DataLife is a measurement and analysis toolset for distributed scientific workflows comprised of tasks that interact using files and storage. DataLife performs data flow lifecycle (DFL) analysis to guide decisions regarding coordinating task and data flows on distributed resources. DataLife provides tools for measuring, analyzing, visualizing, and estimating the severity of flow bottlenecks based on I/O and storage.

<!-- * [FastFlow](https://github.com/pnnl/datalife): -->

* [DaYu](https://github.com/pnnl/DaYu):
The increasing use of descriptive data formats (e.g., HDF5, netCDF) helps organize scientific datasets, but it also creates obscure bottlenecks due to the need to translate high level operations into file addresses and then into low-level I/O operations. DaYu is a method and toolset for analyzing (a) semantic relationships between logical datasets and file addresses, (b) how dataset operations translate into I/O, and (c) the combination across entire workflows.

* [TAZeR](https://github.com/pnnl/tazer):
TAZeR (Transparent Asynchronous Zero-copy Remote I/O) is a remote I/O framework for transparently minimizing the access latencies of remote I/O in workflows.

* [BigFlowSim](https://github.com/PerfLab-EXaCT/BigFlowSim):
BigFlowSim is a workflow I/O simulator-emulator and trace generator that captures several parameters that affect local and remote I/O performance. The [BigFlowSim Driver](https://github.com/PerfLab-EXaCT/BigFlowSim-Driver) is helpful for conducting experiments.


## Application performance analysis and prediction

  * [MemGaze](https://github.com/pnnl/memgaze):
  MemGaze is a memory analysis toolset that combines high-resolution trace analysis and low overhead measurement, both with respect to time and space.

  * [Palm](https://gitlab.com/perflab-exact/palm):
  Palm is a suite of performance modeling tools (Palm, Palm-Task, Representative-Paths, Palm/FastFootprints, MIAMI-NW) to assist performance analysis and predictive model generation.

  * [QuaL²M (QuaLM)](https://github.com/pnnl/qualm):
  Quantitative Learned Latency Model
  [[Extra datasets]](https://github.com/PerfLab-EXaCT/qualm-data)



## PNNL's [CHESS](https://gitlab.com/perflab-exact/chess) ([Cloud, HPC, and Edge for Science and Security](https://www.pnnl.gov/projects/cloud-high-performance-computing-and-edge-science-and-security))

* Workflow templates

    - [AutobahnEM](https://gitlab.com/perflab-exact/chess/autobahn-em):
    CHESS's new workflow for automating experiments with scanning electron microscopes.


* Co-design tools for hybrid workflows

    - [DataLife](https://github.com/pnnl/datalife):
    The combination of ever-growing scientific datasets and distributed workflow complexity creates I/O performance bottlenecks due to data volume, velocity, and variety. DataLife is a measurement and analysis toolset for distributed scientific workflows comprised of tasks that interact using files and storage. DataLife performs data flow lifecycle (DFL) analysis to guide decisions regarding coordinating task and data flows on distributed resources. DataLife provides tools for measuring, analyzing, visualizing, and estimating the severity of flow bottlenecks based on I/O and storage.

    - [FastFlow](https://github.com/pnnl/fastflow):
    <!-- * [FastFlow](https://github.com/pnnl/datalife): -->
    When distributed scientific workflows are not intelligently executed, they can fail time constraints. To improve workflow response time, FastFlow is a new method of scheduling and resource assignment based on a monitor-analyze-optimize strategy. The key insight is to use the global perspective of interacting critical flows to guide a fast (locally greedy) scheduler that uses data flow projections to select between the better of flow parallelism and flow locality. Our method is linear time, unlike the next-best methods.

    - [DaYu](https://github.com/pnnl/DaYu):
    The increasing use of descriptive data formats (e.g., HDF5, netCDF) helps organize scientific datasets, but it also creates obscure bottlenecks due to the need to translate high level operations into file addresses and then into low-level I/O operations. DaYu is a method and toolset for analyzing (a) semantic relationships between logical datasets and file addresses, (b) how dataset operations translate into I/O, and (c) the combination across entire workflows.

    <!-- Candice's resource discovery -->

    - [Scientific workflows](https://gitlab.com/perflab-exact/workflows):
    A suite of distributed scientific workflows with a range of workload characteristics

    <!-- - [TAZeR](https://github.com/pnnl/tazer): TAZeR (Transparent Asynchronous Zero-copy Remote I/O) is a remote I/O framework for transparently minimizing the access latencies of remote I/O in workflows. -->


* Interpretation of scientific data streams

    - [SamIAm](https://github.com/PerfLab-EXaCT/SamIAm):
    Semantic segmentation for images from scanning electron microscopy. SamIAm generates precise segments that accord with domain semantics. It is based on semantic tuning of foundation models for general segmentation.

    - [SamIAm-LabelStudio](https://github.com/PerfLab-EXaCT/SamIAm-LabelStudio):
    A tool to rapidly create precise labels for image segments of identical materials.


* Distributed model training

    - [MassiveGNN](https://github.com/aishwaryyasarkar/Distributed_DGL):
    <!-- [MassiveGNN](https://github.com/pnnl/MassiveGNN) -->
    <!--  Performant and productive training for massively connected (distributed) GNNs within [Deep Graph Library](https://www.dgl.ai). These GNNs can be distributed on distributed and continuum resources. -->
    Graph Neural Networks (GNN) based on massively connected (distributed) GNNs pose significant challenges as even with the best methods, GNN training usually suffers from communication bottlenecks and load imbalance. <!-- due to non-determinism -->
    MassiveGNN introduces performant and productive training for massively connected (distributed) GNNs within the state-of-the-art [Amazon DistDGL](https://www.dgl.ai) (distributed Deep Graph Library). It brings practical trade-offs for improving the sampling and communication overheads for representation learning on distributed graphs by developing a parameterized prefetch and eviction scheme.

    - [PyChip ensemble trainer](https://gitlab.com/perflab-exact/chess/pychip-ensemble-trainer):
    Ensemble-based training for AutoEM's PyChip material classifier.

    - [PRISMScope](https://gitlab.com/perflab-exact/chess/prism-scope):
    Generates a range of (2D) image projections of a material, given a description of the material's crystalline structure and microscope parameters. Uses [Prismatic](https://prism-em.com).


* Compression for science

    - [ViSemZ](https://gitlab.com/perflab-exact/chess/visemz):
    High quality domain-aware compression for scanning electron microscopy. CompressEM leverages generative AI to preserve critical semantic features from the domain while also delivering high compression ratios and strong performance.
  <!-- https://github.com/hipdac-lab/ICS23-GPULZ/tree/microscopy -->


<!-- AI Optimized Dataset Management: Continuum VecDB: Vector databases for dynamic (execution) and long term management of data flow and storage. -->


* [CHESS Data](https://gitlab.com/perflab-exact/chess/chess-data):
  Motivating papers and example data reagrding our new methods for automating for scanning electron microscopes.


## Workload Benchmarking and Characterization

* [Scientific workflows](https://gitlab.com/perflab-exact/workflows):
A suite of distributed scientific workflows with a range of workload characteristics

* [SEAK Suite](https://github.com/pnnl/seak):
The SEAK Suite is a collection of constraining problems for common embedded computing challenges.

* [PERFECT Suite](https://github.com/pnnl/perfect):
The PERFECT Suite consists of kernels and applications for evaluating tradeoffs between performance, power, and architecture within the domains of radar and image processing.

* [miniVite-x](https://github.com/PerfLab-EXaCT/minivite-x):
Mini-application to demonstrate different memory patterns and test memory analysis tools.



## Miscellaneous tools for performance analysis and modeling

* [𝜇bench](https://github.com/PerfLab-EXaCT/ubench)

* [𝜇tools](https://github.com/PerfLab-EXaCT/utools)


## Misc work in progress

* [membench](https://github.com/PerfLab-EXaCT/membench)


<!-- 𝛍 𝜇 𝝁 -->


