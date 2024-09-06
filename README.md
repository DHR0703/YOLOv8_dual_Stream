# DS-YOLO: A Robotic Grasping Method of Box-Shaped Objects Based on Dual-Stream YOLO
This system is based on the improved [YOLOv8](https://github.com/ultralytics/ultralytics?tab=readme-ov-file) Dual-stream RGBD instance segmentation network + feature point matching pose estimation to achieve the suction system for box objects

Visually, the rendered depth map can better help the network distinguish the box-like objects in the stacked state, and improve the segmentation index in complex stacked scenes

After obtaining the segmentation result of the object to be grabbed, the system matches the feature points with the template, and the RT matrix of the template to the actual scene can be obtained, so as to obtain the pose of the object to be grabbed

The project code will be uploaded after the paper is accepted

本系统是基于[YOLOv8](https://github.com/ultralytics/ultralytics?tab=readme-ov-file)改进的到双流RGBD实例分割网络+特征点匹配位姿估计来实现的针对针对盒状物体的吸取系统

经过渲染后的深度图在视觉上可以更好地帮助网络区分堆叠状态下的盒状物体，提高复杂堆叠场景下的分割指标

在获得了待抓取物体的分割结果后，系统将其与模板进行特征点匹配，可以获得模板到实际场景的RT矩阵，以此获得待抓取物体的位姿

项目代码将在论文被录用后上传
# Grasping demo video/实际抓取实验演示视频
## youtube
https://youtu.be/IVwSE0scVIk
## bilibili
https://www.bilibili.com/video/BV1kUHDeZEVd

## Datasets Download/数据集下载:
### Google Cloud Drive
https://drive.google.com/file/d/1q8ADmzlx0v_DcgkVKSn5sjA1ZDqhoqtP/view?usp=drive_link

### 百度网盘
链接：https://pan.baidu.com/s/1gy5uSEOkZksnSurz3uXQcQ?pwd=ivie 
提取码：ivie 

## Frame diagram/框架示意图
### ![系统结构图](/sys.png)

## Experimental index/实验指标
### Results on a jumbled stacked box-shaped dataset/在杂乱堆叠的盒状物体数据集上的结果
| **Modality** | **Method** | **mAP50** | **mAP50-95** |
|:------------:|:----------:|:---------:|:------------:|
| RGB          | YOLOv8     | 0.946     | 0.881        |
| RGBD         | CMMHA      | 0.930     | 0.872        |
| RGBD         | REF        | 0.949     | 0.892        |
| RGBD         | SLBAF      | 0.892     | 0.835        |
| RGBD         | FIRI       | 0.928     | 0.878        |
| RGBD         | CFT        | 0.953     | 0.896        |
| RGBD         | SuperYOLO  | 0.954     | 0.886        |
| RGBD         | ours       | **0.985**     | **0.901**        |

### Results on the LLVIP infrared dataset/在LLVIP红外数据集上的结果
| **Modality** | **Method**               | **mAP50** | **mAP50-95** |
|:------------:|:------------------------:|:---------:|:------------:|
| RGB          | (2023)YOLOv8         | 0.908     | 0.535        |
| RGB+IR       | (2023)TFDet         | 0.957     | 0.561        |
| RGB+IR       | (2021)CFT            | **0.975**     | 0.636        |
| RGB+IR       | (2024)AMFD           | 0.952     | 0.583        |
| RGB+IR       | (2024)TEXT-IF        | 0.941     | 0.602        |
| RGB+IR       | (2023)CSSA          | 0.943     | 0.592        |
| RGB+IR       | (2024)Mamba-Fusion   | 0.97      | 0.63         |
| RGB+IR       | (2023)DIVFusion      | 0.898     | 0.52         |
| RGB+IR       | (2024)RSDet          | 0.958     | 0.613        |
| RGB+IR       | ours                     | 0.97      | **0.653**        |

