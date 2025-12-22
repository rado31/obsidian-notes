
```bash
yt-dlp -f "bv*[ext=mp4][height<=1080]+ba[ext=m4a]/b[ext=mp4]" --merge-output-format mp4 URL
```

### 🔍 What this does

- `bv*` → best **video-only** stream
- `ba` → best **audio-only** stream
- `[ext=mp4]` → forces MP4 container for video
- `[height<=1080]` → best MP4 under a resolution limit
- `[ext=m4a]` → best audio compatible with MP4
- `/b[ext=mp4]` → fallback to best single-file MP4 if separate streams aren’t available
- `--merge-output-format mp4` → ensures final output is **MP4** (`ffmpeg` ***IS REQUIRED***)