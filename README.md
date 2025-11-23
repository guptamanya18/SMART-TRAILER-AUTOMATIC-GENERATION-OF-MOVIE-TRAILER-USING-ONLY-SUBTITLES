# 🎬 Smart Trailer

### Automated Movie Trailer Generation Using Only Subtitles

Welcome to **Smart Trailer**, an AI‑powered Python project that generates cinematic trailers using **only subtitle (.srt) files** — no original video required.

This tool extracts powerful lines, converts them into dramatic narration, and assembles a complete trailer using text‑based visuals or optional stock footage.

---

## ⭐ Features

* ✨ Works **only from subtitles**
* 🧠 Intelligent line selection (embeddings + heuristics)
* 🎤 Automatic narration via TTS
* 🎞️ Trailer assembly with cinematic title cards
* 🎛️ Fully customizable visuals & audio

---

## 📁 Repository Structure

```
smart-trailer/
├─ README.md
├─ requirements.txt
├─ LICENSE
├─ .gitignore
├─ example_data/
│  ├─ sample.srt
│  └─ stock_clips/
├─ src/
│  ├─ main.py
│  ├─ subtitle_parser.py
│  ├─ highlight_selector.py
│  ├─ tts.py
│  ├─ video_assembler.py
│  └─ utils.py
└─ demo.ipynb
```

---

## ⚙️ Installation

```
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

## 🚀 How It Works

1. Parse subtitles (timings + dialogue)
2. Score lines for emotional and narrative impact
3. Convert selected lines to narration (TTS)
4. Build trailer using title cards or stock clips
5. Export final MP4 video

---

## ▶️ Usage

```
python src/main.py --srt example_data/sample.srt --out trailer.mp4
```

**Optional flags:**

```
--max_duration   Max trailer length (default 60 seconds)
--temp_dir       Directory for intermediate audio files
```

---

## 🧩 Highlight Selection Algorithm

Uses:

* Sentence embeddings (MiniLM)
* Heuristics: punctuation, length, intensity
* Greedy duration‑based selection

This produces a flowing, dramatic trailer sequence.

---

## 🎧 Text‑to‑Speech

Default engine: **gTTS**
You may replace it with:

* Coqui TTS
* Azure / Google Cloud TTS
* ElevenLabs

Modify `tts.py` to customize.

---

## 🎞️ Video Assembly

**MoviePy** handles:

* Title cards
* Audio synchronization
* Smooth transitions
* MP4 rendering

---

## 📌 Example Trailer Timeline

```
[Opening Title Card]
[Highlighted Dialogue Line]
[Emotional or Climactic Line]
[Final Outro / Movie Title]
```

---

## 🛠️ Requirements

```
pysrt
moviepy
nltk
sentence-transformers
transformers
gTTS
numpy
python-dotenv
```

---

## 💡 Future Enhancements

* Scene extraction from real video
* Cinematic color grading
* Better emotion‑scoring ML model
* Background music detection & ducking

---

## 📜 License

Licensed under the **MIT License**.

---

## 🙌 Contributions

PRs, issues, and suggestions are welcome!
