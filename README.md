# 🎹 Typing Rhythm Piano

**Typing Rhythm Piano** is a small Python project that turns keyboard typing into music. Every time you press a letter or number, the app plays a musical note and displays it in a live visualizer.

I built this project to experiment with Python, sound generation and Pygame. One interesting part is that the music changes depending on how quickly you type. Faster typing creates a brighter sound, while slower typing gives the music a calmer feel.

You can also change instruments while typing and save your session as MIDI or WAV files.

## 📸 Screenshots

Screenshots will be added soon.

## ✨ Features

### Typing and music
- Press any letter from A to Z to play a note.
- Numbers from 0 to 9 play lower notes.
- Notes are generated using NumPy, so no external sound files are required.
- The app responds to keyboard input in real time.

### Music changes with typing speed
- When you type at around 3.5 keys per second or faster, the app switches to a major scale.
- Slower typing uses a minor scale.
- A bass note plays after every 8 key presses.

### Instruments

There are five instruments available:

- Piano
- Synth
- Bell
- Saw
- Drum

You can switch between them using the F1 to F5 keys.

### Live display

The application also has a visualizer that shows the notes as you type.

It displays:
- Falling bars for played notes.
- Recently pressed keys.
- Total keys pressed.
- Typing speed (WPM).
- Rhythm score.
- Time spent in the session.

### Saving music

Once you're done typing, you can save your session in two formats:

- **MIDI (.mid):** Useful if you want to open or edit the music in a music production application.
- **WAV (.wav):** An audio file that you can play using a regular media player.

## 🎮 Keyboard Controls

| Key | Action |
|---|---|
| A–Z | Play musical notes |
| 0–9 | Play lower notes |
| F1 | Piano |
| F2 | Synth |
| F3 | Bell |
| F4 | Saw |
| F5 | Drum |
| F6 | Save current session |
| ESC | Save and close the application |

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Pygame | Window, graphics and sound playback |
| NumPy | Generating musical sounds |
| Mido | Creating MIDI files |
| wave | Saving audio as WAV |
| colorsys | Colour-related calculations |
| datetime, time, os | Time and file handling |

## 📁 Project Structure

```text
typing-rhythm-piano/
│
├── typing_piano.py
├── requirements.txt
├── README.md
├── LICENSE
├── .gitignore
│
└── songs/
    └── Saved MIDI and WAV files
```

The `songs` folder is created automatically when the application saves a session.

## 🚀 How to Run

### Requirements

Before running the project, make sure you have:

- Python 3.8 or above
- A working speaker or headphones
- The required Python libraries installed

### 1. Download the project

```bash
git clone https://github.com/<your-username>/typing-rhythm-piano.git
```

Move into the project folder:

```bash
cd typing-rhythm-piano
```

### 2. Install the required libraries

```bash
pip install -r requirements.txt
```

### 3. Start the application

```bash
python typing_piano.py
```

Once the window opens, click inside it and start typing.

Your saved music files will be available in the `songs` folder.

## ⚙️ How It Works

The basic idea behind this project is quite simple: keyboard input is converted into musical notes.

**Sound generation:** NumPy is used to generate audio waves. Different waveforms and a decay envelope are used to create the instrument sounds.

**Key mapping:** Each letter is assigned a note from a musical scale. Numbers are assigned lower notes.

**Changing the music:** The application checks the keys pressed during the last three seconds. Based on the typing speed, it decides whether to use a major or minor scale.

**Rhythm score:** The time gaps between recent key presses are compared to calculate how consistent the typing rhythm is.

**Saving:** Mido handles MIDI file creation, while Python's built-in `wave` module is used to save the audio as a WAV file.

## 🔧 Things I Would Like to Improve

There are still a few things I would like to add to this project:

- Add drum sounds for Space and Backspace.
- Allow users to select their own musical scale and key.
- Improve startup time.
- Add an option to record and replay a performance.
- Support symbols and punctuation marks.
- Make MIDI and WAV note durations match exactly.

## 🤝 Contributing

This project was made as part of my college work. I am still learning and experimenting with Python, so there is always room for improvement.

Suggestions and ideas are welcome!

## 📄 License

This project is available under the MIT License.

---

**Made with Python and a little music 🎵**

**Pushkar Mishra**
