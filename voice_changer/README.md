# Voice Changer

This directory contains a simple example of a streaming voice changer that uses open-source voice conversion models. The `streaming.py` script captures microphone audio, converts it to a target timbre, and plays the result in real time.

## Setup

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Download or train an open-source voice conversion model (e.g. [RVC](https://github.com/ylzz1/voice-changer), [so-vits-svc](https://github.com/svc-develop-team/so-vits-svc), or [SpeechT5](https://huggingface.co/microsoft/speecht5_vc)).

## Usage

Run the streaming voice changer with a path to your pretrained model:

```bash
python voice_changer/streaming.py --model path/to/model.pth
```

The script uses `sounddevice` to read from the default microphone and output to the default speakers. The `VoiceConverter` class contains placeholders for loading and running the chosen voice conversion model.

You can extend `VoiceConverter._load_model` and `VoiceConverter.convert` to integrate any compatible open-source model.
