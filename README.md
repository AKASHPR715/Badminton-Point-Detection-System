# 🏸 Badminton Point Detection System  
**Real-Time Cork Tracking & Point Detection Using TrackNet, OpenCV, and YOLO**

> 🚫 **IMPORTANT NOTICE**  
> This project was developed as part of a professional engagement with **iCore Technologies**.  
> Due to confidentiality and intellectual property rights, the **source code, models, and training data cannot be shared publicly**.

---

## 📘 Overview

The Badminton Point Detection System is a **real-time computer vision application** designed to automate point recognition in badminton matches. Traditional sports scoring can often be subjective or prone to human error, especially in fast-paced games like badminton. This system addresses these challenges by employing advanced **AI-powered object detection and trajectory tracking algorithms** to ensure accurate point determination.

This solution was specifically developed for **iCore Technologies**, an AI-driven sports analytics company, and has been tested in semi-professional match settings to aid referees, broadcasters, and performance analysts in accurately detecting shuttle positions and determining valid points.

---

## 🏢 Project Purpose & Professional Context

### 🎯 Developed For:
**iCore Technologies**  
An innovation-focused company leveraging AI and ML to transform sports analysis and automation.

### 📍 Objective:
To build a system that could:
- Accurately **track shuttlecock (cork)** movements across a badminton court.
- **Identify point-scoring events** based on the cork's location and speed.
- Provide **visual overlays and statistical insights** to support decision-making.
- Work in **real-time or near-real-time settings** with high performance.

This project was undertaken as part of my professional training and responsibilities with iCore, and involved full-cycle development: from data collection and preprocessing to model training, evaluation, and integration.

---

## ✨ Key Features

- 🚀 **Real-Time Detection & Tracking**  
  Processes live match feeds or recorded footage and detects key events frame-by-frame.

- 🏸 **Shuttlecock Detection (YOLOv4)**  
  Uses a custom-trained YOLOv4 model capable of identifying shuttlecocks even during high-speed gameplay.

- 🧠 **Trajectory Estimation (TrackNet)**  
  Implements TrackNet architecture to predict the shuttlecock's path and determine where it lands.

- 📏 **Boundary Mapping & Court Calibration**  
  Uses homography and court keypoint mapping to check if the cork landed inside valid scoring zones.

- 🧍 **Player Tracking (optional)**  
  Tracks the movement of individual players for positioning and strategy insights.

- 📊 **Event Annotation & Statistics**  
  Overlays match information like rally count, serve direction, and current scores.

---

## 🧠 System Design & Flow

```text
           [ Live/Recorded Match Footage ]
                          ↓
             [ Frame-by-Frame Extraction ]
                          ↓
                ┌────────────────────────┐
                │ YOLOv4 Shuttle Detection│
                └────────────────────────┘
                          ↓
                ┌────────────────────────┐
                │ TrackNet Trajectory Estimation │
                └────────────────────────┘
                          ↓
             [ Court Zone & Net Calibration ]
                          ↓
           [ Point Validity Inference & Stats ]
                          ↓
        [ Annotated Video Output + Match Data ]

# 📹 How It Works – End-to-End

## Preprocessing:
- Input video is broken down into frames.
- Frame dimensions are standardized.

## YOLO Detection:
- Each frame is passed to a YOLOv4 model.
- If a shuttlecock is detected, its coordinates are stored.

## Trajectory Estimation (TrackNet):
- Sequential frames are analyzed to estimate trajectory and cork speed.
- Prediction is made about the cork's next location.

## Point Determination:
- Based on trajectory end point and court calibration, the system checks if the cork is “in” or “out”.
- Point is assigned to the respective player.

## Overlay & Output:
- Visual feedback like bounding boxes, trajectory lines, and scores are drawn.
- Final annotated video is exported.

# 📈 Improvements & Future Work

- ⚙️ **Automated Net Detection** for full-court calibration from any camera angle.
- 🕵️ **Multi-angle Fusion** using dual-camera input to improve occlusion scenarios.
- 📲 **Web-based Dashboard** to live-stream scores, analysis, and video feed.
- 🤖 **Deep Learning Upgrade**: Integrate transformer-based trackers for better temporal understanding.
- 📦 **Plug-and-Play Hardware Kits** for live match installations.

# 🚫 Code Access
Due to non-disclosure and intellectual property clauses signed with iCore Technologies, the codebase, trained weights, and datasets used for this project cannot be shared. This README serves only as documentation of the work and system capabilities.

If you are interested in learning more or seeing a demonstration, please contact iCore Technologies directly.
