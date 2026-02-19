AI-Based Context-Aware Threat Detection System for Women’s Safety
Overview

This project presents a low-resource, context-aware artificial intelligence framework for real-time threat prediction in women’s safety surveillance environments.

The system integrates three complementary AI modules:

Gender-based contextual risk analysis

Violence detection through temporal action recognition

Emotion-based distress assessment

A final integrated threat score is computed by fusing outputs from all modules to provide a unified security assessment.

System Architecture
Module 1: Gender-Based Contextual Risk Assessment

Person detection using YOLOv5

Gender classification using MobileNetV2

Multi-object tracking using Hungarian Algorithm

Dynamic crowd-aware safety logic

Output:
S_gender

Module 2: Violence Detection

VideoMAE for temporal video classification

XCLIP for action-text alignment

Adaptive thresholding for noise reduction

Action-aware probabilistic risk fusion

Output:
S_action

Module 3: Emotion Recognition

Face detection using OpenCV DNN

CNN-based emotion classification (custom trained model)

Temporal emotional deviation modeling

Dynamic distress risk computation

Output:
S_emotion

Final Threat Score Formula

S_final = 0.5 × S_action + 0.3 × S_gender + 0.2 × S_emotion

Alert Levels

S_final > 0.75 → Critical Threat

0.40 < S_final ≤ 0.75 → Suspicious Activity

S_final ≤ 0.40 → Safe

Repository Structure
FYP2026-WomenViolence/
│
├── Finalcodev1.txt
├── emotion_model.h5
├── best_mobilenet_gender_model.pth
├── README.md
Model Files
Included in Repository

emotion_model.h5

best_mobilenet_gender_model.pth

Violence Detection Model (Large File)

Due to GitHub file size limitations (files larger than 25MB), the trained violence detection model is hosted externally.

Download link:

https://drive.google.com/file/d/1tnrUjs5TLbIJHBIl3bHOk6uaCaBXlk5e/view?usp=sharing

After downloading:

Rename the file to:

final_violence_model.zip

Place it in the same directory as the main code file.

The system will automatically extract and load it during execution.

If the ZIP file is not found, the system falls back to the pretrained base model:

MCG-NJU/videomae-base-finetuned-kinetics

Requirements

Install required dependencies:

pip install torch torchvision transformers tensorflow opencv-python scipy pillow

If running in Google Colab, most dependencies are pre-installed.

How to Run
Step 1: Upload Input Video

When executed in Google Colab, the script automatically prompts for video upload.

Step 2: Run the Pipeline

Command line execution:

python Finalcodev1.txt

Or inside a notebook environment:

main_pipeline()
Output

The system generates:

final_gender_<video_name>.mp4

final_violence_<video_name>.mp4

final_emotion_<video_name>.mp4

The console prints:

S_action

S_gender

S_emotion

Final Integrated Threat Score (S_final)

Key Contributions

Multi-modal AI fusion for surveillance risk detection

Context-aware crowd-based safety modeling

Adaptive temporal risk thresholding

Integrated threat scoring framework

Low-resource compatible architecture

Academic Context

This project was developed as part of a Final Year Project (FYP 2026).

It proposes a hybrid, multi-modal threat prediction framework that integrates contextual proximity analysis, temporal action recognition, and emotional distress modeling to improve surveillance reliability.

Disclaimer

This system is developed strictly for academic and research purposes.
It is not intended to replace certified security infrastructure or law enforcement systems.
