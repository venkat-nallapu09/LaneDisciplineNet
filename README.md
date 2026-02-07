# LaneDisciplineNet 🚦

## AI-Based Lane Monitoring System for Road Safety

LaneDisciplineNet is an AI-powered computer vision system designed to monitor lane discipline, classify vehicles, estimate speed, and detect traffic violations in real time using roadside and overhead camera feeds. The system targets heterogeneous traffic conditions commonly found in developing urban environments and is designed to scale for Smart City deployments.

### Problem Statement
Urban traffic systems suffer from poor lane discipline, overspeeding, and inefficient enforcement, especially under heterogeneous traffic conditions. Traditional monitoring systems lack real-time intelligence, scalability, and automated decision support.

### modular flow & Methodology
```
Video Stream                                                      |   1.Camera installation at pilot sites - [🟩]
   ↓                                                              |
Frame Extractor                                                   |   2.Dataset creation and annotation - []
   ↓                                                              |
┌───────────────┬─────────────────┐                               |   3.Model training and optimization - []
│ Vehicle Model │ Lane Model      │                               |                 
│ (YOLOv8)     │ (UFLD-v2)        │                               |   4.Multi-module system integration - []
└───────┬───────┴────────┬────────┘                               |
        ↓                ↓                                        |   5.Real-world testing and validation - []
   Multi-Object       Lane Geometry                               |
   Tracking           & Boundaries                                |   6.Deployment with traffic management systems - []
        ↓                ↓
        └──────┬─────────┘
               ↓
      Lane Association Logic
               ↓
      Speed + Violation Engine
               ↓
        Events & Metrics
               ↓
        Dashboard / API
```



### Project expected structure
```bash

LaneDisciplineNet/
│
├── data/
│   ├── raw_videos/
│   ├── frames/
│   ├── annotations/
│   ├── calibration/
│
├── models/
│   ├── vehicle_detection/
│   │   ├── train.py
│   │   ├── infer.py
│   │   └── configs/
│   ├── lane_detection/
│   │   ├── train.py
│   │   └── infer.py
│
├── tracking/
│   ├── bytetrack.py
│   └── kalman.py
│
├── perception/
│   ├── detector.py
│   ├── lane_estimator.py
│   └── tracker.py
│
├── geometry/
│   ├── homography.py
│   └── camera_calibration.py
│
├── violations/
│   ├── speed.py
│   ├── lane_change.py
│   └── rule_engine.py
│
├── pipeline/
│   ├── video_pipeline.py
│   └── realtime_pipeline.py
│
├── api/
│   ├── app.py
│   └── schemas.py
│
├── dashboard/
│   └── streamlit_app.py
│
├── experiments/
│   └── ablations/
│
├── configs/
│   ├── model.yaml
│   └── deploy.yaml
│
├── tests/
│
├── docker/
│
└── README.md

```
