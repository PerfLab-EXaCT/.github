<!-- -*-Mode: markdown;-*- -->
<!-- $Id$ -->

Performance Lab for EXtreme Computing and daTa
=============================================================================
<!-- https://github.com/PerfLab-EXaCT https://gitlab.com/PerfLab-EXaCT -->
<!-- ~/bin/admin/sync-git-profile ~/1develop/PerfLab-EXaCT.github -->

<!-- 𝛍 𝜇 𝝁 -->

<a name="repos-workflows"></a>
## [DataFlowDrs](https://github.com/PerfLab-EXaCT/DataFlowDrs): Performance optimization of HPC workflows

<!-- https://gitlab.com/perflab-exact/bigflow-suite -->

* [DataFlowDrs](https://github.com/PerfLab-EXaCT/DataFlowDrs):
  Scientific workflows  are critical in many areas of scientific exploration. Because these workflows tend to be data intensive, severe bottlenecks emerge in storage systems and I/O networks. We introduce DataFlowDrs, a new comprehensive suite of tools for performance optimization of HPC workflows that especially focuses on data flow and storage. DataFlowDrs introduces (a) lightweight high-resolution measurement and visualization tools for workflow profiling and tracing; (b) rapid modeling and analysis that reduces analysis data by compressing common repeated coordination patterns; (c) novel methods for predicting data flow scaling using automatically generated interpretable models of data flow; (d) effective performance analysis and bottleneck detection that can automatically quantify and rank bottlenecks for different combinations of task parallelism and storage resources; (e) actionable performance optimization in the form of new schedules and resource assignments. DataFlowDrs automates several previously difficult manual analyses and substantially reduces the impact of data flow bottlenecks by recommending the right tradeoffs between task parallelism and storage performance.

  - [DataLife](https://github.com/pnnl/datalife):
    The combination of ever-growing scientific datasets and distributed workflow complexity creates I/O performance bottlenecks due to data volume, velocity, and variety. DataLife is a measurement and analysis toolset for distributed scientific workflows comprised of tasks that interact using files and storage. DataLife performs data flow lifecycle (DFL) analysis to guide decisions regarding coordinating task and data flows on distributed resources. DataLife provides tools for measuring, analyzing, visualizing, and estimating the severity of flow bottlenecks based on I/O and storage.

  - [DaYu](https://github.com/pnnl/DaYu):
    The increasing use of descriptive data formats (e.g., HDF5, netCDF) helps organize scientific datasets, but it also creates obscure bottlenecks due to the need to translate high level operations into file addresses and then into low-level I/O operations. DaYu is a method and toolset for analyzing (a) semantic relationships between logical datasets and file addresses, (b) how dataset operations translate into I/O, and (c) the combination across entire workflows. DaYu's analysis and visualization enables identification of critical bottlenecks and reasoning about remediation. With DaYu, one can extract workflow data patterns, develop insights into the behavior of data flows, and identify opportunities for both users and I/O libraries to optimize the applications.

  - [FlowForecaster](https://github.com/pnnl/FlowForecaster): 
    FlowForecaster is a tool for automatically inferring detailed and interpretable workflow scaling models from only a few (3--5) empirical task property graphs. A model represents workflow control and data flow as an abstract DAG with analytical expressions to describe how the DAG scales and how data flows along edges. Thus, with a model and proposed workflow input, FlowForecaster predicts the workflow's tasks, control, and data flow properties. 

  - FastFlow: <!-- [FastFlow]() https://github.com/pnnl/FastFlow https://github.com/PerfLab-EXaCT/FastFlow/ -->
    When distributed scientific workflows are not intelligently executed, they can fail time constraints. To improve workflow response time, FastFlow is a new method of scheduling that prioritizes critical flow paths and their interactions. The key insight is to use the global perspective of interacting critical flows to guide a fast (locally greedy) scheduler that uses data flow projections to select between the better of flow parallelism and flow locality. The result is a rapid, linear-time scheduling method that achieves high quality results and excels on data-intensive workflows.

  <!-- Candice's SPM / resource discovery -->

* [TAZeR](https://github.com/pnnl/tazer):
  TAZeR (Transparent Asynchronous Zero-copy Remote I/O) is a remote I/O framework for transparently minimizing the access latencies of remote I/O in workflows. TAZeR captures dynamic and irregular inter-task locality, both temporal and spatial, via adaptive hierarchical staging that ensures most frequently accessed data is `close'.

* [BigFlowSim](https://github.com/PerfLab-EXaCT/BigFlowSim):
  BigFlowSim is a workflow I/O simulator-emulator and trace generator that captures several parameters that affect local and remote I/O performance. BigFlowSim generates a large variety of flows within and between tasks of distributed workflows. The [BigFlowSim Driver](https://github.com/PerfLab-EXaCT/BigFlowSim-Driver) is helpful for conducting experiments.


<a name="repos-aisys"></a>
## AI Systems • Data Analytics

<!-- PowerTrip, LLMTailer -->
<!-- Scientific compression: BMQ, ViSemZ -->

* [MassiveGNN](https://github.com/pnnl/MassiveGNN): <!-- [(development)](https://github.com/aishwaryyasarkar/Distributed_DGL) -->
  Graph Neural Networks (GNN) based on massively connected (distributed) GNNs pose significant challenges as even with the best methods, GNN training usually suffers from communication bottlenecks and load imbalance. <!-- due to non-determinism -->
  MassiveGNN introduces performant and productive training for massively connected (distributed) GNNs within the state-of-the-art [Amazon DistDGL](https://www.dgl.ai) (distributed Deep Graph Library). It brings practical trade-offs for improving the sampling and communication overheads for representation learning on distributed graphs by developing a parameterized continuous prefetch and eviction scheme.
  <!--  Performant and productive training for massively connected (distributed) GNNs within [Deep Graph Library](https://www.dgl.ai). These GNNs can be distributed on distributed and continuum resources. -->

* [SamIAm](https://github.com/pnnl/SAMIAm): <!-- https://github.com/PerfLab-EXaCT/SamIAm -->
    [(Demo)](https://colab.research.google.com/github/PerfLab-EXaCT/SamIAm-LabelStudio/blob/main/SamIAm_Demo.ipynb)
    Image segmentation is a critical enabler for tasks ranging from medical diagnostics to autonomous driving. However, the correct segmentation semantics -- where are boundaries located? what segments are logically similar? -- change depending on the domain, such that state-of-the-art foundation models can generate meaningless and incorrect results. Moreover, in certain domains, fine-tuning and retraining techniques are infeasible: obtaining labels is costly and time-consuming; domain images (micrographs) can be exponentially diverse; and data sharing  (for third-party retraining) is restricted. To enable rapid adaptation of the best segmentation technology, we define _semantic boosting_: given a zero-shot foundation model, _guide_ its segmentation and adjust results to match domain expectations. We apply semantic boosting to the Segment Anything Model (SAM) to obtain _microstructure segmentation_ for transmission electron microscopy. Our booster, SAM-I-Am, extracts geometric and textural features of various intermediate masks to perform mask removal and mask merging operations.

* [SuperSAM](https://github.com/pnnl/SuperSAM):
  Neural Architecture Search (NAS) is a powerful approach of automating the design of efficient neural architectures. In contrast to traditional NAS methods, recently proposed one-shot NAS methods prove to be more efficient in performing NAS. One-shot NAS works by generating a singular weight-sharing supernetwork that acts as a search space (container) of subnetworks. Despite its achievements, designing the one-shot search space remains a major challenge. In this work we propose a search space design strategy for Vision Transformer (ViT)-based architectures. In particular, we convert the Segment Anything Model (SAM) into a weight-sharing supernetwork called SuperSAM. Our approach involves automating the search space design via layer-wise structured pruning and parameter prioritization. While the structured pruning applies probabilistic removal of certain transformer layers, parameter prioritization performs weight reordering and slicing of MLP-blocks in the remaining layers. We train supernetworks on several datasets using the sandwich rule. For deployment, we enhance subnetwork discovery by utilizing a program autotuner to identify efficient subnetworks within the search space. The resulting subnetworks are 30-70% smaller in size compared to the original pre-trained SAM ViT-B, yet outperform the pretrained model. Our work introduces a new and effective method for ViT NAS search-space design.

<!-- * [ViSemZ](https://gitlab.com/perflab-exact/chess/visemz): -->


<a name="repos-perftool"></a>
## Hardware/Software Co-design • Application Performance Analysis

* [MemGaze/MemFriend](https://github.com/pnnl/memgaze):
   MemGaze is a memory analysis toolset that combines high-resolution trace analysis and low overhead measurement, both with respect to time and space. MemGaze provides high-resolution by collecting world-level memory access traces, where the highest resolution supported is back-to-back sequences. MemGaze provides several post-mortem trace processing methods, including multi-resolution analysis for locations vs. operations; accesses vs. spatio-temporal reuse, and reuse (distance, rate, volume) vs. access patterns.
    
   Memgaze now includes *MemFriend*, a new analysis module that introduces spatial and temporal locality analysis that captures affinity (access correlation) between pairs of memory locations. MemFriend's multi-resolution analysis identifies significant memory segments and simultaneously prunes the analysis space such that time and space complexity is modest. MemFriend creates signatures, selectable at 3D, 2D, and 1D resolutions, that provide novel insights and enable predictive reasoning about application performance. The results aid data layout optimizations, and data placement decisions.

* [Palm](https://gitlab.com/perflab-exact/palm):
  Palm is a suite of performance modeling tools (Palm, Palm-Task, Representative-Paths, Palm/FastFootprints, MIAMI-NW) to assist performance analysis and predictive model generation. Palm generates models by combining top-down (human-provided) semantic insight with bottom-up static and dynamic analysis. Palm has been used to model irregular applications with sparse data structures and unpredictable access patterns. Recent additions focus on rapid characterization of memory behavior.

* [QuaL²M (QuaLM)](https://github.com/pnnl/qualm):
  Quantitative Learned Latency Model
  [[Extra datasets]](https://github.com/PerfLab-EXaCT/qualm-data)


<a name="repos-bench"></a>
## Workload Benchmarking and Characterization

* [Scientific workflows](https://gitlab.com/perflab-exact/workflows):
  A suite of distributed scientific workflows with a range of workload characteristics

* [SEAK Suite](https://github.com/pnnl/seak):
  The SEAK Suite is a collection of constraining problems for common embedded computing challenges. A _constraining problem_ is a mission-centric and goal-oriented problem specification that separate problem-domain constraints from solution implementations so as to encourage creative solutions that meet goals but that may deviate from standard implementations.

* [PERFECT Suite](https://github.com/pnnl/perfect):
  The PERFECT Suite consists of kernels and applications for evaluating tradeoffs between performance, power, and architecture within the domains of radar and image processing.

* [miniVite-x](https://github.com/PerfLab-EXaCT/minivite-x):
  Mini-application to demonstrate different memory patterns and test memory analysis tools.


## Miscellaneous tools for performance analysis and modeling

* [𝜇bench](https://github.com/PerfLab-EXaCT/ubench)

* [𝜇tools](https://github.com/PerfLab-EXaCT/utools)

* [membench](https://github.com/PerfLab-EXaCT/membench)


## PNNL's [CHESS](https://gitlab.com/perflab-exact/chess) ([Cloud, HPC, and Edge for Science and Security](https://www.pnnl.gov/projects/cloud-high-performance-computing-and-edge-science-and-security))

