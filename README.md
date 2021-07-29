# MMD_Detectron2

The project is inspired by the OpenMMD project [OpenMMD](https://github.com/peterljq/OpenMMD).

Except for the final VMD file generation(I have no 3D model to generate, so do not do this step now.), the step is similar with the OpenMMD.

However, I replace some methods in OpenMMD to the recent networks with Pretrained Weights. Considering the specialistic of the animation dataset, I will try to use Unsupervised methods after finding a large-scale anime dataset.

Including Methods:

1.(Pose Estimation) 3D human pose estimation in video with temporal convolutions and semi-supervised training,CVPR2019    [code](https://github.com/facebookresearch/VideoPose3D)

2.(Included in 1,Motion Keypoint Detection) COCO Keypoint-RCNN Detection Based On Detectron2(I will update this method because I find it is not very accurate)
2.Ex(Recent method in Human keypoint detection, but the result is worse) Deep High-Resolution Representation Learning for Human Pose Estimation (CVPR 2019) [code](https://github.com/leoxiaobin/deep-high-resolution-net.pytorch)

3.(Single-image Depth Estimation)Digging into Self-Supervised Monocular Depth Prediction,ICCV2019   [code](https://github.com/nianticlabs/monodepth2/)


   
