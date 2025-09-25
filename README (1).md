# Voice Cloning with XTTS v2

This project demonstrates **voice cloning** using the [Coqui TTS](https://github.com/coqui-ai/TTS) library with the **XTTS v2** multilingual text-to-speech model.  
It allows you to generate speech from text while cloning a target speaker’s voice using a sample audio file.

---

## ✨ Features
- 🎙️ **Voice Cloning**: Generate speech that mimics the style of a reference speaker audio.  
- 🌍 **Multilingual Support**: Supports multiple languages including English.  
- ⚡ **GPU Acceleration**: Automatically runs on CUDA if available.  
- 📄 **Export to File**: Saves output audio as `.wav`.

---

## 🚀 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/voice-cloning-xtts.git
   cd voice-cloning-xtts
   ```

2. **Create a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # For Linux/Mac
   venv\Scripts\activate      # For Windows
   ```

3. **Install dependencies**:
   ```bash
   pip install torch
   pip install TTS
   ```

---

## ▶️ Usage

1. Place your **reference audio file** (e.g., `.wav` or `.mp3`) inside the project folder.  
   Example: `voice_sample.mp3`

2. Run the script:
   ```bash
   python main.py
   ```

3. The cloned voice audio will be saved as:
   ```
   output4.wav
   ```

---

## 📝 Example Code

```python
import torch
from TTS.api import TTS
from TTS.tts.configs.xtts_config import XttsConfig, XttsAudioConfig, XttsArgs
from TTS.config.shared_configs import BaseDatasetConfig
from torch.serialization import add_safe_globals

# Allow PyTorch to trust XTTS config classes during checkpoint loading
add_safe_globals([XttsConfig, XttsAudioConfig, BaseDatasetConfig, XttsArgs])

# Device setup
device = "cuda" if torch.cuda.is_available() else "cpu"

# Load model
tts = TTS("tts_models/multilingual/multi-dataset/xtts_v2").to(device)

# Generate cloned voice
tts.tts_to_file(
    text="i was made by mohamed kamal and mohamed hossam and marwan gamal and filopater hany",
    file_path="output4.wav",
    speaker_wav=["./voice_sample.mp3"],  # Replace with your file path
    language="en",
    split_sentences=True
)
```

---

## 📂 Project Structure
```
voice-cloning-xtts/
│── main.py          # Main script
│── README.md        # Documentation
│── requirements.txt # Dependencies
│── voice_sample.mp3 # Example speaker audio
│── output4.wav      # Generated output
```

---

## 📌 Requirements

- Python 3.8+
- PyTorch
- [Coqui TTS](https://github.com/coqui-ai/TTS)

---

## 👨‍💻 Credits
- Developed by **Mohamed Kamal, Mohamed Hossam, Marwan Gamal, and Filopater Hany**.  
- Powered by [Coqui TTS](https://github.com/coqui-ai/TTS).
