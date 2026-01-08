
> **LTS: fixed problem with cookies**

## Download video

```bash
yt-dlp -f "bv*[ext=mp4][height<=1080]+ba[ext=m4a]/b[ext=mp4]" --merge-output-format mp4 --cookies-from-browser chrome URL
```

### 🔍 What this does

- `bv*` → best **video-only** stream
- `ba` → best **audio-only** stream
- `[ext=mp4]` → forces MP4 container for video
- `[height<=1080]` → best MP4 under a resolution limit
- `[ext=m4a]` → best audio compatible with MP4
- `/b[ext=mp4]` → fallback to best single-file MP4 if separate streams aren’t available
- `--merge-output-format mp4` → ensures final output is **MP4** (`ffmpeg` ***IS REQUIRED***)

## Download audio

```bash
yt-dlp -f "ba/best" -x --audio-format mp3 --audio-quality 0 --cookies-from-browser chrome URL
```

### 🔍 What this means

- `"ba/best"` → this ensures `yt-dlp` grabs the **best available audio stream** (Opus/M4A), then converts to mp3
- `-x` → extract audio
- `--audio-format mp3` → convert to MP3
- `--audio-quality 0` → **best V0 (~245 kbps)** via LAME

> `0` = best  
> `5` ≈ medium  
> `9` = worst