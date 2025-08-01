# GRL-SLAM: A Robust 3D Mapping and Fruit Localization System for Dynamic Vineyard

![System Overview](images/grl_slam_framework.png)

**GRL-SLAM** is a real-time SLAM and fruit localization system designed for complex and dynamic vineyard environments. It integrates lightweight semantic segmentation with a visual SLAM backend, dynamic object removal, and 3D clustering to support autonomous agricultural robots.

---

## 🔧 Features

- 🧠 **PIDSNet**: A lightweight segmentation network with attention-based enhancements.
- 🧹 **Dynamic Object Filtering**: Removes pedestrians and moving elements to stabilize SLAM.
- 🌐 **3D Semantic Mapping**: Embeds fruit information into point clouds.
- 🍇 **Grape Bunch Clustering**: Uses DBSCAN and PCA for ellipsoid modeling.
- 🚀 **Real-Time Execution**: 23.1 FPS on standard GPU hardware.

---

## 📷 Visual Results

### 🔍 Semantic Segmentation
PIDSNet accurately segments grape bunches and pedestrians in complex vineyard scenes.

**Static Scene**  
![Segmentation Static](images/segmentation_static.png)

**Dynamic Scene**  
![Segmentation Dynamic](images/segmentation_dynamic.png)

---

### 🗺️ 3D Mapping

**Original SLAM Mapping**  
![3D Original](images/3d_original.png)

**Semantic-Enhanced Mapping**  
![3D Semantic](images/3d_semantic.png)

---

### 🍇 Fruit Localization and Clustering

**Extracted Grape Point Clouds**  
![Grape Points](images/grape_points.png)

**Clustered & Fitted with Ellipsoids**  
![Grape Clusters](images/grape_clusters.png)

---

## 🧠 Network Architecture

**GRL-SLAM Pipeline**  
![GRL-SLAM Overview](images/grl_slam_framework.png)

**PIDSNet Semantic Segmentation Structure**  
![PIDSNet](images/pidsnet_framework.png)

---

## 🧪 Experimental Setup

The mobile platform is equipped with:
- ZED2 stereo camera
- Robosense Helios 32 LiDAR (for ground truth)
- Intel i5-12500H + NVIDIA RTX 3060
- Ubuntu 20.04 with PyTorch + ROS

---

## 📊 Performance Summary

| Metric                        | Value                     |
|------------------------------|---------------------------|
| Semantic mIoU                | 89.45%                    |
| 3D Localization Error        | 21.02 mm (avg)            |
| Bunch Counting Error         | 5.7% (single-row)         |
| System Speed                 | 23.1 FPS                  |

