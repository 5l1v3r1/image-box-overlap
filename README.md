# [Predicting Visual Overlap of Images Through Interpretable Non-Metric Box Embeddings](https://arxiv.org/abs/)

**[Anita Rau](https://www.ucl.ac.uk/surgical-robot-vision/anita-rau), [Guillermo Garcia-Hernando](https://guiggh.github.io/), [Danail Stoyanov](https://scholar.google.co.uk/citations?user=pGfEK6UAAAAJ&hl=en), [Gabriel J. Brostow](http://www0.cs.ucl.ac.uk/staff/g.brostow/) and [Daniyar Turmukhambetov](http://dantkz.github.io/about)  – ECCV 2020 (Spotlight presentation)**


[Link to paper](https://arxiv.org/abs/)  

<p align="center">
  <a href="https://storage.googleapis.com/niantic-lon-static/research/image-box-overlap/short-video.mp4">
  <img src="assets/2min.png" alt="2 minute ECCV presentation video link" width="400">
  </a>
</p>


<p align="center">
  <a href="https://storage.googleapis.com/niantic-lon-static/research/image-box-overlap/long-video.mp4">
  <img src="assets/10min.png" alt="10 minute ECCV presentation video link" width="400">
  </a>
</p>


**Code and supplementary pdf are coming soon...**


<p align="center">
  <img src="assets/teaser.png" alt="Our box representation versus traditional vector representation of images" width="600" />
</p>

To what extent are two images picturing the same 3D surfaces? Even when this is a known scene, the answer typically
requires an expensive search across scale space, with matching and geometric verification of large sets of
local features. This expense is further multiplied when a query image is evaluated against
a gallery, e.g. in visual relocalization. While we don’t obviate the need for geometric
verification, we propose an interpretable image-embedding that cuts the search in scale space to essentially a lookup.
Our approach measures the asymmetric relation between two images. The model then learns
a scene-specific measure of similarity, from training examples with known 3D visible-surface overlaps.
The result is that we can quickly identify, for example, which test image is a close-up version of another, and
by what scale factor. Subsequently, local features need only be detected at that scale. We validate our scene-specific
model by showing how this embedding yields competitive image-matching results, while being simpler, faster,
and also interpretable by humans.

<p align="center">
  <img src="assets/method.png" alt="Overview of our stereo data generation approach" width="600" />
</p>

Inspired by recent progress in monocular depth estimation, we generate plausible disparity maps from single images. In turn, we use those flawed disparity maps in a carefully designed pipeline to generate stereo training pairs. Training in this manner makes it possible to convert any collection of single RGB images into stereo training data. This results in a significant reduction in human effort, with no need to collect real depths or to hand-design synthetic data. We can consequently train a stereo matching network from scratch on datasets like COCO, which were previously hard to exploit for stereo. 


<p align="center">
  <img src="assets/world-space-measure.png" alt="Different ways of encoding positional relationship between pairs of images" width="600" />
</p>


<p align="center">
  <img src="assets/relations.png" alt="Normalize surface overlap measure provides interpretable relationships between pairs of images" width="600" />
</p>


<p align="center">
  <img src="assets/generalization-plot.png" alt="Our box embeddings can provide interpretable relationships between images from the test set" width="600" />
</p>


<p align="center">
  <img src="assets/relative-scale.png" alt="Predicted normalized surfaces overlap can be used to compute relative scale between pairs of images" width="600" />
</p>



## ✏️ 📄 Citation

If you find our work useful or interesting, please consider citing [our paper](https://arxiv.org/abs/):

```
@inproceedings{rau-2020-image-box-overlap,
 title   = {Predicting Visual Overlap of Images Through Interpretable Non-Metric Box Embeddings},
 author  = {Anita Rau and
            Guillermo Garcia-Hernando and
            Danail Stoyanov and
            Gabriel J. Brostow and
            Daniyar Turmukhambetov
           },
 booktitle = {European Conference on Computer Vision ({ECCV})},
 year = {2020}
}
```


# 👩‍⚖️ License
Copyright © Niantic, Inc. 2020. Patent Pending. All rights reserved. Please see the license file for terms.
