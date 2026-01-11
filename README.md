# Pedestrian Detection System

A real-time pedestrian detection system designed for automotive safety applications. The system uses a Raspberry Pi 4, an Anker 2K USB camera, and a Google Coral Edge TPU to detect pedestrians approximately 20 feet in front of a vehicle and provide an audible alert via a buzzer.

The project leverages Edge Impulse for machine learning model training, optimization, and deployment, enabling low-latency, on-device inference.

---

## Project Overview

This project demonstrates a complete embedded AI pipeline: data collection, model training, edge deployment, and real-time inference. The system continuously analyzes camera input to detect pedestrians and triggers a warning buzzer when a pedestrian is detected within a defined forward range.

---

## Key Features

- Real-time pedestrian detection
- Approximately 20 ft forward detection range
- Edge TPU–accelerated inference
- Low-latency, on-device AI processing
- Audible alert via buzzer
- Optimized using Edge Impulse

---

## System Architecture

### Hardware Components
- Raspberry Pi 4 (main controller)
- Anker 2K USB camera (visual input)
- Google Coral USB Accelerator (Edge TPU)
- Active buzzer (alert output)

### Software Stack
- Raspberry Pi OS
- Edge Impulse Linux SDK
- TensorFlow Lite (Edge TPU)
- Python-based inference pipeline

---

## Vision and Detection Pipeline

1. Camera captures video frames
2. Frames are preprocessed for the model
3. Edge TPU performs accelerated inference
4. Pedestrian confidence score evaluated
5. If confidence exceeds threshold:
   - Buzzer is activated
   - Detection event recorded

---

## Model Training and Deployment

**Training Platform:** Edge Impulse  
**Model Type:** Vision-based pedestrian detection model

### Workflow
1. Collect pedestrian and non-pedestrian images
2. Label dataset using Edge Impulse Studio
3. Train and optimize the model
4. Quantize the model for Edge TPU execution
5. Deploy the optimized model to the Raspberry Pi

---

## Alert Logic

- Detection confidence threshold is configurable
- Debounce logic reduces false positives
- Alerts only trigger when pedestrians are detected directly ahead

---

## Performance Considerations

- Low inference latency due to Edge TPU acceleration
- Real-time processing suitable for automotive scenarios
- Edge-based deployment avoids cloud dependency

---

## Future Improvements

- Distance estimation using monocular vision
- Visual indicators or HUD integration
- Multi-class detection (cyclists, vehicles)
- Sensor fusion with ultrasonic or radar systems
- Integration with vehicle control systems

---

## Tools and Technologies

- Raspberry Pi 4
- Google Coral Edge TPU
- Edge Impulse
- Python
- TensorFlow Lite
