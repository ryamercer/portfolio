# portfolio

Live at: https://ryamercer.github.io/portfolio/

Not linked from anywhere and blocked from search indexing (`robots.txt` +
`<meta name="robots" content="noindex, nofollow">`), so only people with the
direct link can find it. Anyone with the link *can* view it — GitHub Pages'
free tier requires the repo to be public.

## Adding a new track

1. Drop the audio file into this folder (same folder as `index.html`).
2. Open `index.html`, find the `TRACKS` array near the bottom (inside the
   `<script>` tag), and add a new object:

   ```js
   {
     title: "Track or artist name",
     date: "2026-07-01",
     tags: "Genre, context",
     audioFile: "exact-filename.wav",
     youtubeId: "the-11-character-id-from-the-youtube-url"
   }
   ```

   Get `youtubeId` from the share URL, e.g. `https://youtu.be/feyz3PxqceQ`
   → `feyz3PxqceQ`. Leave `youtubeId: ""` if there's no video yet — it'll
   show a "coming soon" placeholder instead of breaking.

3. Commit and push:

   ```bash
   git add .
   git commit -m "Add [track name]"
   git push
   ```

Pages redeploys automatically within a minute or two of the push.
