---
title: "OpenCap"
excerpt: "3D human movement dynamics from smartphone videos <br/><img src='/images/OpenCap_1.png'>"
collection: portfolio
---

OpenCap is a software package to quantify human movement from smartphone videos. OpenCap combines computer vision, deep learning, and biomechanical modeling and simulation to estimate the kinematics (ie, motion) and kinetics (ie, musculoskeletal forces) of movement from two or more videos. OpenCap comes with an iOS application, a web application, and is deployed in the cloud. To get started, visit [opencap.ai](https://www.opencap.ai/).

<p align="center">
  <img src="/images/OpenCap-worflow.jpg">
</p>

OpenCap is open-source, under Apache 2.0 license, and available on GitHub. The backend can be found in [this repository](https://github.com/stanfordnmbl/opencap-core). OpenCap uses a deep learning model to predict anatomical markers from sparse video keypoints. The model was trained using [this code](https://github.com/antoinefalisse/marker-augmentation). Finally, to estimate kinetics (ie, musculoskeletal forces), OpenCap relies on muscle-driven musculoskeletal simulations. You can find example of how to generate such simulations in [this repository](https://github.com/stanfordnmbl/opencap-processing). More details in [the preprint](https://www.biorxiv.org/content/10.1101/2022.07.07.499061v1) of our paper.
