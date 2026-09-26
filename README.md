# Qwen3-ASR

**Demo — transcribe audio to text in Colab (Qwen3-ASR).**

Not a client case study. A short pipeline: audio in → 16 kHz mono → model → `transcription.txt`. GPU (T4) recommended.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/47096/qwen3-asr/blob/main/qwen3-asr.ipynb)

---

## Run it

1. Click **Open In Colab** · **Runtime → T4 GPU**  
2. Run all cells (English sample loads by default)  
3. Swap in your file, or use `sample-voice/chinese-sample-voice.wav`  

**Privacy:** audio is processed in Colab / Hugging Face — don’t upload confidential calls.

## Five commercial use cases

| # | Use case | Who cares |
|---|----------|-----------|
| 1 | **Subtitle drafts** | Marketing / video |
| 2 | **Call / support transcripts** | CX analytics |
| 3 | **Meeting minutes** | Ops / exec assistants |
| 4 | **Podcast → show notes** | Media |
| 5 | **Voice → searchable text** | Knowledge / CRM |

## Five personal use cases

| # | Use case |
|---|----------|
| 1 | Lecture / interview notes |
| 2 | Podcast bookmarking |
| 3 | Language practice (listen + read) |
| 4 | Accessibility: speech → text |
| 5 | Archive voice memos as text |

## What it does

```text
Audio file → resample 16 kHz mono → Qwen3-ASR → text file
```

| Model | Size | Best for |
|-------|------|----------|
| `Qwen/Qwen3-ASR-0.6B` | 0.6B | Fast, Colab T4 |
| `Qwen/Qwen3-ASR-1.7B` | 1.7B | More accuracy / VRAM |

Optional: `return_time_stamps=True` for word timings.

## Repo

| Path | Role |
|------|------|
| `qwen3-asr.ipynb` | Full Colab walkthrough |
| `sample-voice/*.wav` | English / Chinese samples |

**Stack:** `qwen-asr` · `librosa` · `soundfile` · Colab GPU

---

*Speech demos: [`lux-tts`](https://github.com/47096/lux-tts) (clone) · [`qwen3-tts-voice-clone`](https://github.com/47096/qwen3-tts-voice-clone) · products: [`mimo-reader`](https://github.com/47096/mimo-reader) · [datafying](https://datafying.co/)*
