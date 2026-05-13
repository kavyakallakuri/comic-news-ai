# 🗞️ ComicNews AI — Audio News to Comic Illustration Pipeline

An end-to-end multimodal AI pipeline that transforms any news audio into a comic-style illustrated article.

---

## 🧠 What It Does

| Step | Task | Tool |
|------|------|------|
| 1 | Download news audio from any public URL | `requests` |
| 2 | Convert & compress audio | `pydub` + `ffmpeg` |
| 3 | Transcribe speech to text | OpenAI Whisper (local) |
| 4 | Summarize & generate image prompt | Groq API — LLaMA 3 (free) |
| 5 | Generate comic illustration | Stable Diffusion (local) |
| 6 | Save full report | Python file I/O |

---

## 🚀 How to Run

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/comicnews-ai.git
cd comicnews-ai
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
apt-get install -y ffmpeg
```

### 3. Get a free Groq API key
Sign up at [groq.com](https://console.groq.com) — it's free.  
Add your key to the notebook in Step 3.

### 4. Run the notebook
Open `comicnews.ipynb` in VS Code or Google Colab and run all cells.

> ⚠️ For image generation, a GPU is recommended.  
> In Google Colab: Runtime → Change runtime type → T4 GPU

---

## 🛠️ Tech Stack

- **OpenAI Whisper** — Local speech-to-text (no API key needed)
- **Groq API** — Free LLaMA 3 inference for summarization
- **Stable Diffusion v1.5** — Local image generation (no API key needed)
- **pydub + ffmpeg** — Audio processing

---

## 💡 Key Features

- ✅ User can input **any public audio URL**
- ✅ User can choose **image style** (comic / realistic / sketch)
- ✅ **Fully free** — no paid APIs required (only Groq free tier)
- ✅ **Error handling** throughout the pipeline
- ✅ Saves a **complete report** with transcript, article, and image path
- ✅ Token count check before sending to LLM

---

## 📁 Project Structure

```
comicnews-ai/
│
├── comicnews.ipynb        ← Main notebook
├── requirements.txt       ← Python dependencies
├── README.md              ← This file
└── images/                ← Generated images saved here (auto-created)
```

---

## 🔮 Possible Extensions

- Support YouTube URLs using `yt-dlp`
- Generate multi-panel comic strips
- Build a Gradio/Streamlit web UI
- Compare outputs across LLaMA 3, Mistral, and Gemma models

---

## ⚠️ Note

This project requires a free [Groq API key](https://console.groq.com).  
Whisper and Stable Diffusion run entirely locally — no other credentials needed.
