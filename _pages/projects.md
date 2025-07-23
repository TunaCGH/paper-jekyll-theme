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

- Open datasets, from available Kaggle dataset source, include [open and closed eye](https://www.kaggle.com/datasets/tauilabdelilah/mrl-eye-dataset),  [and hair style](https://www.kaggle.com/datasets/kavyasreeb/hair-type-dataset).

- Preprocessing
  
- Adjust the input

~~~Python
# Create the array of the right shape to feed into the keras model
# The 'length' or number of images you can put into the array is
# determined by the first position in the shape tuple, in this case 1
data = np.ndarray(shape=(1, 224, 224, 3), dtype=np.float32)

# Replace this with the path to your image
image = Image.open("<IMAGE_PATH>").convert("RGB")

# resizing the image to be at least 224x224 and then cropping from the center
size = (224, 224)
image = ImageOps.fit(image, size, Image.Resampling.LANCZOS)

# turn the image into a numpy array
image_array = np.asarray(image)

# Normalize the image
normalized_image_array = (image_array.astype(np.float32) / 127.5) - 1

# Load the image into the array
data[0] = normalized_image_array

~~~
- Predicting process
~~~Python
# Predicts the model
prediction = model.predict(data)
index = np.argmax(prediction)
class_name = class_names[index]
confidence_score = prediction[0][index]
~~~

# 4. Technologies Used
` keras ` model 
Library, include : ` tensorflow `, ` keras `,...
Code editor... `visual studio code`

# 5. Results
Overall accuracy: 


Class-wise performance:

Open eyes: 92%

Closed eyes: 88%

Head down: 85%

# 6. Limitations & Improvements
Limitation
- Misclassification with glasses
- Head-down face not visible
- Poor lighting affects accuracy

# 7. Real-world Applications
Workplace: Help managers monitor attention levels non-invasively.

Education: Detect students falling asleep in online classes.

Self-learning: Provide feedback to learners who lose focus (e.g., beep alert after inactivity).


