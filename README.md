# Streaming Voice Changer

This repository demonstrates a simple streaming voice changer built with open-source tools. It can clone a speaker's timbre and convert real-time microphone input to that target voice.

## Contents
- `voice_changer/streaming.py` – example Python script for real-time voice conversion
- `voice_changer/README.md` – additional setup and usage notes
- `requirements.txt` – Python dependencies

## Quick Start

1. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Download or train an open-source voice conversion model (e.g. RVC, so-vits-svc, or SpeechT5).
3. Start the voice changer:
   ```bash
   python voice_changer/streaming.py --model path/to/model.pth
   ```

The script reads audio from the default microphone, processes it with the chosen model, and plays the converted audio through the default output device in real time.
