<!-- -*-Mode: markdown;-*- -->
<!-- $Id$ -->

Performance Lab for Extreme Computing and Data
=============================================================================
<!-- https://github.com/PerfLab-EXaCT https://gitlab.com/PerfLab-EXaCT -->


## BigFlow Suite: Performance analysis and scheduling for distributed scientific workflows
<!-- BigFlow Tools -->

* [DataLife](https://github.com/pnnl/datalife): DataLife is a measurement and analysis toolset for distributed scientific workflows that use I/O and storage for task composition.

* [TAZeR](https://github.com/pnnl/tazer): TAZeR (Transparent Asynchronous Zero-copy Remote I/O) is a remote I/O framework for transparently minimizing the access latencies of remote I/O in workflows.

* [BigFlowSim](https://gitlab.pnnl.gov/perf-lab/tazer/tazer-bigflow-sim): BigFlowSim is a workflow I/O simulator-emulator and trace generator that captures several parameters that affect local and remote I/O performance.


## Application performance analysis and prediction

  * [MemGaze](https://github.com/pnnl/memgaze): MemGaze is a memory analysis toolset that combines high-resolution trace analysis and low overhead measurement, both with respect to time and space.

  * [Palm](https://gitlab.pnnl.gov/perf-lab/palm/): Palm is a suite of performance modeling tools (Palm, Palm-Task, Representative-Paths, Palm/FastFootprints, MIAMI-NW) to assist performance analysis and predictive model generation.

  * [QuaL²M (QuaLM)](https://github.com/pnnl/qualm): Quantitative Learned Latency Model
  [[Extra datasets]](https://github.com/PerfLab-EXaCT/qualm-data)



## PNNL's [CHESS](https://gitlab.com/perflab-exact/chess) (Cloud, HPC, and Edge for Science and Security)

* [CHESS Data](https://gitlab.com/perflab-exact/chess/chess-data):
  Motivating papers and example data reagrding our new methods for automating for scanning electron microscopes.

* [AutobahnEM](https://gitlab.com/perflab-exact/chess/autobahn-em):
  CHESS's new workflow for automating experiments with scanning electron microscopes.

* [SamIAm](https://github.com/PerfLab-EXaCT/SamIAm):
  Semantic segmentation for images from scanning electron microscopy. SamIAm generates precise segments that accord with domain semantics. It is based on semantic tuning of foundation models for general segmentation.

* [SamIAm-LabelStudio](https://github.com/PerfLab-EXaCT/SamIAm-LabelStudio):
  A tool to rapidly create precise labels for image segments of identical materials.

* [CompressEM](https://gitlab.com/perflab-exact/chess/compress-em) ([In-progress](https://github.com/hipdac-lab/ICS23-GPULZ/tree/microscopy)):
  High quality domain-aware compression for scanning electron microscopy. CompressEM leverages generative AI to preserve critical semantic features from the domain while also delivering high compression ratios and strong performance.

* [PRISMScope](https://gitlab.com/perflab-exact/chess/prism-scope):
  Generates a range of (2D) image projections of a material, given a description of the material's crystalline structure and microscope parameters. Uses [Prismatic](https://prism-em.com).

* [PyChip ensemble trainer](https://gitlab.com/perflab-exact/chess/pychip-ensemble-trainer):
  Ensemble-based training for AutoEM's PyChip material classifier.

* [Massive GNN](https://github.com/aishwaryyasarkar/Distributed_DGL):
  Performant and productive training for massive GNNs within [Deep Graph Library](https://www.dgl.ai). These GNNs must be distributed on distributed and continuum resources.

<!-- Continuum VecDB: Vector databases for dynamic (execution) and long term management of data flow and storage. -->


* [Scientific workflows](https://gitlab.com/perflab-exact/workflows)
  ([In migration](https://gitlab.pnnl.gov/perf-lab/workflows)): A suite of distributed scientific workflows with a range of workload characteristics


## Workload Benchmarking and Characterization

* [Scientific workflows](https://gitlab.com/perflab-exact/workflows)
  ([In migration](https://gitlab.pnnl.gov/perf-lab/workflows)): A suite of distributed scientific workflows with a range of workload characteristics

* [SEAK Suite](https://github.com/pnnl/seak): The SEAK Suite is a collection of constraining problems for common embedded computing challenges.

* [PERFECT Suite](https://github.com/pnnl/perfect): The PERFECT Suite consists of kernels and applications for evaluating tradeoffs between performance, power, and architecture within the domains of radar and image processing.

* [miniVite-x](https://github.com/PerfLab-EXaCT/minivite-x): Mini-application to demonstrate different memory patterns and test memory analysis tools.



## Miscellaneous tools for performance analysis and modeling

* [𝜇bench](https://github.com/PerfLab-EXaCT/ubench)

* [𝜇tools](https://github.com/PerfLab-EXaCT/utools)


## Misc work in progress

* [membench](https://github.com/PerfLab-EXaCT/membench)


<!-- 𝛍 𝜇 𝝁 -->


