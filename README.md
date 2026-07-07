# Video Analysis Pipeline

Drop a video into a [new issue](https://github.com/Bliixkii/video-analysis-pipeline/issues/new) and a worker will reply with a professional analysis.

## What happens
1. You open an issue and upload a video.
2. A local worker (on your Windows PC) polls GitHub every 10 minutes and on issue open/edit.
3. It downloads the video, extracts key frames, transcribes audio with Whisper, and posts an analysis comment.

## Requirements
- This repo uses a **self-hosted runner** (`windows-local`) registered on your PC.
- `GH_PAT` secret with `repo` scope.
- FFmpeg and Whisper installed locally.

## Cost
- GitHub issue attachments: free.
- Whisper runs locally (no API cost).
- No LFS or large-storage fees.
