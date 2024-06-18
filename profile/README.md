<!-- -*-Mode: markdown;-*- -->
<!-- $Id$ -->

Performance Lab for EXtreme Computing and daTa
=============================================================================
<!-- https://github.com/PerfLab-EXaCT https://gitlab.com/PerfLab-EXaCT -->
<!-- ~/bin/admin/sync-git-profile ~/1develop -->


## [BigFlow Suite](https://gitlab.com/perflab-exact/bigflow-suite): Performance analysis and scheduling for distributed scientific workflows
<!-- BigFlow Tools -->

* [DataLife](https://github.com/pnnl/datalife): DataLife is a measurement and analysis toolset for distributed scientific workflows that use I/O and storage for task composition.

<!-- * [FastFlow](https://github.com/pnnl/datalife): -->

<!-- * [DaYu](https://github.com/pnnl/datalife): -->

<!-- * [MassiveGNN](https://github.com/pnnl/datalife): -->


* [TAZeR](https://github.com/pnnl/tazer): TAZeR (Transparent Asynchronous Zero-copy Remote I/O) is a remote I/O framework for transparently minimizing the access latencies of remote I/O in workflows.

* [BigFlowSim](https://github.com/PerfLab-EXaCT/BigFlowSim): BigFlowSim is a workflow I/O simulator-emulator and trace generator that captures several parameters that affect local and remote I/O performance. The [BigFlowSim Driver](https://github.com/PerfLab-EXaCT/BigFlowSim-Driver) is helpful for conducting experiments.


## Application performance analysis and prediction

  * [MemGaze](https://github.com/pnnl/memgaze): MemGaze is a memory analysis toolset that combines high-resolution trace analysis and low overhead measurement, both with respect to time and space.

  * [Palm](https://gitlab.com/perflab-exact/palm): Palm is a suite of performance modeling tools (Palm, Palm-Task, Representative-Paths, Palm/FastFootprints, MIAMI-NW) to assist performance analysis and predictive model generation.

  * [QuaL²M (QuaLM)](https://github.com/pnnl/qualm): Quantitative Learned Latency Model
  [[Extra datasets]](https://github.com/PerfLab-EXaCT/qualm-data)



## PNNL's [CHESS](https://gitlab.com/perflab-exact/chess) ([Cloud, HPC, and Edge for Science and Security](https://www.pnnl.gov/projects/cloud-high-performance-computing-and-edge-science-and-security))

* Workflow templates

    - [AutobahnEM](https://gitlab.com/perflab-exact/chess/autobahn-em): CHESS's new workflow for automating experiments with scanning electron microscopes.


* Co-design tools for hybrid workflows

    - [DataLife](https://github.com/pnnl/datalife): DataLife is a measurement and analysis toolset for distributed scientific workflows that use I/O and storage for task composition.

    - [FastFlow](https://github.com/pnnl/fastflow):

    - [DaYu](https://github.com/pnnl/dayu): 

    <!-- Candice's resource discovery -->

    - [Scientific workflows](https://gitlab.com/perflab-exact/workflows): A suite of distributed scientific workflows with a range of workload characteristics

    <!-- - [TAZeR](https://github.com/pnnl/tazer): TAZeR (Transparent Asynchronous Zero-copy Remote I/O) is a remote I/O framework for transparently minimizing the access latencies of remote I/O in workflows. -->


* Interpretation of scientific data streams

    - [SamIAm](https://github.com/PerfLab-EXaCT/SamIAm): Semantic segmentation for images from scanning electron microscopy. SamIAm generates precise segments that accord with domain semantics. It is based on semantic tuning of foundation models for general segmentation.

    - [SamIAm-LabelStudio](https://github.com/PerfLab-EXaCT/SamIAm-LabelStudio): A tool to rapidly create precise labels for image segments of identical materials.


* Distributed model training

    - [MassiveGNN](https://github.com/aishwaryyasarkar/Distributed_DGL): Performant and productive training for massively connected (distributed) GNNs within [Deep Graph Library](https://www.dgl.ai).
  <!-- These GNNs can be distributed on distributed and continuum resources. -->

    - [PyChip ensemble trainer](https://gitlab.com/perflab-exact/chess/pychip-ensemble-trainer): Ensemble-based training for AutoEM's PyChip material classifier.

    - [PRISMScope](https://gitlab.com/perflab-exact/chess/prism-scope): Generates a range of (2D) image projections of a material, given a description of the material's crystalline structure and microscope parameters. Uses [Prismatic](https://prism-em.com).


* Compression for science

    - [ViSemZ](https://gitlab.com/perflab-exact/chess/visemz) High quality domain-aware compression for scanning electron microscopy. CompressEM leverages generative AI to preserve critical semantic features from the domain while also delivering high compression ratios and strong performance.
  <!-- https://github.com/hipdac-lab/ICS23-GPULZ/tree/microscopy -->


<!-- AI Optimized Dataset Management: Continuum VecDB: Vector databases for dynamic (execution) and long term management of data flow and storage. -->


* [CHESS Data](https://gitlab.com/perflab-exact/chess/chess-data):
  Motivating papers and example data reagrding our new methods for automating for scanning electron microscopes.


## Workload Benchmarking and Characterization

* [Scientific workflows](https://gitlab.com/perflab-exact/workflows): A suite of distributed scientific workflows with a range of workload characteristics

* [SEAK Suite](https://github.com/pnnl/seak): The SEAK Suite is a collection of constraining problems for common embedded computing challenges.

* [PERFECT Suite](https://github.com/pnnl/perfect): The PERFECT Suite consists of kernels and applications for evaluating tradeoffs between performance, power, and architecture within the domains of radar and image processing.

* [miniVite-x](https://github.com/PerfLab-EXaCT/minivite-x): Mini-application to demonstrate different memory patterns and test memory analysis tools.



## Miscellaneous tools for performance analysis and modeling

* [𝜇bench](https://github.com/PerfLab-EXaCT/ubench)

* [𝜇tools](https://github.com/PerfLab-EXaCT/utools)


## Misc work in progress

* [membench](https://github.com/PerfLab-EXaCT/membench)


<!-- 𝛍 𝜇 𝝁 -->


