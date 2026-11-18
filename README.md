<div align="center">
🎹 Typing Rhythm Piano

A Python music app that turns your keyboard typing into a song, with a live Pygame visualizer

Python Pygame NumPy Show Image Show Image

</div>
📖 Overview

Typing Rhythm Piano is a desktop application that turns every key you press into a musical note. The way you type shapes the music: type fast and the song becomes bright and happy, type slowly and it turns calm and moody. When you finish, your session is saved as a real MIDI file and a WAV file that you can play anywhere.

It is built to demonstrate Python programming, sound synthesis with NumPy, event-driven GUI development with Pygame, and file handling with MIDI and WAV formats.

🖼️ Screenshots
<!-- Add screenshots here once available. Suggested layout: | Idle Screen | Live Performance | |-------------|------------------| | ![Idle](assets/screenshots/idle.png) | ![Live](assets/screenshots/live.png) | A short GIF of typing and the colorful bars falling works even better than static images. -->

Screenshots coming soon. See the Getting Started section to run it yourself in the meantime.

✨ Features
⌨️ Typing to Music
Every letter a-z plays a melody note
Every digit 0-9 plays a lower note, so digits never clash with letters
All notes are generated live with NumPy (no audio files needed)
🎼 Smart Musical Mood
Fast typing (3.5+ keys per second) switches to a bright major scale
Slower typing uses a moody minor scale
A bass note is added automatically on every 8th key
🎛️ Instruments
5 built-in instruments: Piano, Synth, Bell, Saw and Drum
Switch instrument any time with F1 to F5
📊 Live Dashboard
Colorful falling bars for every note you play
Recent input display
Live stats: keys played, typing speed (WPM), rhythm score and session time
💾 Export
Save your session as a .mid file (opens in any music software)
Save your session as a .wav file (plays in any media player)
🎮 Controls
Key	Action
a-z, 0-9	Play notes
F1	Piano
F2	Synth
F3	Bell
F4	Saw
F5	Drum
F6	Save session
ESC	Save and exit
🛠️ Tech Stack
Layer	Technology
Language	Python
GUI and Sound Playback	Pygame
Sound Synthesis	NumPy
MIDI Export	Mido
WAV Export	wave (built-in)
Other	colorsys, collections, datetime, time, os
📁 Project Structure
text
typing-rhythm-piano/
├── typing_piano.py     # Main application (sound, GUI and export)
├── requirements.txt    # Python dependencies
├── README.md           # Project documentation
├── LICENSE             # MIT License
├── .gitignore          # Files Git should ignore
└── songs/              # Saved sessions (created automatically)
🚀 Getting Started
Prerequisites
Python 3.8+
A speaker or headphones
1. Clone the repository
bash
git clone https://github.com/<your-username>/typing-rhythm-piano.git
cd typing-rhythm-piano
2. Install dependencies
bash
pip install -r requirements.txt
3. Run the app
bash
python typing_piano.py

Click the window, then start typing. Your saved sessions appear in the songs/ folder as session_YYYYMMDD_HHMMSS.mid and .wav.

🧠 How It Works
Sound generation: each note is synthesized with NumPy using sine, square or saw waves and a decay envelope, then played with pygame.mixer.
Note mapping: every key maps to a position on a musical scale, so the same key always gives the same note in the same mode.
Mood detection: the app counts the keys pressed in the last 3 seconds to choose between major and minor.
Rhythm score: calculated from how even the gaps are between your last 20 key presses. A steadier rhythm gives a higher score.
Export: events are written to a MIDI file with Mido and mixed down into a WAV file.
🗺️ Roadmap / Future Improvements
[ ] Map space and backspace to drum hits
[ ] Choose scale and key from a menu
[ ] Faster startup by loading instruments in the background
[ ] Record and replay mode
[ ] Support for symbols and punctuation keys
[ ] Make WAV and MIDI note lengths match exactly
🤝 Contributing

This started as a college project, but suggestions and pull requests are welcome. Feel free to open an issue if you spot a bug or have an idea for improvement.

📄 License

This project is licensed under the MIT License.

<div align="center"> Made with Python & 🎵 by <strong>Pushkar Mishra</strong> </div>
