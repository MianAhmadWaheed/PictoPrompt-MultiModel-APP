# PictoPrompt-MultiModel-APP 
I just deployed a proof-of-concept app that lets you ask questions about any image using your voice – and get both text and spoken answers in return!
🔹 Speech-to-Text with Whisper
🔹 Visual Question Answering using BLIP-2 + Flan-T5
🔹 Text-to-Speech with gTTS
🔹 Built with Gradio + Hugging Face
Try it out and let me know what you think!


**Ask-the-Image** is a proof-of-concept multimodal mini-app that allows users to ask questions about an uploaded image using their **voice**, and receive answers in both **text and spoken audio**. This project showcases the integration of **speech recognition**, **vision-language models**, and **text-to-speech synthesis** in one lightweight app.

## Features

- **Speech-to-Text**: Speak your question (max 10s), transcribed using OpenAI's Whisper-small ASR model.
- **Image Question Answering**: Upload or capture an image. The app uses BLIP-2 + Flan-T5-small to understand and answer your question.
- **Text-to-Speech**: The generated answer is rendered on-screen and spoken back using Google Text-to-Speech (gTTS).
- **Modular Design**: Code is split into reusable modules – `asr.py`, `qa.py`, `tts.py`, and `app.py`.

## Tech Stack
- Python, PyTorch, Hugging Face Transformers

## How to Run Locally

1. **Clone the repo**

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Run the app**

```bash
python app.py
```

4. Open the link provided by Gradio in your browser.

## 🗂️ File Structure

```
ask-the-image/
├── app.py         # Gradio interface and orchestrator
├── asr.py         # Audio transcription using Whisper
├── qa.py          # Image QA using BLIP-2 + Flan-T5
├── tts.py         # Text-to-Speech using gTTS
└── requirements.txt
```

## 📷 Example Use Case

1. Upload an image (e.g., a traffic scene).
2. Ask: "How many cars are in the image?" using your mic.
3. The app will display and **speak** the answer.
