# Video FAQ files

The microneedling Video FAQ player loads these files. Compress each source
MP4 to web-optimised 720p H.264 (see command below) and save it here with the
exact filename in the left column.

| Filename in this folder      | Source video (Google Drive)             |
|------------------------------|-----------------------------------------|
| benefits.mp4                 | Benefits & Starting Point               |
| safe.mp4                     | Is Microneedling Safe?                  |
| tighten.mp4                  | Can Microneedling Tighten Skin?         |
| acne-scarring.mp4            | Microneedling for Acne Scarring         |
| cause-scars.mp4              | Can Microneedling Cause Scars?          |
| botox.mp4                    | Microneedling and Botox                 |
| rosacea.mp4                  | Microneedling and Rosacea               |
| marionette-lines.mp4         | Microneedling and Marionette Lines      |
| at-home-vs-clinic.mp4        | At-Home Kits vs Clinic                  |

## Compress each file (720p, web-optimised, faststart)

```
ffmpeg -i "INPUT.mp4" -vf "scale=-2:720" -c:v libx264 -crf 24 -preset slow \
  -profile:v high -pix_fmt yuv420p -movflags +faststart \
  -c:a aac -b:a 128k "OUTPUT.mp4"
```

`-movflags +faststart` lets the video start playing before it fully downloads.
Target roughly 5-12 MB per clip. If a file is still large, raise `-crf` to 26-28.
