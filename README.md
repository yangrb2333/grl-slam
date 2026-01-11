# A Real-Time Semantic 3D Vineyard Mapping and Fruit Localization System for Yield Estimation in Dynamic Vineyards

This is a real-time and robust system for 3D mapping and fruit localization in dynamic vineyard environments. It combines the ORB-SLAM3 framework with a lightweight semantic segmentation network (EFSegNet), dynamic feature filtering, point cloud optimization, and ellipsoid-based grape bunch localization.

---

## 🧠 Network Architecture

**Pipeline**  
![Our System Overview](figures/grl_slam_framework.png)

**EFSegNet Semantic Segmentation Structure**  
![EFSegNet](figures/pidsnet_framework.png)

---

## 🔧 Features

- 🧠 **EFSegNet**: A lightweight segmentation network with attention-based enhancements.
- 🧹 **Dynamic Object Filtering**: Removes pedestrians and moving elements to stabilize SLAM.
- 🌐 **3D Semantic Mapping**: Embeds fruit information into point clouds.
- 🍇 **3D Grape Localization**: Uses DBSCAN and PCA for ellipsoid modeling.
- 🚀 **Real-Time Execution**: 23.1 FPS on standard GPU hardware.

---

## 📷 Visual Results

### 🔍 Semantic Segmentation
EFSegNet accurately segments grape bunches and pedestrians in complex vineyard scenes.

**Static Scene**  
![Segmentation Static](figures/segmentation_static.png)

**Dynamic Scene**  
![Segmentation Dynamic](figures/segmentation_dynamic.png)

---

### 🗺️ 3D Mapping

**Original SLAM Mapping**  
![3D Original](figures/3d_original.png)

**Semantic-Enhanced Mapping**  
![3D Semantic](figures/3d_semantic.png)

---

### 🍇 Fruit Localization and Clustering

**Extracted Grape Point Clouds**  
![Grape Points](figures/grape_points.png)

**Clustered & Fitted with Ellipsoids**  
![Grape Clusters](figures/grape_clusters.png)

---

## 🧪 Experimental Setup

The mobile platform is equipped with:
- ZED2 stereo camera
- Robosense Helios 32 LiDAR (for ground truth)
- Intel i5-12500H + NVIDIA RTX 3060
- Ubuntu 20.04 with PyTorch + ROS

---

## 📦 Dataset Download

We provide the dataset used in our experiments for reproducibility and further research.

- 📁 **Dataset Download (Baidu Netdisk)**  
  🔗 [https://pan.baidu.com/s/1spMpWn3_jbq4pOYelJ1kVw?pwd=1234](https://pan.baidu.com/s/1spMpWn3_jbq4pOYelJ1kVw?pwd=1234)  
  🔑 **Extraction Code**: `1234`  
> ⚠️ If you use the dataset, please cite our paper accordingly.

---

## 📊 Performance Summary

| Metric                        | Value                     |
|------------------------------|---------------------------|
| Semantic mIoU                | 89.45%                    |
| 3D Localization Error        | 21.02 mm (avg)            |
| Bunch Counting Error         | 5.7% (single-row)         |
| System Speed                 | 23.1 FPS                  |
