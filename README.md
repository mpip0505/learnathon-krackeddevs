# Golf Swing Analyzer — Example Viewer (Learnathon Build)

A lightweight, interactive demo of the coaching-feedback loop from the larger [Golf Swing Analyzer](#) project. Instead of running live pose estimation, this build uses curated example swing phases to demonstrate how the final product will guide a golfer from "here's what your swing looks like" to "here's what to fix."

## What it does

You pick a swing phase, see it compared against a reference example, and get plain-English coaching tips based on what's different. That's the whole loop — small, but it's the loop that matters.

## Sections

1. **Swing Phase List** — 2–3 example swing phases (e.g. address, top of backswing, impact) the user can scan and pick from.
2. **Example Comparison Panel** — shows the selected phase side-by-side with a reference example, plus a short note on what's different.
3. **Coaching Tips Panel** — plain-English tips tied to the selected phase, generated from the comparison.

## Features

1. **Tap a swing phase** — selecting a phase updates the comparison panel on screen.
2. **Show example feedback** — picking a phase swaps in matching coaching tips.
3. **Reset to sample view** — clearing the selection returns the app to the starter examples.

## Why this scope

This is a deliberately reduced slice of a larger idea (pose estimation → P1–P10 checkpoint detection → consistency analysis → LLM coaching). For a time-boxed build, the goal isn't the ML — it's proving the interaction pattern end-to-end with static example data, so the loop is provably real before the pipeline behind it is.

## Tech stack

_Fill in once decided — e.g. React (frontend), static JSON for example phase data, deployed via [hosting]._

## Status

Learnathon prototype. Not connected to the live pose-estimation pipeline yet — see [`NOTES.md`](./NOTES.md) for design reasoning and what's deliberately out of scope.