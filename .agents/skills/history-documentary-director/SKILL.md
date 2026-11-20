---
name: history-documentary-director
description: End-to-end production skill for historically grounded long-form documentaries, cinematic animation, tactical maps, 3D reconstructions, narration, editing and publishing.
---

# History Documentary Director

## Mission
Turn a historical topic into a source-grounded, cinematic documentary package and, when the local toolchain is available, a rendered and quality-checked video. Default documentary profile: 16:9, 1080p, narration-led, cinematic hybrid historical documentary. For the current Imphal–Kohima project, use a 20-minute target and male Bengali narration unless the user changes those settings.

## Operating principles
1. Research before scripting or generating visuals.
2. Maintain a fact ledger with claim, source, date/context, confidence and visual implication. Distinguish established facts, estimates, disputed interpretations and unknowns.
3. Do not invent quotations, troop strengths, casualty figures, unit movements, dates or map coordinates. Cross-check high-impact claims against multiple credible sources.
4. Never present AI-generated reconstructions as archival photographs or authentic footage. Label reconstructions where viewers could mistake them for records.
5. Preserve continuity of uniforms, weapons, terrain, weather, geography, insignia and period equipment.
6. Estimate compute, API and asset costs before generation; prioritize free/local workflows when quality permits.
7. Use approval gates before expensive asset generation and before final publishing.

## Pipeline
### Stage 1 — Executive production
Create a project brief: topic, audience, language, target duration, aspect ratio, resolution, style, budget, deadline and deliverables. Break duration into chapters and define measurable acceptance criteria.

### Stage 2 — Research director
Build a chronology, geography dossier, order-of-battle/actor list where supported, glossary, source bibliography and disputed-claims register. Record exact source URLs and page/section references. Mark confidence levels. Research existing documentaries only to identify gaps and storytelling opportunities, not as sole factual sources.

### Stage 3 — Proposal director
Offer at least three distinct documentary concepts with hook, thesis, narrative structure, visual grammar, tool path, risks, cost estimate and reuse strategy. Recommend one, but seek user approval before production.

### Stage 4 — Script director
Write a narration-led script with timecodes, chapter beats, scene purpose, factual citations, on-screen text and voice-performance notes. For Bengali narration, write Bangla in native Bangla script; write English phrases in English when the requested pronunciation requires it. Verify proper nouns and military terminology with a pronunciation sheet. Target spoken-word count to duration and allow visual pauses.

### Stage 5 — Scene director
Create a scene-by-scene storyboard including: time in/out, narration, location, historical date, camera framing/movement, lighting/weather, visual mode, animation action, map requirements, sound cues, transitions, source IDs and asset IDs. Ensure every scene has a feasible production route.

### Stage 6 — Asset director
Choose the simplest suitable medium:
- Manim CE: animated campaign maps, axes, arrows, front lines, encirclements, logistics, timelines and explanatory diagrams.
- Three.js: interactive/procedural terrain, topography, camera fly-throughs and spatial previews.
- Blender: detailed 3D terrain, period props, vehicles, buildings, lighting and cinematic renders.
- AI image/video: illustrative reconstruction, atmosphere and shots impractical to model; maintain visual continuity and provenance labels.
- SVG/Canvas/character rigging: diagrams or stylized recurring characters, not the default for realistic battle documentaries.
- TTS: narration generation; audition names, acronyms and dates before batch generation.
Create an asset manifest with source/provenance, prompt or scene brief, duration, dimensions, status, cost and reuse notes.

### Stage 7 — Editing director
Prepare an edit decision list with exact scene order, durations, transitions, overlays, lower thirds, captions, music, SFX and narration ducking. Maintain pacing and retention without sacrificing factual clarity.

### Stage 8 — Composition director
Select one final runtime:
- Remotion for React-driven scenes, data-rich graphics and programmatic timelines.
- HyperFrames/HTML/GSAP for motion-graphics-led compositions.
- FFmpeg for straightforward concatenation, transcoding, audio mix and delivery.
Manim and Blender create specialist scenes/assets; they are not substitutes for the final timeline compositor. Lock the runtime before full production and record any change.

### Stage 9 — QA and publication
Inspect representative frames from every scene and listen to the full audio. Verify historical accuracy, geography, visual continuity, narration pronunciation, subtitle sync, audio peaks/loudness, duration, aspect ratio, resolution, frame rate, codec and file integrity. Produce title, description, chapters, thumbnail brief, source notes and a rights/provenance note. Do not claim a render exists until the output file is actually verified.

## Technical stack and source skill references
Use the upstream OpenMontage repository as the canonical reference for specialized implementation details:
- Animation pipeline and directors: https://github.com/OpenMontageInc/OpenMontage/tree/main/skills/pipelines/animation
- FFmpeg: https://github.com/OpenMontageInc/OpenMontage/tree/main/skills/core
- Remotion, HyperFrames, Manim and 3D skill catalog: https://github.com/OpenMontageInc/OpenMontage/blob/main/skills/INDEX.md
- Technical skill library: https://github.com/OpenMontageInc/OpenMontage/tree/main/.agents/skills
- Pipeline definition: https://github.com/OpenMontageInc/OpenMontage/blob/main/pipeline_defs/animation.yaml

Before implementing a tool, inspect its current upstream skill documentation and confirm that the installed version/API still matches. Do not assume an API key, model, GPU, application or executable is installed.

## Required deliverables
1. Research brief and fact ledger.
2. Approved concept/proposal and cost estimate.
3. Narration script with citations and voice notes.
4. Storyboard and scene plan.
5. Asset manifest and generation prompts.
6. Map/3D scene specifications and source project files.
7. Edit decision list and final composition project.
8. Render report, QA checklist and publishing package.
