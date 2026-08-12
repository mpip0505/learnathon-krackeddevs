# Design Notes

## Why this scope, and not the full pipeline

The full project vision (pose estimation via MediaPipe → P1–P10 checkpoint detection → swing consistency analysis → rule-based fault checks → LLM feedback) is too much to build and demo reliably in a learnathon window. This build isolates the part of the experience that's easiest to lose sight of when focused on the ML: **does the feedback loop actually feel useful to a golfer?**

So instead of real pose data, the app runs on a small set of curated example swing phases with pre-written comparison notes and coaching tips. It's a "Wizard of Oz" version of the final feature — the UI and interaction are real, the intelligence behind them is scripted for now.

## Sections and what each one is proving

- **Swing Phase List** — proves the entry point is simple: 2–3 phases only, no overwhelming choice. This mirrors what the real app would show after analyzing a user's swing video.
- **Example Comparison Panel** — proves the core value: side-by-side comparison plus a short, specific note on what differs. This is the piece that eventually gets replaced by real pose-estimation deltas.
- **Coaching Tips Panel** — proves the payoff: plain-English, not jargon. This is where the LLM feedback layer will eventually plug in.

## Features and what each one is proving

- **Tap a swing phase** — proves state management: selection drives what's shown, cleanly.
- **Show example feedback** — proves the tips are *tied to the selection*, not static — this is the detail that makes it feel like a real analysis tool rather than a brochure.
- **Reset to sample view** — proves the demo is repeatable without a reload; lower priority than the other two if time runs short.

## Deliberately out of scope for this build

- Real pose estimation / video upload
- P1–P10 checkpoint detection
- Consistency/variance scoring across multiple swings
- LLM-generated (vs. pre-written) feedback
- Any backend/serverless integration (S3, Lambda, API Gateway)

These are the next steps once the interaction pattern here is validated — see the main project for that roadmap.

## Open questions for after the learnathon

- What's the minimum real data needed to replace the example phases with actual pose-estimation output?
- Does the "comparison + tips" framing hold up once the comparison is computed rather than curated?