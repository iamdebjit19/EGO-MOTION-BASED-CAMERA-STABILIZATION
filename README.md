# Ego-Motion Based Camera Stabilization

## Overview
This project implements an **ego-motion based camera stabilization pipeline** using classical computer vision techniques.  
The system estimates inter-frame camera motion (translation and rotation) and compensates for unwanted jitter to produce a stabilized video output.

The project is implemented entirely in **Python using OpenCV** and demonstrated through a **Jupyter Notebook**.



## Problem Statement
Hand-held and mobile cameras often introduce unwanted motion (jitter and shake), which degrades visual quality and affects downstream vision tasks such as VR, AR, and tracking.

This project aims to:
- Estimate camera ego-motion between frames
- Smooth the motion trajectory
- Generate a visually stabilized video



## Methodology / Pipeline

1. **Frame Extraction**
   - Read consecutive frames from the input video

2. **Feature Detection**
   - ORB keypoints are detected for robust feature representation

3. **Optical Flow Estimation**
   - Dense optical flow (Farneback) is used to track inter-frame motion

4. **Ego-Motion Estimation**
   - Translation (dx, dy) and rotation are computed from motion vectors

5. **Camera Trajectory Construction**
   - Motion parameters are accumulated over time

6. **Motion Smoothing**
   - Moving average smoothing is applied to reduce jitter

7. **Frame Warping**
   - Frames are transformed using smoothed motion parameters

8. **Evaluation & Results**
   - Motion variance before and after stabilization is analyzed
   - Visual comparison confirms significant jitter reduction



## Results

- Significant reduction in camera jitter
- Motion variance reduced by approximately **75–80%**
- Visual smoothness improved without structural distortion

Example outputs included:
- ORB keypoints visualization
- Optical flow tracks
- Motion trajectory graphs
- Variance reduction summary table



## Tools & Technologies
- Python
- OpenCV
- NumPy
- Jupyter Notebook



## Applications
- Virtual Reality (VR)
- Augmented Reality (AR)
- Mobile video stabilization
- Robotics and navigation
- Preprocessing for vision pipelines



## How to Run
1. Clone the repository
2. Open the Jupyter Notebook
3. Update the input video path if required
4. Run cells sequentially to reproduce results



## Author
**Debjit Ghosh**





