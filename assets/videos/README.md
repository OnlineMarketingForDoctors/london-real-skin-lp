# Video FAQ files

The microneedling Video FAQ player loads these files. Until they exist, the
player automatically falls back to the Google Drive version, so the section
keeps working. Once a file is added here, the clean native player is used.

Save each file with the exact filename in the left column.

| Filename in this folder | Source video (Google Drive)                         |
|-------------------------|-----------------------------------------------------|
| benefits.mp4            | What Are Benefits Of Microneedling                  |
| safe.mp4                | Is Medical Microneedling Safe                       |
| tighten.mp4             | Can Microneedling Tighten The Skin                  |
| cause-scars.mp4         | Can Microneedling Cause Scars                       |
| permanent.mp4           | Are Microneedling Results Permanent                 |
| recovery.mp4            | What Does Aftermath Of Microneedling Look Like      |
| botox.mp4               | Can Microneedling Affect Botox                      |
| marionette-lines.mp4    | Will Microneedling Help Marionette Lines            |
| at-home-kits.mp4        | Are Home Kits And Derma Rollers The Same As Microneedling |

## These files are already small (3-12 MB), so no compression is needed

Just download each from Drive and save it here with the matching name above.

If you ever want to shrink one further (the largest is ~12 MB), you can run:

```
ffmpeg -i "INPUT.mp4" -vf "scale=-2:720" -c:v libx264 -crf 24 -preset slow \
  -profile:v high -pix_fmt yuv420p -movflags +faststart \
  -c:a aac -b:a 128k "OUTPUT.mp4"
```
