# MCCA-MOT
MCCA-MOT: Multimodal Collaboration-Guided Cascade Association Network for 3D Multi-Object Tracking

![fig 2  Framework](https://github.com/yuanfuture/MCCA-MOT/assets/113290883/cdde3a15-3c70-4d83-a49f-fad81f38e370)
The overall chartffow of the proposed MCCA-MOT approach for 3D multi-object tracking.

# Abstract
3D multi-object tracking is an important component of autonomous driving technology. Recent 3D multi-object tracking methods still suffer from issues such as information loss during the fusion of multimodal features, weak discriminative power of the association matrix, and poor robustness of single similarity measurement. To address these problems, this paper proposes a Multimodal Collaboration-guided Cascade Association network for 3D multi-object tracking (MCCA-MOT). We designed an adaptive diffusion fusion method for point cloud features, effectively solving the information loss problem. Then, we introduced a feature collaborative fusion method for fine-grained fusion of object features, further enhancing the distinctiveness of the object features. Finally, the designed multi-similarity measure-driven cascading association method effectively strengthened the discriminative power of the association matrix and the robustness of data association. Extensive experiments on the KITTI dataset have demonstrated the superiority of our proposed method in various performance metrics, indicating our framework possesses strong object recognition, localization, and association capabilities, effectively dealing with challenges such as small objects, occlusions, identity switches, and trajectory fragmentation.

# Cascade association
![Cascade association algorithm](https://github.com/yuanfuture/MCCA-MOT/assets/113290883/2da988da-92f9-4fd1-af9a-c76664fb38e5)


# Perfoemance
![KITTI test set Car](https://github.com/yuanfuture/MCCA-MOT/assets/113290883/dbf42a72-dc32-4e0e-aa99-088de2a64558)
![KITTI test set Pedestrian](https://github.com/yuanfuture/MCCA-MOT/assets/113290883/258ef62a-c7d6-4895-b3ae-e7575093bf3c)


# Dependencies
#### Ubuntu 20.04.3 LTS
#### Intel(R) Core(TM) i7-11700F @ 2.50GHz<br>
#### NVIDIA GeForce GTX 1080 Ti*2<br>
#### python: 3.8.16<br>
#### pytorch: 1.9.1<br>
#### Torchvision: 0.10.1<br>
#### CUDA: 11.1<br>
#### CUDNN: 8.0.5<br>

# Started

#### *1. Clone the github repository.*

```
git clone https://github.com/yuanfuture/MCCA-MOT
```

#### *2. Dataset preparation*

Please go to KITTI official to download the required datasets. [object tracking dataset](http://www.cvlibs.net/datasets/kitti/eval_tracking.php).

The final dataset organization should be like this:

    ```
    MCCA-MOT
    ├── data
    │   ├── kitti
    │   │   │── training
    │   │   │   ├──calib & velodyne & label_02 & image_02 & depth_2 & (optional: planes) 
    │   │   │── testing
    │   │   │   ├──calib & velodyne & image_02 
    ```

#### *3. Install dependency*

```
cd your_path/MCCA-MOT
pip install -r requirements.txt
```
#### *4. Run*

```
python main.py
```


#### *5. KITTI MOT Evaluation*

If you want to evaluate the tracking results using the evaluation tool on the KITTI website, you will need to go https://github.com/JonathonLuiten/TrackEval to download the evaluation code and follow the appropriate steps to set.

the following results will be obtained.

|                      | HOAT( **↑)** | **AssA( **↑)**** | **LocA**(**↑)** | MOTA（↑） | MOTP(**↑)** |  FP(**↓)**  |   FN（↓） |  IDSW（↓）|
| :------------------: | :----------: | :--------------: | :-------------: | :-------: | :---------: | :---------: | :------:  | :------:  |
|       **Car**        |    79.31%    |      83.49%      |     88.60%      |   86.71%  |   87.51%    |    3992     |   513     |     66    |
|    **Pedestrian**    |    51.79%    |      56.95%      |     78.52%      |   60.36%  |   74.50%    |    7687     |   1317    |    173    |


### Citation

If you find this work useful, please consider to cite our paper:

```
@ARTICLE{  
author={},  
journal={},   
title={MCCA-MOT: Multimodal Collaboration-Guided Cascade Association Network for 3D Multi-Object Tracking},   
year={2024},  volume={},  number={},  pages={},  doi={}

```





