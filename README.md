# AI_Pose_Estimation

A Python computer vision pipeline that uses **YOLO pose estimation** to track body landmarks in real time and analyze exercise form — currently implemented for squats.

## Features

- YOLO-based pose model (`src/models/yolo_pose.py`) with a pluggable frame-processing pipeline
- Exercise registry pattern (`src/exercises/registry.py`) with squat detection as the first implementation (`src/exercises/squat.py`)
- Automatic device selection (`src/pipeline/device_selector.py`) — runs on CUDA or Apple Silicon (MPS)
- Config-driven app, exercise and model settings (`config/*.yml`)
- Real-time visualization/overlay rendering (`src/visualization/renderer.py`)

## Tech stack

Python · PyTorch · YOLO (pose) · OpenCV

## Setup

Conda environments are provided for both platforms:

```bash
conda env create -f environment_mac_intel.yml      # macOS
conda env create -f environment_linux_cuda.yml      # Linux + CUDA
python main.py
```
