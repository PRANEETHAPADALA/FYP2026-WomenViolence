AI-Based Context-Aware Threat Detection System for Women’s Safety
Overview

This project presents a low-resource, context-aware artificial intelligence framework designed for real-time threat prediction in women’s safety surveillance environments.

The system integrates three AI modules:

Gender-based contextual risk analysis

Violence detection through temporal action recognition

Emotion-based distress assessment

A final integrated threat score is computed by fusing outputs from all modules.

Final Threat Score Formula
S_final = 0.5 * S_action + 0.3 * S_gender + 0.2 * S_emotion
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
Violence Detection Model (Large File)

Download the trained model from:

https://drive.google.com/file/d/1tnrUjs5TLbIJHBIl3bHOk6uaCaBXlk5e/view?usp=sharing

After downloading:

Rename to: final_violence_model.zip
Place it in the same directory as Finalcodev1.txt
Installation
pip install torch torchvision transformers tensorflow opencv-python scipy pillow
Run the Project
python Finalcodev1.txt

Or in a notebook:

main_pipeline()
