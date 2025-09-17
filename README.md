# Automated-movement-detection-and-Biomechanical-Analysis
This project applies ‘pose estimation’ (MediaPipe) and signal processing to detect and analyze goblet squat repetitions from video. It is designed for sports performance analysis, rehabilitation monitoring, and as a demonstration of combining biomechanics with computer vision.
## Features
- Extracts knee joint angles using MediaPipe.
- Cleans noisy pose-estimation data with:
  - NaN handling,
  - short-gap interpolation,
  - zero-phase smoothing (no lag).
- Detects squat repetitions using:
  - peaks, troughs, and velocity zero-crossings,
  - minimum concentric duration rules.
- Outputs per-rep metrics:
  - start, bottom, end timestamps,
  - range of motion (ROM),
  - concentric phase duration.
- Saves results to CSV and visualizes reps on angle–time plots.

## Dependencies
mediapipe, opencv-python, numpy, pandas, matplotlib

- Example Output

| rep | start\_s | bottom\_s | end\_s | ROM\_deg | duration\_s | concentric\_s |
| --- | -------- | --------- | ------ | -------- | ----------- | ------------- |
| 1   | 1.2      | 2.0       | 2.9    | 85.2     | 1.7         | 0.9           |
| 2   | 4.5      | 5.3       | 6.2    | 87.5     | 1.7         | 0.9           |
| 3   | 7.1      | 7.9       | 8.7    | 86.8     | 1.6         | 0.8           |
