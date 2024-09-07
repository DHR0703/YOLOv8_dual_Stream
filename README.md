# DS-YOLO: A Robotic Grasping Method of Box-Shaped Objects Based on Dual-Stream YOLO


In industrial production, efficient sorting and precise placement of box-shaped objects
 have always been a key task, traditionally relying heavily on manual operation. Given the rapid
 development of industrial automation, exploring automation solutions to replace human labor has
 become an inevitable trend. At present, there is still a lack of box-shaped object classification and
 grasping methods for cluttered stacking scenes. To address this issue, this paper proposes an RGBD
 instance segmentation network based on the [YOLOv8](https://github.com/ultralytics/ultralytics?tab=readme-ov-file)  framework, called as DS-YOLO, and then
 combined with feature point matching algorithm, we can achieve precise recognition, grasping, and
 orderly placement of box-shaped objects in complex stacking environments. Due to the lack of a
 dataset for box-shaped objects, we created a synthetic dataset, referred to as Snack Box. Compared
 to state-of-the-art methods, the model trained on the Snack Box dataset using DS-YOLO showed
 3.9% and 2% higher mAP50 and mAP50-90 metrics, respectively. In experiments involving 1,000
 scenarios from the synthetic dataset, 93.3% of the scenes provided grasp parameters, with an average
 center point error of 6.45mm, and average errors of 4.18° for plane normal vectors and 6.85° for
 object angles. Furthermore, our method also demonstrates superior performance compared to state
of-the-art approaches on the LLVIP infrared dataset.

**The source code will be submitted after the paper is accepted.**
# Grasping demo video:
## youtube
https://youtu.be/IVwSE0scVIk
## bilibili
https://www.bilibili.com/video/BV1kUHDeZEVd

## Datasets Download:
### Google Cloud Drive
https://drive.google.com/file/d/1q8ADmzlx0v_DcgkVKSn5sjA1ZDqhoqtP/view?usp=drive_link

### baidu pan
链接：https://pan.baidu.com/s/1gy5uSEOkZksnSurz3uXQcQ?pwd=ivie 
提取码：ivie 

## Frame diagram
### ![系统结构图](/sys.png)

## Experimental index
### Results on a jumbled stacked box-shaped dataset
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

### Results on the LLVIP infrared dataset
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

