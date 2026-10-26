---
name: code-lyric-mv
description: >-
  Use when making an original vertical code-driven lyric MV (Canvas/WebGL plates
  + karaoke lyrics + beat cuts) with Claude Opus craft—learning open-source
  craft patterns without copying another project's story, lyrics, or scenes.
---
# Code lyric MV (original craft)

Build a short vertical music video where **lyrics drive on-screen type** and **code draws the plates**—not AI video gen frames. Learn craft from open-source references (beat cuts, word karaoke, plate idioms, post) but **never copy** their story, lyrics, characters, or scene layouts.

## When this applies
- User wants a code MV / lyric karaoke MV / Remotion-or-canvas music short
- They already have (or will make) music + timed lyrics
- Deliverable is an mp4 they can post, plus optional reusable plate recipes

## Hard rules
1. **Original content only** — no cloning another repo's TREATMENT text, plate names tied to their IP, or lyric lines.
2. **Clone to study** when learning a reference: full local clone + read engine; do not claim you learned from README alone.
3. **Gate before Skill/tutorial publish**: self-made cut must pass owner review first.
4. Prefer **Opus-class coding agent** for plate/engine code; GPT/Codex for lyric polish and prompt packs; music tool (e.g. Suno) for the track.

## Pipeline
1. **Brief** — logline, emotion arc (5–7 beats), aspect (default 1080×1920), duration target ≈ audio length.
2. **Music** — lock one mix; note exact duration.
3. **Lyrics JSON** — word-level `{start,end,text}` (or line-level then upgrade). Schema must drive on-screen karaoke; never hardcode final lyric strings inside plate draw code.
4. **Treatment (own)** — motif, color bible, plate list (one idiom per beat), what is forbidden (e.g. static bottom subtitle bar only).
5. **Prompt pack for Opus** — one brief + per-plate prompts + acceptance checklist (density, karaoke sync, no borrowed IP).
6. **Engine** — deterministic canvas/WebGL (or Remotion): `drawFrame(t)`, seeded random, FPS from config; puppeteer or native export → frames → ffmpeg mux with audio (`-movflags +faststart`).
7. **Render** — full frames; skip existing; mux to `out/*.mp4`; pull 3–5 stills for QC.
8. **Accept** — duration ≈ audio; karaoke readable; plates change on beats; no empty stretches; owner OK before packaging as Skill/tutorial.

## Plate craft checklist
- Change major boards every few seconds; avoid one static table
- Put lyric highlights **inside** props (ticket, flag, bar, stamp)—not only a bottom ticker
- One recurring visual motif through all plates
- Stamp / scale / slam micro-motions on numbers and hooks

## Delivery
- Final mp4 path + duration + stills
- NOTES for owner: what is original, known flaws, next deepen pass
- Do **not** auto-publish or seal a new public Skill until the owner accepts the cut

## Anti-patterns
- TTS-only MVP sold as the final music video when a sung track was requested
- Claiming study without a local clone of the reference engine
- Copying peer titles/covers/characters from other AI UP accounts into the MV story
