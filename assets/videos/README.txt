4 of your real video clips are already in here, compressed for the web
and with poster thumbnails generated:

  video_01.mp4  (poster_01.jpg)
  video_02.mp4  (poster_02.jpg)
  video_03.mp4  (poster_03.jpg)
  video_04.mp4  (poster_04.jpg)

They show up in the "A Few Seconds of Us" section as tap-to-play cards —
tapping the poster image swaps it for the actual video and plays it.

To change captions, edit the `videos` array in the CONFIG block near the
top of index.html's <script> tag. To add another clip, drop the file in
here and add a matching entry to that array (poster images can be any
still frame — a phone screenshot of the video works fine if you don't
want to generate a proper thumbnail).

Keep clips reasonably short and compressed (under ~20-25MB each) so the
page still loads fast on mobile data — these four are already sized that
way.
