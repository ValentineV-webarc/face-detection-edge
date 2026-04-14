# Face Detection Edge Deployment

Real-time face detection pipeline using deep learning, exported to ONNX format for edge deployment. Achieves 65+ FPS on CPU with live footfall counting and CSV logging.

## Demo
- Detects multiple faces in real-time via webcam
- Displays confidence score per face
- Logs face count + FPS per frame to CSV — simulating edge-based footfall analytics

## Pipeline
` ` `
OpenCV DNN (ResNet-10 SSD)
        ↓
ONNX Export (MobileNetV2)
        ↓
ONNX Runtime Inference
        ↓
Live Webcam — 65 FPS, Multi-face, CSV Logging
` ` `

## Why ONNX?
ONNX enables models to run on optimized edge runtimes targeting ARM and NPU accelerators — directly relevant to edge AI chips. No cloud dependency, no heavy framework at inference time.

## Tech Stack
- Python, Jupyter Notebook
- OpenCV DNN module
- PyTorch + TorchVision (MobileNetV2)
- ONNX + ONNX Runtime
- Matplotlib

## Results
| Metric | Value |
|---|---|
| FPS (CPU) | 65.6 |
| Confidence Score | 0.96 |
| Faces Detected | Multi-face |
| Edge Ready | ONNX |

## Setup
```bash
pip install opencv-python torch torchvision onnx onnxruntime onnxscript matplotlib
jupyter notebook FaceDetection.ipynb
```

## Author
**Valentine** — Information Engineering and Media Student, NTU Singapore
