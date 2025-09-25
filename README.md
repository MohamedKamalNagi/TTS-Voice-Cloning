🎙️ <span style="font-size:40px;">Voice Cloning with XTTS v2</span>








<span style="font-size:28px;">✨ Features</span>

🎤 Voice Cloning – Clone a voice from a short audio recording (input.wav).

🌍 Multilingual TTS – Generate speech in English, Arabic, French, German, and more.

⚡ Fast Inference – Runs on GPU (CUDA) if available.

💾 File Output – Save generated audio directly as .wav.

<span style="font-size:28px;">📦 Installation</span>
<span style="font-size:22px;">1️⃣ Clone this repo</span>
git clone https://github.com/your-username/voice-cloning-xtts.git
cd voice-cloning-xtts

<span style="font-size:22px;">2️⃣ Create a virtual environment</span>
python -m venv venv
venv\Scripts\activate   # On Windows
source venv/bin/activate   # On Linux/Mac

<span style="font-size:22px;">3️⃣ Install dependencies</span>
pip install -r requirements.txt

<span style="font-size:28px;">▶️ Usage</span>

Place your reference audio as input.wav in the project folder.

Run the script:

python d.py


The generated cloned voice will be saved as output.wav.

<span style="font-size:28px;">📝 Example Code</span>
tts.tts_to_file(
    text="Hello, this is a voice cloning test. Nice to meet you!",
    file_path="output.wav",
    speaker_wav=["input.wav"],
    language="en",
    split_sentences=True
)
