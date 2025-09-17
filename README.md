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
| 1   | 2.633    | 4.0       | 6.167  | 137.7     | 3.533       | 2.167           |
| 2   | 6.2      | 7.567     | 9.533  | 138.9     | 3.33        | 1.967           |
