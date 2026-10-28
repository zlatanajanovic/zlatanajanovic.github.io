# Video placeholders

Drop the following files into this folder; `index.html` already references them.
Once a file is in place, delete the matching `<div class="video-placeholder-badge">…</div>` in `index.html`.

| File | Where it appears |
| --- | --- |
| `teaser.mp4` | Teaser under the title (autoplay, muted, loop). Poster: `static/images/teaser_poster.jpg` |
| `st2_paper_video.mp4` | "Video" section. Alternatively, uncomment the YouTube iframe above that block and set `VIDEO_ID` |
| `monolithic_teaching.mp4` | Carousel "Teaching the restocking task", slide 1 |
| `st2_teaching.mp4` | Carousel, slide 2 |
| `autonomous_execution.mp4` | Carousel, slide 3 |
| `correction.mp4` | Carousel, slide 4 |

Keep files under ~10 MB each for GitHub Pages (H.264 mp4, 1280x720 is plenty).
