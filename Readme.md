# AerialMind: Towards Referring Multi-Object Tracking in UAV Scenarios

This official repository of the paper [AerialMind: Towards Referring Multi-Object Tracking in UAV Scenarios](). 
<div align=center><img src="./Figs/motivation.pdf"/></div>
# Abstract
Referring Multi-Object Tracking (RMOT) aims to achieve precise target detection and tracking through natural language instructions. While existing RMOT methods have demonstrated promising results in ground-level scenarios, they fundamentally lack the capability to address the unique challenges inherent in aerial perspectives. The dramatic scale variations, complex spatial relationships, and dynamic viewpoint changes in it lead to the limited generalization ability of these methods in real-world applications. Consequently, we introduce AerialMind, the first large-scale RMOT benchmark in Unmanned Aerial Vehicle (UAV) scenarios, which aims to bridge this research gap.  To facilitate its construction, we developed COALA, a novel semi-automated collaborative agent-based labeling assistant framework that significantly reduces labor costs while maintaining annotation quality. Furthermore, we propose HawkEyeTrack (HETrack), a novel tracking method that synergistically vision-language representation learning and enhances the perception of small-scale objects. Comprehensive experiments validated the challenge of our dataset and the effectiveness of our method. The dataset and code will be publicly at here.
<div align=center><img src="./Figs/vis_analysis.pdf"/></div>
# Method
<div align=center><img src="./Figs/annotation.pdf"/></div>

<div align=center><img src="./Figs/pipeline.pdf"/></div>
# Results

## Visualization
<div align=center><img src="./Figs/vis.pdf"/></div>
# Getting started
## Data Preparation
Put the tracking datasets in ./data. It should look like:
   ```
   ${PROJECT_ROOT}
    -- data
        --  AerialMind
            |-- Attribute
            |-- image_02
                 -- Visdrone
                 -- UAVDT
            |-- labels_with_ids
   ```

## Installation

* Linux, CUDA>=9.2, GCC>=5.4
  
* Python>=3.7

    We recommend you to use Anaconda to create a conda environment:
    ```bash
    conda create -n deformable_detr python=3.7 pip
    ```
    Then, activate the environment:
    ```bash
    conda activate deformable_detr
    ```
  
* PyTorch>=1.5.1, torchvision>=0.6.1 (following instructions [here](https://pytorch.org/))

    For example, if your CUDA version is 9.2, you could install pytorch and torchvision as following:
    ```bash
    conda install pytorch=1.5.1 torchvision=0.6.1 cudatoolkit=9.2 -c pytorch
    ```
  
* Other requirements
    ```bash
    pip install -r requirements.txt
    ```

* Build MultiScaleDeformableAttention
    ```bash
    cd ./models/ops
    sh ./make.sh
    ```

# TODO List

- [x] release the dataset [Train]
- [ ] release the dataset [Test]
- [ ] release the code
