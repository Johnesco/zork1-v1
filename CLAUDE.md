# Zork I — v1: The Port (FROZEN)

This is a **frozen published snapshot** of Zork I. New work does NOT happen here.

| | |
|---|---|
| Repo | `Johnesco/zork1-v1` |
| Hub registration | `zork1-v1` (`versionOf: zork1`, `versionLabel: v1 — The Port`) |
| Companion repos | `zork1` (Current), `zork1-v0` (ZIL), `zork1-v2`, `zork1-v3` |
| Golden seed | **13** (in `tests/seeds.conf`) |
| Binary | `zork1-v1.ulx` (compiled from this repo's `story.ni`) |

## What v1 is

A complete, playable, winnable translation of Zork I from ZIL into Inform 7. **Every room, puzzle, text response, and behavior** from v0 is reproduced here. No fixes, no enhancements, no quality-of-life improvements. Goal: 1:1 gameplay match with v0.

Some original ZIL bugs vanish naturally in translation to a modern engine — that's fine; we don't force them back in.

## Editing rules

**Default:** Don't edit this repo. Work happens in **`Johnesco/zork1`** (Current).

This repo is only edited when:
- A v0-fidelity bug surfaces and must be fixed at the v1 level
- The fix must then propagate **upward** to v2, v3, and Current (never downward)

If you patch this repo:
1. Edit `story.ni` here
2. Recompile: `python /c/code/ifhub/tools/pipeline.py zork1-v1 compile`
3. Run walkthrough with golden seed 13: `python /c/code/ifhub/tools/testing/run_walkthrough.py --config tests/project.conf --seed 13`
4. Commit + push (auto-deploys to `johnesco.github.io/zork1-v1/`)
5. Apply the same change to `zork1-v2`, `zork1-v3`, and `zork1` (Current), recompile each

For the full multi-version workflow, see `C:\code\ifhub\reference\multi-version-guide.md`.

## Project-wide context

For Zork-specific game systems, scoring, and project workflow conventions, see the main repo's `CLAUDE.md` at `C:\code\text-games\i7\zork1\CLAUDE.md`.
