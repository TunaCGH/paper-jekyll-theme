---
layout: content
title: Projects
permalink: /projects/
---

# Content menu..
## 1. Project Introduction
# Objective

This project aims to build a system that detects employee attention levels based on input from a webcam or surveillance camera. The system distinguishes between:

 ` Open eyes `

 ` Closed eyes `

 ` Only hair visible ` the person is likely resting their head on the desk (asleep).


Motivation

- In both remote and on-site work environments

- Monitoring focus and attention is crucial.

- Applied in online classrooms or e-learning platforms.

## 2. Problem Statement

- Input: Images.

- Output: A label classifying the person’s state as either ` open eyes `, ` closed eyes `, or ` only hair `.

# Challenges

- Real-world variations such as different head angles, lighting conditions, obstructions (e.g., hair, glasses, masks).

- The model needs to be sensitive enough to make accurate predictions but also robust to noise.

## 3. Development Roadmap
# Problem Analysis

- Define the key visual cues for each state.

- Identify common scenarios in an office or working environment.

- Determine whether full-face detection is necessary or just upper face (eye region).

# Data Collection & Preprocessing

- Open datasets, from available Kaggle dataset source, include `open and closed eye`, ` and hair style `

- Preprocessing
Face detection using HaarCascade, MTCNN, or Dlib.

Resize images to a uniform shape (e.g., 224x224).

Normalize pixel values (0–1) or standardize.

Augmentation:

Rotation (±15°)

Brightness adjustment

Zoom in/out

Horizontal flip
- [Awesome Project]()đsf


# Talks
- How to ????

