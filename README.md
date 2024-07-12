# Caption Generator, Translator and Summarizer

Multilingual subtitle generation system that takes a YouTube video, transcribes the audio, translates to any language, and generates a summary. Built as a research project at VIT Chennai.

## What It Does

Three-stage pipeline:

1. **Transcription** — Pulls audio from a YouTube URL using `pytube`, sends it to AssemblyAI's API, and gets back a word-level timestamped transcript
2. **Translation** — Feeds the transcript through `googletrans` to translate into any of 20+ supported languages
3. **Summarization** — Runs the translated text through a T5 model (`MBZUAI/LaMini-Flan-T5-248M`) to produce a 200-word summary
4. **SRT Export** — Outputs a properly timed `.srt` subtitle file synced to the original video

## Supported Languages

English, Spanish, Chinese, Hindi, Arabic, Portuguese, Bengali, Russian, Japanese, Punjabi, German, French, Italian, Korean, Turkish, Telugu, Marathi, Tamil, Vietnamese, Urdu — and more through Google Translate.

## Repository Contents

| File | Description |
|---|---|
| `Captions Generator, Translator and Summarizer.ipynb` | Full pipeline — audio extraction, transcription, translation, summarization, SRT generation |
| `subtitle_result.srt` | Sample output SRT file |
| `summarized_datasetlink.txt` | Reference links for datasets used |
| `21BCE1950_Omprakash_DA1.pdf` | Data analysis survey report |
| `21BCE1950_AI_DA2_PAPER.pdf` | Research paper |
| `21BCE1950_AI_DA2_OUTPUT.pdf` | Model output documentation |
| `21BCE1950_AI_DA3.pdf` | Final data analysis report |
| `AI(SUB GEN PPT REVIEW).pdf` | Presentation slides |
| `Implemented code.pdf` | Code documentation PDF |

## Stack

Python · HuggingFace Transformers · T5 (LaMini-Flan-T5-248M) · PyTorch · NLTK · googletrans · pytube · AssemblyAI API · Jupyter Notebook
