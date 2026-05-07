# VSDSquadron PRO Internship



## Task 1 – Hardware Setup & Validation (VSDSquadron PRO)



---



## Objective



The objective of this task is to:



- Install and configure the RISC-V development environment



- Validate hardware functionality using the VSDSquadron PRO board



- Upload and execute a basic program



- Understand hardware specifications



- Document the complete setup process clearly



This task forms the foundation for further Edge AI and embedded systems development.



---



## Overview



This repository documents the complete setup and validation of the VSDSquadron PRO RISC-V board.



## Contents
- [Installation Guide](installation_guide.md)
- [System Configuration](system_config.md)
- [Commands Used](commands_used.md)
- [Hardware Summary](hardware_summary.md)
- [issues_faced](issues_faced.md)
- [Screenshots](screenshots/)

---

## Board Used
VSDSquadron PRO (SiFive based RISC-V board)

---


## Screenshots

### Driver Installation
![Driver](screenshots/driver.jpg)

### Setup Process
![Setup](screenshots/setup.jpg)

### Debug Session
![Debug](screenshots/debug.jpg)

### Output / Execution
![Output](screenshots/output.jpg)

### Hardware Setup
![Board](screenshots/board.jpg)


---

# Task 2 – Embedded AI Model for Handwritten Digit Recognition
# BitNet-like Quantized MNIST Classification on VSDsquadron PRO

This project demonstrates deployment of a quantized handwritten digit recognition model on the VSDsquadron PRO board powered by the SiFive FE310-G002 RISC-V microcontroller.

The implementation uses TensorFlow Lite generated model parameters integrated with Embedded C for lightweight AI inference on resource-constrained hardware.

---

# Aim

The aim of this project is to implement and deploy a handwritten digit recognition system on embedded RISC-V hardware using quantized neural network techniques.

This project demonstrates:

- AI model deployment on embedded systems
- Quantized inference using TensorFlow Lite
- Embedded C integration
- RISC-V based hardware acceleration
- Real-time digit prediction on VSDsquadron PRO

---

# Features

- Quantized MNIST handwritten digit recognition
- TensorFlow Lite model conversion
- Embedded C based inference engine
- RISC-V compatible implementation
- Lightweight execution on VSDsquadron PRO
- Real-time serial output prediction

---

# Hardware Used

- VSDsquadron PRO Board
- SiFive FE310-G002 RISC-V MCU
- USB Type-C Cable
- Windows Laptop

---

# Software Requirements

### Freedom Studio 3.1.1
IDE used for RISC-V embedded development and debugging.

### Python 3.x
Used for model conversion and parameter generation.

### Python Libraries

```bash
pip install tensorflow numpy matplotlib jupyter
```

---

# Project Structure

```text
sifive_hifive1_BitNet_MNIST_App/

├── src/
│ ├── main.c
│ ├── app_inference.h
│ ├── mnist_model_data.h
│ ├── mnist_model_params.c
│ ├── mnist_model_params.h
│ └── generate_c_model_params.py
│
├── mnist_baseline_model.ipynb
├── mnist_quantized_model.tflite
├── Makefile
└── README.md
```

---

# Getting Started

## 1. Install Freedom Studio

Install Freedom Studio and required drivers for VSDsquadron PRO board.

---

## 2. Setup Python Environment

Install Python and required libraries:

```bash
pip install tensorflow numpy matplotlib jupyter
```

---

## 3. Generate C Model Parameters and Sample Inputs

The notebook trains and quantizes the MNIST model and converts it into TensorFlow Lite format.

### Run Jupyter Notebook

Open and execute:

```text
mnist_baseline_model.ipynb
```

This generates:

```text
mnist_quantized_model.tflite
```

---

## 4. Run Parameter Generation Script

Navigate to the source directory and execute:

```bash
python generate_c_model_params.py
```

This generates:

- mnist_model_params.c
- mnist_model_params.h

These files contain:

- Quantized weights
- Bias values
- Scale factors
- Sample input images
- Digit labels

---

# Build the Embedded Application

## Step 1: Open Project

Open Freedom Studio and import the project.

---

## Step 2: Clean Project

Go to:

```text
Project → Clean
```

Select your project and clean it.

---

## Step 3: Build Project

Go to:

```text
Project → Build Project
```

Expected Result:

```text
Build Finished with 0 errors
```

---

# Configure and Run on VSDsquadron PRO

## Connect Board

Connect the VSDsquadron PRO board using USB Type-C cable.

---

## Configure Debug Session

Go to:

```text
Run → Debug Configurations
```

Select:

```text
GDB OpenOCD Debugging
```

Ensure correct executable path is selected.

---

## Start Debugging

Click:

```text
Debug
```

Program will load into hardware memory.

---

## Run Application

Press the Resume/Run button.

The serial terminal displays prediction outputs.

---

# Output

Example terminal output:

```text
BitNet MNIST Dataset Handwritten Digit Classification

Inference of Sample 1 -> Prediction: 7
Inference of Sample 2 -> Prediction: 2
Inference of Sample 3 -> Prediction: 0
Inference of Sample 4 -> Prediction: 5
```

This confirms successful deployment and execution on RISC-V hardware.

---

# Model Details

The model is a quantized neural network trained using TensorFlow/Keras on the MNIST handwritten digit dataset.

### Architecture

- Input Layer: 28x28 grayscale image
- Hidden Layer: Dense layer with ReLU activation
- Output Layer: 10-class digit prediction

### Quantization

- 8-bit integer quantization
- Reduced memory footprint
- Faster embedded execution

---

# Troubleshooting / Common Issues

### Python Not Configured

Configure Python interpreter in Freedom Studio preferences.

---

### OpenOCD Connection Failed

Check:

- USB connection
- Driver installation
- COM port availability

---

### Build Errors

Ensure:

- Correct project imported
- All source files present
- Python libraries installed

---

### Debug Session Issues

Verify:

- Correct executable selected
- Board connected properly
- OpenOCD configuration correct

---

# Learning Outcomes

Through this project, I learned:

- Embedded AI deployment
- TensorFlow Lite integration
- Quantized neural networks
- RISC-V debugging workflow
- Embedded C programming
- Freedom Studio configuration

---

# Conclusion

This project successfully demonstrates deployment of a quantized handwritten digit recognition model on VSDsquadron PRO using RISC-V architecture and embedded AI techniques.
