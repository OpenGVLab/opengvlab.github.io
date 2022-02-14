# Overview

We construct a well-designed data system, GV-D, which
consists of  $ GV$-$D$-$10B$ with multi-modal data, as well as $ GV$-$D_c$, $ GV$-$D_d$ and  $GV$-$D_s$ with classification, detection, and segmentation annotations, respectively. Here, we release $ GV$-$D_c$ and $ GV$-$D_d$.

# Description
To efficiently obtain annotations for classification and detection tasks, we propose a hierarchical label system with a rigorously-defined taxonomy. The label system is a crucial component of our GV-D with more than 119K concepts from existing datasets, WikiData and WordNet. 

Powered by the hierarchical label system, we annotate 8.1 million images, including 10.5 million semantic labels and 2.7 million bounding boxes. 

Besides, we inherit public datasets including both their concepts and images. We collect ten image classification datasets and three object detection datasets. They are ImageNet21K，iNaturalist2021，Herbarium2021，DF20，iWildCam2020，TsinghuaDog, Places365，iFood2019，CompCars, COCO, OpenImages, and Objects365. 

After mergeing newly collected data public datasets , we construct two datasets as GV-D$_\text{c}$ and GV-D$_\text{d}$. 

# Download

GV-D can be accessed from this website: http://opengvlab.shlab.tech/bamboo