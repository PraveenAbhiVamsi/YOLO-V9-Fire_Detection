# YOLO-V9 for Forest Fire and Smoke Detection

## Overview

This project demonstrates the use of the YOLOv9 model for detecting forest fires and smoke. The notebook covers the steps from setting up the environment, downloading necessary model weights and datasets, to performing inference with pre-trained models.

## Before You Start

Ensure you have access to a GPU. You can verify this by running the `nvidia-smi` command. If there are any issues, navigate to `Edit` -> `Notebook settings` -> `Hardware accelerator`, set it to `GPU`, and click `Save`.

## Setup

### Clone and Install Dependencies

YOLOv9 is a new release. It is recommended to use a fork of the main repository because the `detect.py` script in the original repository contains a bug that prevents inference. This bug is patched in the fork.

Install the `roboflow` package to manage datasets, images, and models. The `roboflow` package is used to download the dataset from [Roboflow Universe](https://universe.roboflow.com/).

### Download Model Weights

In the YOLOv9 paper, versions `yolov9-s` and `yolov9-m` are mentioned, but the weights for these models are not yet available in the YOLOv9 [repository](https://github.com/WongKinYiu/yolov9).

### Download Example Data

If you want to run inference using your own file as input, upload the image to Google Colab and update `SOURCE_IMAGE_PATH` with the path to your file.

### Detection with Pre-trained COCO Model

The results of each subsequent inference session are saved in `{HOME}/yolov9/runs/detect/`, in directories named `exp`, `exp2`, `exp3`, etc. You can override this behavior by using the `--name` parameter.

## Dataset

Authenticate and download the dataset. The dataset must be saved inside the `{HOME}/yolov9` directory for the training to succeed.

In this tutorial, the [football-players-detection](https://universe.roboflow.com/roboflow-jvuqo/football-players-detection-3zvbc) dataset is used as an example. Feel free to replace it with your own dataset in YOLO format or use another dataset available on [Roboflow Universe](https://universe.roboflow.com).

## Steps

1. **Environment Setup**: Set up the environment and ensure GPU availability.
2. **Clone YOLOv9 Repository**: Clone the forked repository of YOLOv9 that contains the necessary bug fixes.
3. **Install Dependencies**: Install required packages including `roboflow`.
4. **Download Model Weights**: Download pre-trained YOLOv9 model weights.
5. **Download Dataset**: Authenticate and download your dataset from Roboflow.
6. **Run Inference**: Perform detection using the pre-trained COCO model.

## Notes

- The YOLOv9 implementation is subject to updates. Check the repository for the latest versions and patches.
- Ensure your dataset is in the correct format and placed in the specified directory for successful training and inference.

## Conclusion

This project serves as a guide to using the YOLOv9 model for forest fire and smoke detection. By following the steps outlined, you can set up the environment, download the necessary resources, and perform object detection tasks using YOLOv9.

For more details, refer to the [YOLOv9 repository](https://github.com/WongKinYiu/yolov9) and the [Roboflow Universe](https://universe.roboflow.com).
