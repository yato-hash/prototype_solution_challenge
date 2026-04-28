# Prototype Solution
# Multimodal Fake Content Detection

## Overview
This project detects potentially misleading content by analyzing **images, audio, and video**.

## Pipeline
- **Image → OCR (Tesseract)** → extracted text
- **Audio → Speech-to-Text (Whisper)** → transcript
- **Video → Audio extraction + Whisper** → transcript
- **Scoring** → keyword-based risk score
- **Aggregation** → final decision (Likely FAKE / Suspicious / Likely REAL)

## Demo
1. Upload an image
2. Upload an audio clip
3. System generates a video with the same narrative
4. Model extracts and scores each modality
5. Final combined verdict is displayed

## Tech Stack
- Python, OpenCV, PIL
- Tesseract OCR
- OpenAI Whisper
- MoviePy

## Result
The system flags high-risk content like:
> “Breaking news… 100% guaranteed cure…”

## Future Work
- Replace keyword scoring with ML classifier
- Add deepfake detection (faces/voice)
- Build UI (Streamlit)
