# Video Analysis Pipeline

Drop a video into a [new issue](https://github.com/Bliixkii/video-analysis-pipeline/issues/new) and a worker will reply with a professional analysis.

## What happens
1. You open an issue and upload a video.
2. A local worker (on your Windows PC) polls GitHub every 10 minutes and on issue open/edit.
3. It sends the **raw video** to Gemini Flash, which watches the full video end-to-end.
4. Gemini returns a structured professional analysis, posted as a comment.

## No screenshots, no frames, no verbatim transcripts
The worker does **not** extract frames, take screenshots, or paste transcript snippets. The model consumes the video directly.

## Analysis focus
The prompt is optimized to flag the gap between **what is said** and **what is shown** — the #1 correction most creators miss.

## Requirements
- This repo uses a **self-hosted runner** (`windows-local`) registered on your PC.
- `GH_PAT` secret with `repo` scope.
- `GEMINI_API_KEY` secret from [Google AI Studio](https://aistudio.google.com/app/apikey).

## Cost
- GitHub issue attachments: free.
- Gemini Flash has a generous free tier; paid tier is cheap for video.
- No LFS or large-storage fees.
