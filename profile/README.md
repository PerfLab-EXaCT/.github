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
The increasing use of descriptive data formats (e.g., HDF5, netCDF) helps organize scientific datasets, but it also creates obscure bottlenecks due to the need to translate high level operations into file addresses and then into low-level I/O operations. DaYu is a method and toolset for analyzing (a) semantic relationships between logical datasets and file addresses, (b) how dataset operations translate into I/O, and (c) the combination across entire workflows. DaYu's analysis and visualization enables identification of critical bottlenecks and reasoning about remediation. With DaYu, one can extract workflow data patterns, develop insights into the behavior of data flows, and identify opportunities for both users and I/O libraries to optimize the applications.


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
    CHESS's new workflow for automating experiments with scanning electron microscopes. We are currently working on finalizing documentation and examples for different optimization targets.


* Co-design tools for hybrid workflows

    - [DataLife](https://github.com/pnnl/datalife):
    The combination of ever-growing scientific datasets and distributed workflow complexity creates I/O performance bottlenecks due to data volume, velocity, and variety. DataLife is a measurement and analysis toolset for distributed scientific workflows comprised of tasks that interact using files and storage. DataLife performs data flow lifecycle (DFL) analysis to guide decisions regarding coordinating task and data flows on distributed resources. DataLife provides tools for measuring, analyzing, visualizing, and estimating the severity of flow bottlenecks based on I/O and storage.

    - [DaYu](https://github.com/pnnl/DaYu):
    The increasing use of descriptive data formats (e.g., HDF5, netCDF) helps organize scientific datasets, but it also creates obscure bottlenecks due to the need to translate high level operations into file addresses and then into low-level I/O operations. DaYu is a method and toolset for analyzing (a) semantic relationships between logical datasets and file addresses, (b) how dataset operations translate into I/O, and (c) the combination across entire workflows.

    <!-- Candice's resource discovery -->

    - [FastFlow](https://github.com/pnnl/fastflow):
    When distributed scientific workflows are not intelligently executed, they can fail time constraints. To improve workflow response time, FastFlow is a new method of scheduling and resource assignment based on a monitor-analyze-optimize strategy. The key insight is to use the global perspective of interacting critical flows to guide a fast (locally greedy) scheduler that uses data flow projections to select between the better of flow parallelism and flow locality. Our method is linear time, unlike the next-best methods.
    <!-- * [FastFlow](https://github.com/pnnl/datalife): -->

    - [Scientific workflows](https://gitlab.com/perflab-exact/workflows):
    A suite of distributed scientific workflows with a range of workload characteristics

    <!-- - [TAZeR](https://github.com/pnnl/tazer): TAZeR (Transparent Asynchronous Zero-copy Remote I/O) is a remote I/O framework for transparently minimizing the access latencies of remote I/O in workflows. -->


* Interpretation of scientific data streams

    - [SamIAm](https://github.com/pnnl/SAMIAm): <!-- https://github.com/PerfLab-EXaCT/SamIAm -->
    [(Demo)](https://colab.research.google.com/github/PerfLab-EXaCT/SamIAm-LabelStudio/blob/main/SamIAm_Demo.ipynb)
    Image segmentation is a critical enabler for tasks ranging from medical diagnostics to autonomous driving. However, the correct segmentation semantics -- where are boundaries located? what segments are logically similar? -- change depending on the domain, such that state-of-the-art foundation models can generate meaningless and incorrect results. Moreover, in certain domains, fine-tuning and retraining techniques are infeasible: obtaining labels is costly and time-consuming; domain images (micrographs) can be exponentially diverse; and data sharing  (for third-party retraining) is restricted. To enable rapid adaptation of the best segmentation technology, we define _semantic boosting_: given a zero-shot foundation model, _guide_ its segmentation and adjust results to match domain expectations. We apply semantic boosting to the Segment Anything Model (SAM) to obtain _microstructure segmentation_ for transmission electron microscopy. Our booster, SAM-I-Am, extracts geometric and textural features of various intermediate masks to perform mask removal and mask merging operations.

    - [SuperSAM](https://github.com/pnnl/SuperSAM):
    Neural Architecture Search (NAS) is a powerful approach of automating the design of efficient neural architectures. In contrast to traditional NAS methods, recently proposed one-shot NAS methods prove to be more efficient in performing NAS. One-shot NAS works by generating a singular weight-sharing supernetwork that acts as a search space (container) of subnetworks. Despite its achievements, designing the one-shot search space remains a major challenge. In this work we propose a search space design strategy for Vision Transformer (ViT)-based architectures. In particular, we convert the Segment Anything Model (SAM) into a weight-sharing supernetwork called SuperSAM. Our approach involves automating the search space design via layer-wise structured pruning and parameter prioritization. While the structured pruning applies probabilistic removal of certain transformer layers, parameter prioritization performs weight reordering and slicing of MLP-blocks in the remaining layers. We train supernetworks on several datasets using the sandwich rule. For deployment, we enhance subnetwork discovery by utilizing a program autotuner to identify efficient subnetworks within the search space. The resulting subnetworks are 30-70% smaller in size compared to the original pre-trained SAM ViT-B, yet outperform the pretrained model. Our work introduces a new and effective method for ViT NAS search-space design.

    - [SamIAm-LabelStudio](https://github.com/PerfLab-EXaCT/SamIAm-LabelStudio)
    It is critical to pre-train AI models with accurate labels. However, precisely segmenting and labeling an image dataset is extraordinarily time-consuming. SamIAm-LabelStudio is a SamIAm-assisted labeling assistant to to rapidly create precise labels for image segments of identical materials.

    - [SamIAm Dataset](https://zenodo.org/records/10909552)
    It is critical to pre-train AI models with accurate labels. However, precisely segmenting and labeling an image dataset is extraordinarily time-consuming. SamIAm-LabelStudio is a SamIAm-assisted labeling assistant to to rapidly create precise labels for image segments of identical materials.


* Distributed model training

    - [MassiveGNN](https://github.com/pnnl/MassiveGNN) 
    [(development)](https://github.com/aishwaryyasarkar/Distributed_DGL):
    Graph Neural Networks (GNN) based on massively connected (distributed) GNNs pose significant challenges as even with the best methods, GNN training usually suffers from communication bottlenecks and load imbalance. <!-- due to non-determinism -->
    MassiveGNN introduces performant and productive training for massively connected (distributed) GNNs within the state-of-the-art [Amazon DistDGL](https://www.dgl.ai) (distributed Deep Graph Library). It brings practical trade-offs for improving the sampling and communication overheads for representation learning on distributed graphs by developing a parameterized continuous prefetch and eviction scheme.
    <!-- [MassiveGNN](https://github.com/pnnl/MassiveGNN) -->
    <!--  Performant and productive training for massively connected (distributed) GNNs within [Deep Graph Library](https://www.dgl.ai). These GNNs can be distributed on distributed and continuum resources. -->

    - [PyChip ensemble trainer](https://gitlab.com/perflab-exact/chess/pychip-ensemble-trainer):
    Ensemble-based training for AutoEM's PyChip material classifier.

    - [PRISMScope](https://gitlab.com/perflab-exact/chess/prism-scope):
    Given a description of the material's crystalline structure and microscope parameters, PRISMScope generates a range of (2D) image projections of a material (from a 4D original). Based on the input request, PRISMScope automatically retrieves a set of relevant parameters and uses [Prismatic](https://prism-em.com) to generate the 4D structure. The results enables association between a material, its crystalline structure, and STEM settings.

* Compression for science

    - [ViSemZ](https://gitlab.com/perflab-exact/chess/visemz):
      Scientific images are crucial for many experimental sciences, but dataset volumes pose significant challenges. Effective image compression must be quick, achieve high ratios, and enable automated interpretation by preserving essential domain features. Traditional image compressors like JPEG can distort critical textures at high compression ratios. In contrast, AI-based compression offers excellent image quality and impressive ratios. However, they are much slower than traditional approaches. To address this, ViSemZ is a high-performance image compressor that preserves *vi*sual *sem*antics.
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


