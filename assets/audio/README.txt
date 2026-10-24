MUSIC — one file, then it works
═══════════════════════════════

The site is wired for a fixed, looping, quiet (22% volume) background
track that plays across every slide and survives the phone locking.

The track IS in place: track.mp3, 34.1s, stereo, 128 kbps, 536 KB.

TO ADD IT:
  Put the file in THIS folder, named exactly:

      track.mp3            (or track.m4a)

  No code changes. Refresh.

  If you have it as a video (mp4/mov), the audio can be pulled out with:
      ffmpeg -i yours.mp4 -vn -c:a libmp3lame -b:a 128k track.mp3

WHILE IT IS MISSING
  Nothing breaks. The control top-right shows "♪?" and the site is silent.

NOTES
  - It starts on her/his FIRST TAP. Every mobile browser blocks audio
    before a user gesture — a platform rule, not a bug.
  - Volume is 0.22, faded in. To change it, edit `const VOL = 0.22;`
    in index.html.
  - Keep it under ~6 MB. 128 kbps is plenty for background music.
