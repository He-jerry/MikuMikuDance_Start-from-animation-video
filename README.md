# MMD_Detectron2

```diff
- text in red
+ text in green
! text in orange
# text in gray
```


The project is inspired by the OpenMMD project [OpenMMD](https://github.com/peterljq/OpenMMD).

The main idea is to solve the MMD generation problem while the original input video is animation(Cartoon) but not real human video. Because the domain of the animation is not similar with real human, it makes the pose estimation not as accurate as real world. However, I still want to test it because the animation is the main video type to generate the MMD file.

Except for the final VMD file generation(I have no 3D model to generate, so do not do this step now.), the step is similar with the OpenMMD.

However, I replace some methods in OpenMMD to the recent networks with Pretrained Weights. Considering the specialistic of the animation dataset, I will try to use Unsupervised methods after finding a large-scale anime dataset.

Including Methods:

1.(Pose Estimation) 3D human pose estimation in video with temporal convolutions and semi-supervised training,CVPR2019    [code](https://github.com/facebookresearch/VideoPose3D)

2.(Included in 1,Motion Keypoint Detection) COCO Keypoint-RCNN Detection Based On Detectron2(I will update this method because I find it is not very accurate)

2.Ex(Recent method in Human keypoint detection, but the result is worse) Deep High-Resolution Representation Learning for Human Pose Estimation (CVPR 2019) [code](https://github.com/leoxiaobin/deep-high-resolution-net.pytorch)

3.(Single-image Depth Estimation)Digging into Self-Supervised Monocular Depth Prediction,ICCV2019   [code](https://github.com/nianticlabs/monodepth2/)


Use the Colab File to run! [MikuMukuDance.ipynb](https://github.com/He-jerry/MMD_Detectron2/blob/main/MikuMukuDance.ipynb)

(Because I have finished the codes of each part, it may seems messy.)


Result
==== 

original short video
-----

![image](https://github.com/He-jerry/MMD_Detectron2/blob/main/video_teaser/original.gif)

[Original Video](https://www.bilibili.com/video/BV1V54y1J7HS)

```diff
+Which is a cute Virtuber in BiliBili: Merry
```

Bilibili Space Address: [Bilibili](https://space.bilibili.com/745493?spm_id_from=333.788.b_765f7570696e666f.2)


Inc.1: 2D Keypoint Detection
-----
![image](https://github.com/He-jerry/MMD_Detectron2/blob/main/video_teaser/1_1.gif)


Inc.2: 2D Keypoint to 3D pose estimation
-----
![image](https://github.com/He-jerry/MMD_Detectron2/blob/main/video_teaser/1_3.gif)

Inc.2-ex: Human Pose Estimation
-----
![image](https://github.com/He-jerry/MMD_Detectron2/blob/main/video_teaser/2ex_2.gif)

The frames with Keypoint Detection Result(Although the position is wrong)

![image](https://github.com/He-jerry/MMD_Detectron2/blob/main/video_teaser/2ex.gif)

Full video in the 2-Ex Human Keypoint Detection.

It is quiet sad that the network could not be adapted in this new domain.

Inc.3 Video Depth Estimation
-----

![image](https://github.com/He-jerry/MMD_Detectron2/blob/main/video_teaser/3.gif)

