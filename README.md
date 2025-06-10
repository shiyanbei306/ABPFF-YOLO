
## <div align="center">Documentation</div>

Welcome to the ABPFF-YOLO repository! This project implements the ABPFF-YOLO algorithm, a novel method based on YOLOv8s designed for detecting small objects in UAV (Unmanned Aerial Vehicle) images. The algorithm integrates an auxiliary backbone and a multi-branch feature fusion module to enhance small object detection performance.and see the [ABPFF-YOLO Docs](https://docs.ultralytics.com) for full documentation on training, validation, prediction and deployment.

<details open>
<summary>Install</summary>

Pip install the ultralytics package including all [requirements](https://github.com/ultralytics/ultralytics/blob/main/requirements.txt) in a [**Python>=3.8**](https://www.python.org/) environment with [**PyTorch>=1.13.1**](https://pytorch.org/get-started/locally/).

```bash
pip install ultralytics
```

</details>

<details open>
<summary>Usage</summary>

#### CLI

ABPFF-YOLO may be used directly in the Command Line Interface (CLI) with a `yolo` command:

```bash
yolo predict model=yolov8n.pt source='https://ultralytics.com/images/bus.jpg'
```

`yolo` can be used for a variety of tasks and modes and accepts additional arguments, i.e. `imgsz=640`. See the YOLOv8 [CLI Docs](https://docs.ultralytics.com/usage/cli) for examples.



[Models](https://github.com/ultralytics/ultralytics/tree/main/ultralytics/models) download automatically from the latest Ultralytics [release]

#### Requirements
Python 3.8+，
PyTorch 1.13.1，
Other dependencies listed in requirements.txt
```bash
pip install -r requirements.txt
```


See [Pose Docs](https://docs.ultralytics.com/tasks/pose) for usage examples with these models.

VisDrone Dataset: A leading UAV vision dataset with diverse data from 14 Chinese cities, featuring various objects like pedestrians and vehicles under different scene densities, weather, and lighting conditions.

- **mAP<sup>val</sup>** values are for single-model single-scale on [COCO Keypoints val2017](http://cocodataset.org)
  dataset.
  <br>Reproduce by `yolo val pose data=coco-pose.yaml device=0`
- **Speed** averaged over COCO val images using an [Amazon EC2 P4d](https://aws.amazon.com/ec2/instance-types/p4/) instance.
  <br>Reproduce by `yolo val pose data=coco8-pose.yaml batch=1 device=0|cpu`

</details>


