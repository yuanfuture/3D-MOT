# MCCA-MOT
MCCA-MOT: Multimodal Collaboration-Guided Cascade Association Network for 3D Multi-Object Tracking

![fig 2  Framework](https://github.com/yuanfuture/MCCA-MOT/assets/113290883/cdde3a15-3c70-4d83-a49f-fad81f38e370)
The overall chartffow of the proposed MCCA-MOT approach for 3D multi-object tracking.

# Abstract
3D multi-object tracking is an important component of autonomous driving technology. Recent 3D multi-object tracking methods still suffer from issues such as information loss during the fusion of multimodal features, weak discriminative power of the association matrix, and poor robustness of single similarity measurement. To address these problems, this paper proposes a Multimodal Collaboration-guided Cascade Association network for 3D multi-object tracking (MCCA-MOT). We designed an adaptive diffusion fusion method for point cloud features, effectively solving the information loss problem. Then, we introduced a feature collaborative fusion method for fine-grained fusion of object features, further enhancing the distinctiveness of the object features. Finally, the designed multi-similarity measure-driven cascading association method effectively strengthened the discriminative power of the association matrix and the robustness of data association. Extensive experiments on the KITTI dataset have demonstrated the superiority of our proposed method in various performance metrics, indicating our framework possesses strong object recognition, localization, and association capabilities, effectively dealing with challenges such as small objects, occlusions, identity switches, and trajectory fragmentation.

# Cascade association
![Cascade association algorithm](https://github.com/yuanfuture/MCCA-MOT/assets/113290883/689f1129-040f-44a2-ad6e-9b731918dca2)

# Perfoemance
![KITTI test set Car](https://github.com/yuanfuture/MCCA-MOT/assets/113290883/582d9ed5-8e21-4c71-b342-d49049365728)
![KITTI test set Pedestrian](https://github.com/yuanfuture/MCCA-MOT/assets/113290883/258ef62a-c7d6-4895-b3ae-e7575093bf3c)

# Dependencies
Ubuntu 20.04.3 LTS
Intel(R) Core(TM) i7-11700F @ 2.50GHz
NVIDIA GeForce GTX 1080 Ti*2
python: 3.8.16
pytorch: 1.9.1
Torchvision: 0.10.1
CUDA: 11.1
CUDNN: 8.0.5

# Started

#### *1. Clone the github repository.*

```
git clone https://github.com/wangxiyang2022/DeepFusionMOT
```

#### *2. Dataset preparation*

 Please download the official KITTI [object tracking dataset](http://www.cvlibs.net/datasets/kitti/eval_tracking.php).

The final dataset organization should be like this:

```
DeepFusionMOT
├── data
│   ├── kitti
│   │   │── tracking
│   │   │   │──testing
|   │   │   │   ├──calib
|   │   │   │   |    ├──0000.txt
|   │   │   │   |    ├──....txt
|   │   │   │   |    └──0028.txt
|   │   │   │   ├──image_02
|   │   │   │   |    ├──0000
|   │   │   │   |    ├──....
|   │   │   │   |    └──0028
|   │   │   │   ├──oxts
|   │   │   │   |    ├──0000.txt
|   │   │   │   |    ├──....
|   │   │   │   |    └──0028.txt
|   │   │   │   ├──label_02
|   │   │   │   |    ├──0000.txt
|   │   │   │   |    ├──....txt
|   │   │   │   |    └──0028.txt
|   │   │   │   ├──velodyne
|   │   │   │   |    ├──0000
|   │   │   │   |    ├──....
|   │   │   │   |    └──0028  
│   │   │   │──training  # the structure is same as testing set
|   │   │   │   ├──calib
|   │   │   │   ├──image_02
|   │   │   │   ├──pose
|   │   │   │   ├──label_02
|   │   │   │   └──velodyne 
```

#### *3. Install dependency*

```
cd your_path/DeepFusionMOT
pip install -r requirements.txt
```






