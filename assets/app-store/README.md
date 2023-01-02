# App Store Marketing Assets
This document describes how to produce App Store marketing assets via simulator and device.

## iPhone 6.5 inch display
### Screenshots
Use iPhone 14 Plus in simulator.
### Previews
Use iPhone 14 Pro on device then use Handbrake to reduce framerate to 30 and keep dimensions at 886x1920.

Sometimes the preview might be rejected with an error of "Your app preview contains unsupported or corrupted audio.".
This can be fixed by adding a silent audio track using `ffmpeg`:
```
ffmpeg -f lavfi -i anullsrc=channel_layout=stereo:sample_rate=44100 -i SOURCE -c:v copy -c:a aac -shortest OUTPUT
```

## iPhone 5.5 inch display
### Screenshots
Use iPhone 8 and resize to 1242x2208. This requires changing the aspect ratio slightly.
