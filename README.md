# YOLOv8-twoStream
本系统是基于[YOLOv8](https://github.com/ultralytics/ultralytics?tab=readme-ov-file)改进的到双流RGBD实例分割网络+特征点匹配位姿估计来实现的针对针对盒状物体的吸取系统

经过渲染后的深度图在视觉上可以更好地帮助网络区分堆叠状态下的盒状物体，提高复杂堆叠场景下的分割指标

在获得了待抓取物体的分割结果后，系统将其与模板进行特征点匹配，可以获得模板到实际场景的RT矩阵，以此获得待抓取物体的位姿

## 数据集下载:
### 百度网盘
链接：https://pan.baidu.com/s/1gy5uSEOkZksnSurz3uXQcQ?pwd=ivie 

提取码：ivie 

### 谷歌云盘
https://drive.google.com/file/d/1q8ADmzlx0v_DcgkVKSn5sjA1ZDqhoqtP/view?usp=drive_link

## ![系统结构图](/sys.png)
