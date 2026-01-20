# ESTS-ROS-Dataset
A real-world indoor ROS 2 dataset acquired with TurtleBot 4 at the Higher School of Technology of Salé (UM5 Rabat). It includes LiDAR, odometry, IMU, RGB data, TF frames, SLAMToolbox maps, ROS 2 bag files, CSV exports, and videos, supporting SLAM, localization, navigation, and education.


UM5-ESTS TurtleBot ROS 2 Dataset

Overview

This repository provides a real-world indoor mobile robotics dataset acquired using a TurtleBot 4 running ROS 2 Humble at the Higher School of Technology of Salé (ESTS), Mohammed V University in Rabat, Morocco.

The dataset is intended to support SLAM, localization, mapping, and autonomous navigation research, as well as educational activities in mobile robotics.

Data were collected in real academic buildings (corridors, classrooms, laboratories, open halls) rather than controlled laboratory environments, making the dataset suitable for realistic benchmarking and algorithm evaluation.


Platform and Software
	•	Robot: TurtleBot 4 (Standard configuration)
	•	OS & Middleware: Ubuntu 22.04, ROS 2 Humble
	•	SLAM Framework: SLAMToolbox
	•	Navigation Framework: Nav2


Dataset Contents

Each acquisition sequence includes synchronized multi-sensor data:
	•	2D LiDAR scans
	•	Wheel encoder odometry
	•	IMU measurements
	•	RGB camera streams
	•	TF and TF_static transforms
	•	Occupancy grid maps (.pgm, .yaml, .png)
	•	ROS 2 bag files (.db3)
	•	CSV exports of sensor data
	•	Video recordings of each traversal


Dataset Structure

SLAM_ESTS/
├── ADMINISTRATION/
│   ├── RDC/
│   │   ├── map.yaml
│   │   ├── map.pgm
│   │   ├── map.png
│   │   └── Odom_Scan_Cam/
│   │       ├── odom_scan_camera_0.db3
│   │       ├── metadata.yaml
│   │       ├── video.mp4
│   │       └── csv_output/
│   │           ├── odom.csv
│   │           ├── scan.csv
│   │           └── camera.csv
│   └── ETAGE1/
├── BLOC_1/
└── DEPARTEMENT/

Each top-level folder corresponds to a building, with subfolders representing individual floors.


Use Cases

This dataset can be used for:
	•	Benchmarking 2D LiDAR-based SLAM algorithms
	•	Evaluating ROS 2 navigation pipelines (Nav2)
	•	Offline replay and analysis using rosbag2
	•	Teaching and student projects in mobile robotics
	•	Research on realistic indoor environments


Data Acquisition
	•	Data recorded as ROS 2 bag files preserving original timestamps
	•	Manual robot driving at controlled speed to ensure scan overlap
	•	Maps generated using SLAMToolbox
	•	CSV exports provided for use outside the ROS ecosystem


Citation

If you use this dataset in your research, please cite:

@inproceedings{Abouzahir2026TurtleBotDataset,
  title     = {A ROS 2-Based Indoor Mapping Dataset Acquired in an Academic Building Using TurtleBot 4},
  author    = {Abouzahir, Mohamed and Ayachi, Ouafa},
  booktitle = {Proceedings of WCCS 2026},
  year      = {2026}
}


License

This dataset is released for research and educational use.
Please check the LICENSE file for details.


Contact

Mohamed Abouzahir
LASTIMI Laboratory – ESTS
Mohammed V University in Rabat, Morocco
📧 mohamed.abouzahir@est.um5.ac.ma

