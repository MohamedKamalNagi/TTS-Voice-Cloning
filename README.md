🎙️ Voice Cloning with XTTS v2








This project demonstrates multilingual text-to-speech (TTS) with voice cloning using the Coqui TTS
 library and the XTTS v2 model.

With just one reference audio sample, you can generate natural-sounding speech in multiple languages.

✨ Features

🎤 Voice Cloning – Clone a voice from a short audio recording (input.wav).

🌍 Multilingual TTS – Generate speech in English, Arabic, French, German, and more.

⚡ Fast Inference – Runs on GPU (CUDA) if available.

💾 File Output – Save generated audio directly as .wav.

📂 Project Structure
voice-cloning-xtts/
│── Voice_Cloning.py              # Main script (voice cloning example)
│── input.wav         # Reference audio (speaker voice sample)
│── output.wav        # Generated speech
│── requirements.txt  # Dependencies
│── README.md         # Documentation

📦 Installation
1️⃣ Clone this repo
git clone (https://github.com/MohamedKamalNagi/TTS-Voice-Cloning)
cd voice-cloning-xtts

2️⃣ Create a virtual environment
python -m venv venv
venv\Scripts\activate   # On Windows
source venv/bin/activate   # On Linux/Mac

3️⃣ Install dependencies
pip install -r requirements.txt

▶️ Usage

Place your reference audio as input.wav in the project folder.

Use a clear recording (mono, 16kHz preferred).

Run the script:

python Voice_Cloning.py


The generated cloned voice will be saved as:

output.wav

📝 Example Code
tts.tts_to_file(
    text="Hello, this is a voice cloning test. Nice to meet you!",
    file_path="output.wav",
    speaker_wav=["input.wav"],
    language="en",
    split_sentences=True
)


You can change the language by modifying language="en" to "ar", "fr", "de", etc.

⚡ Tips

✅ Use CUDA GPU if available (device = "cuda") for faster generation.

✅ Test different reference audios for better cloning quality.

✅ Try longer texts with split_sentences=True for smoother audio.

🤝 Credits

Coqui TTS

PyTorch
