# AI & Social Media: from idea to product

Content creation has become one of the fastest-growing fields of recent years. Today, beyond what gets made, what
gives content its value is what it conveys and how that message is understood by the people it reaches.

This repo holds the scripts behind every video and image on my portfolio site and the
[Ardea Skin](https://github.com/izzosuarez-boop/ardea-skin) demo store.

## The problem

Making content keeps getting easier, so social networks, media outlets and websites flood people with more
information than they can take in. Selling an idea through your site is not the same when twenty other places are
trying to do it too. That is why, more than ever, what matters is not the medium that carries the idea but the idea
itself: presented so it is easy to understand and digest, and so it builds an identity people remember in the
medium and long term.

## How I built it

Every video on this site follows a structure built to convey one idea and what I want to sell. I used Google's AI
models (Gemini Omni and its Flash version, plus Gemini for images and voice), Seedance and DaVinci AI, and coding
tools like Claude Opus 5.5. That last part matters: a good result comes from a solid base and a model that drives
the whole creative process during development. Code doesn't replace the AI; it complements it.

A good video doesn't come from a prompt: it comes from deciding what you want to say, which part of the product to
show, and how to tell it so it's understood the first time.

- **The idea:** each shot carries a single message and one line that goes with it.
- **Consistency is designed:** the same character and the same setting in every shot. Each new image is generated
  from the previous one, so the viewer follows the story without getting distracted.
- **Then it gets corrected:** every fix is checked frame by frame before moving on.
- **What AI doesn't do well, code solves:** the screens it invents are replaced with real content; text, speech
  bubbles and subtitles are drawn separately; and every voice line is transcribed to check it says exactly what it
  should.

## Result

Videos with an intent and an idea behind them. The site exists to sell my portfolio and my skills to anyone who needs
to build, improve, or simply find talent for their projects, and that is what every video tries to convey: a
problem, its solution and my role in it, while showing what I can do.

All the multimedia content created and corrected with AI for the portfolio and for Ardea Skin, retakes included,
cost less than 25 dollars. Nothing is made at random: every step is measured and costs are cut, for example by
doing in code what AI charges a lot for and does badly.

## What's in this repo

| Path | What it is |
|---|---|
| `scripts/images/` | Product photos and the portrait scene (Gemini image), with the approved versions in `approved.json` |
| `scripts/media/generate_category_media.py` | Category covers and the narrated tutorial videos of the store |
| `scripts/media/explainer_video.py` | Stills and AI clips for the explainer videos, each with its cost |
| `scripts/media/*_assemble.py` | Assembly of each video: voice (Gemini TTS) checked by transcription, shots, subtitles in English and Spanish, ffmpeg |
| `scripts/media/scenes/` | Scenes made in code (HTML), filmed frame by frame with Playwright: the screens, diagrams, speech bubbles and the 6-second loops |
| `scripts/media/record_app.py`, `record_store.py` | Real software captured state by state, instead of screens invented by AI |
| `scripts/media/PLAYBOOK.md` | My working notes (in Spanish): every decision, error and cost, video by video |
| `scripts/shopify/` | Uploads the published files to the Shopify CDN |

The scripts were written inside my portfolio's monorepo, so the publishing steps write into that site's content
files. Reference photos of real people are kept out of the repo (`refs/`).

## Stack

Gemini Omni · Gemini image · Gemini TTS · Seedance · DaVinci AI · Claude Opus 5.5 · Python · Playwright · ffmpeg ·
Pillow · OpenCV · Shopify Files
