# Wahid Wasiqs Production Studio

A single-file, browser-only studio for planning and previewing short vertical Reels.

## Publish free with GitHub Pages

1. Create a new public GitHub repository.
2. Upload `index.html` to the repository root.
3. In **Settings → Pages**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. Open the URL GitHub displays after it finishes building.

No server, database, or build step is required. Image and writing providers are optional: their keys stay in the local browser and are never part of the exported plan.

## Important limits

The studio can generate prompts, call Gemini or Hugging Face when users provide their own keys, preview narration via the browser speech engine, trim music for planning, export a JSON production plan, and render a silent WebM Reel directly in the browser. WebM is used because it is natively supported by browser video APIs; MP4 export would require loading a large FFmpeg module and will be less dependable on mobile.
