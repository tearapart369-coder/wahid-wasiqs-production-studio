---
name: all-skills
description: Master index of every skill available in this environment, grouped by domain, with when-to-use guidance and routing rules. Use at the start of a task to pick the right skill, or when the user asks what skills exist or which one fits.
---

# All Skills: Master Index

This is a compiled routing guide built from the name and description of every skill available in this environment. It does not contain the full instructions of each skill. When a row below matches the task, invoke that skill with the Skill tool (`plugin:skill` for plugin skills) and follow its own instructions.

## Routing rules
1. **Process before implementation.** Use a process skill first (brainstorming for new features, systematic-debugging for bugs), then the domain skill.
2. **If a skill plausibly applies, invoke it** before answering or acting.
3. **User instructions win** over any skill (CLAUDE.md, direct requests).
4. **Don't guess names.** Use only names listed here or in the live skill listing.
5. **Check pricing before installing anything.** Some skills front paid services (vidIQ, Ayrshare, CellCog, Kling, Supabase). Don't enter credentials or payment details without the user's go-ahead.
6. **Failed MCP servers.** If a plugin's MCP server failed to connect (proxy 403, connection closed), tell the user. The skill text may still load, but its tools won't work.

---

## 1. Core / Claude Code
| Skill | Use when |
|---|---|
| session-start-hook | User wants a SessionStart hook committed to their repo (not for environment setup) |
| update-config | Changing settings.json: hooks, permissions, env vars, "from now on when X" automations |
| keybindings-help | Rebinding keys, chord shortcuts, `~/.claude/keybindings.json` |
| fewer-permission-prompts | Building a read-only allowlist to cut permission prompts |
| code-review | Reviewing a diff, PR, branch or path for correctness bugs (levels low to max; `--comment`, `--fix`) |
| simplify | Cleaning up changed code for reuse and efficiency (no bug hunting) |
| security-review | Security review of pending changes |
| init | Initialise project instructions (CLAUDE.md) |
| loop | Recurring or polling tasks on an interval, or self-paced |
| claude-api | Anything involving Claude/Anthropic APIs, SDKs, models, pricing, caching, tool use |
| run | Launch and drive the project's app to see a change working |
| plugin-authoring | Making mods: themes, panes, status lines, slash commands, tool-call hooks |

## 2. Artifacts and visuals
| Skill | Use when |
|---|---|
| artifact-design | **Always load before writing any Artifact** |
| artifact-capabilities | Page needs runtime behaviour: live data, shared state, viewer identity, Claude calls, file storage |
| artifact-diagramming | A diagram would show a mechanism better than prose (inline SVG) |
| dataviz | Any chart, graph, dashboard, stat tile or data visualization |

## 3. Superpowers (engineering workflow)
| Skill | Use when |
|---|---|
| using-superpowers | Start of any conversation: how to find and use skills |
| brainstorming | Before building any feature or entering plan mode |
| writing-plans | Turning a spec into an implementation plan |
| executing-plans | Running a written plan |
| subagent-driven-development | Executing a plan through subagents |
| dispatching-parallel-agents | Several independent tasks that can run in parallel |
| test-driven-development | Before writing implementation code |
| systematic-debugging | Any bug, failure or unexpected behaviour |
| requesting-code-review / receiving-code-review | Asking for a review, or handling review feedback |
| verification-before-completion | Before claiming work is done or passing |
| finishing-a-development-branch | Work is done: decide on merge, PR or cleanup |
| using-git-worktrees | Isolated workspace for feature work |
| writing-skills | Creating or editing skills |
| diagnosing-superpowers | Skills aren't loading or firing as expected |

## 4. Anthropic document and browser skills
| Skill | Use when |
|---|---|
| docx / pdf / pptx / xlsx | Word, PDF, PowerPoint or Excel files specifically |
| docs | Living documents |
| google-workspace | Creating or changing Google Docs, Sheets or Slides in Drive (load before the first connector call) |
| built-in-browser / chrome-browser / computer-use | Browser or desktop interaction |
| deep-research | Multi-source research with citations |
| skill-creator | Authoring new skills |
| import-memory | Importing memory from elsewhere |
| morning | Morning briefing routine |

**YouTube set (anthropic-skills:yt-\*):** yt-audit, yt-chapters, yt-comment, yt-edit, yt-package, yt-plan, yt-retention, yt-script, yt-seo, yt-shorts, yt-viral.

## 5. Vercel / web platform
- **Deploy and ops:** vercel:deploy, vercel:status, vercel:env, vercel:env-vars, vercel:bootstrap, vercel:deployments-cicd, vercel:vercel-cli, vercel:access-protected-vercel-deployment, vercel:verification
- **Frameworks:** vercel:nextjs, next-cache-components, next-upgrade, next-forge, turbopack, react-best-practices, shadcn, routing-middleware, microfrontends
- **AI:** vercel:ai-sdk, ai-gateway, build-agents, eve, chat-sdk, workflow, vercel-agent
- **Platform:** vercel:vercel-functions, vercel-services, vercel-storage, vercel-sandbox, vercel-firewall, vercel-connect, cdn-caching, runtime-cache, flags-sdk, marketplace, auth, create-a-backend
- **Reference:** vercel:knowledge-update (corrects outdated Vercel knowledge)

## 6. Design
design:accessibility-review, design-critique, design-handoff, design-system, research-synthesis, user-research, ux-copy.
Other: image-generation:image-generation, screeny:screeny-mockups (device mockups and 3D animation), animation-studio, motion-reel.

**AnimatedWebs** (animated sites, heroes, backgrounds): the commands background, browse, component, design, gradient, hero, request, save, site, style, and the matching skills animatedwebs-backgrounds, -components, -design, -gradients, -hero, -site, -style.

## 7. Video, audio and media generation
- **Remotion:** remotion-best-practices, -captions, -create, -docs, -interactivity, -maps, -markup, -multimedia, -render, -saas, -studio, -upgrade
- **AI video editor:** ai-video-edit, ai-video-shot, video-editing, video-generation
- **Kling:** kling-ai, kling-ai-generate-image, kling-ai-generate-video
- **CellCog** (any-to-any agent): cellcog, cellcog-setup, 3d-model-generation, audio-generation, data-analysis, deep-research, diagram-flowchart, excel-spreadsheet, game-asset-generation, image-generation, meme-generator, music-generation, pdf-document-generation, presentation-slides, sticker-generator, ui-prototype-wireframe, video-generation

## 8. Social media (social-media-skills:\*)
- **Strategy:** social-strategy, goals-and-kpis, content-calendar, content-pillars, batch-content-plan, campaign-and-launch-planning, brand-profile, audience-research, competitor-analysis, content-audit, experimentation-and-ab-testing, analytics-and-reporting, scheduling-and-queue, seasonal-and-moment-marketing, trend-jacking
- **Writing:** caption-writer, hook-writer, carousel-writer, thread-writer, story-writer, reels-script, short-form-video-script, tiktok-script, linkedin-post-writer, threads-post, text-post-and-microblog, reply-and-comment-writer, writing-style-and-tone, voice-builder, storytelling-and-narrative, listicle-and-roundup, contrarian-and-opinion, educational-content-and-how-to, scripting-and-storyboarding
- **Platforms:** instagram-growth, instagram-reels-publishing, instagram-seo, facebook-strategy, facebook-groups, linkedin-growth, linkedin-company-pages, tiktok-growth, tiktok-photo-mode, tiktok-video-publishing, threads-growth, x-growth, pinterest-growth, pinterest-pin-design, pinterest-seo, reddit-marketing, youtube-long-form, youtube-shorts, youtube-publishing-and-metadata
- **Growth and community:** community-management, crisis-and-moderation, engagement-routine, collabs-and-cross-promotion, ugc-and-influencer, social-proof-and-testimonials, social-selling-and-dm, lead-magnets-and-funnels, link-in-bio-and-traffic, creator-monetization, email-and-newsletter, hashtag-strategy, social-seo, ai-search-optimization, profile-optimization
- **Formats and ideas:** content-recycling, content-research-and-sourcing, cross-platform-repurposing, idea-generation-and-ideation, before-after-and-transformation, behind-the-scenes-and-founder, data-and-original-research, interactive-content, livestream-and-realtime, meme-and-culture, podcast-and-audiograms, talking-head-and-piece-to-camera, viral-reverse-engineering, platform-specs-and-validation
- **Design and AI tools:** canva, capcut, descript, design-and-templates, infographic-and-data-viz, quote-cards-and-text-graphics, thumbnail-design, image-prompt, ai-image-editing, ai-music-and-sound, ai-video, ai-voiceover, captions-and-clipping, flux, heygen, ideogram, kling, luma, nano-banana, opus-clip, runway, suno, synthesia, veo-3

## 9. Publishing and analytics platforms
- **Ayrshare:** setup, getting-started, post, plan-and-schedule-campaign, draft-in-brand-voice, generate, media, history, analytics, comments, messages, profiles, webhooks, errors
- **vidIQ:** vidiq-get-started, channel-audit, comment-insights, competitor-watchlist, new-upload-review, next-video-planner, packaging-comparison, packaging-studio, retention-analysis, shorts-inspiration, trend-radar, video-ideas
- **Instagram:** access, configure, qualification
- **Posty:** posty

## 10. Hugging Face (huggingface-skills:\*)
hf-cli, hf-mem, hf-cloud-aws-context-discovery, hf-cloud-python-env-setup, hf-cloud-sagemaker-deployment-planner, hf-cloud-sagemaker-iam-preflight, hf-cloud-sagemaker-production-defaults, hf-cloud-serving-image-selection, huggingface-best, -community-evals, -datasets, -gradio, -llm-trainer, -local-models, -lora-space-builder, -paper-publisher, -papers, -spaces, -tool-builder, -trackio, -vision-trainer, -zerogpu, train-sentence-transformers, transformers-js, trl-training.

---

## Quick decision guide
- **Build a feature:** brainstorming, then writing-plans, then test-driven-development, then verification-before-completion
- **Fix a bug:** systematic-debugging, then verification-before-completion
- **Ship to the web:** vercel:nextjs, then vercel:deploy
- **Make a chart or dashboard:** dataviz, then artifact-design
- **Make a deck, doc or sheet:** pptx, docx or xlsx (or google-workspace if the user names Google)
- **Social content:** social-strategy, then the platform and writing skills, then ayrshare:post to publish
- **YouTube channel work:** yt-\* or vidiq:\*
- **Video or motion:** remotion-\*, kling-ai, ai-video-editor or cellcog video-generation
- **Claude or Anthropic API code:** claude-api

## Maintenance
This index reflects the skill listing at compile time (2026-11-20). Re-run the listing and update it when plugins are added or removed. Per-skill bodies are not duplicated here, so always load the real skill for its full workflow.
