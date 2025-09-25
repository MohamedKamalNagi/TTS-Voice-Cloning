🎙️ Voice Cloning with XTTS v2

This project demonstrates multilingual text-to-speech (TTS) with voice cloning using the Coqui TTS
 library and the XTTS v2 model.

It allows you to:

Clone a voice from a sample audio file (input.wav).

Generate speech in multiple languages.

Save the output to a .wav file.

🚀 Features

✅ Voice cloning from a reference audio file.

✅ Support for multilingual TTS.

✅ GPU acceleration with CUDA if available.

✅ Save generated speech to an audio file.

📦 Installation

Clone this repository:

git clone https://github.com/your-username/voice-cloning-xtts.git
cd voice-cloning-xtts


Create a virtual environment (recommended):

python -m venv venv
venv\Scripts\activate   # On Windows
source venv/bin/activate   # On Linux/Mac


Install dependencies:

pip install torch torchvision torchaudio
pip install TTS

▶️ Usage

Place your reference voice file in the project folder (e.g., input.wav).

Run the script:

python d.py


The cloned speech will be saved as:

output.wav

📝 Example
tts.tts_to_file(
    text="Hello, this is a voice cloning test. Nice to meet you!",
    file_path="output.wav",
    speaker_wav=["input.wav"],
    language="en",
    split_sentences=True
)

📂 Project Structure
├── d.py              # Main script (voice cloning example)
├── input.wav         # Reference speaker audio (provide your own)
├── output.wav        # Generated speech
├── README.md         # Documentation

⚡ Notes

Make sure input.wav is a clear voice recording (mono, 16kHz preferred).

Use CUDA for faster inference if available.

You can change language="en" to "ar", "fr", "de", etc.

🤝 Credits

Coqui TTS

PyTorch
