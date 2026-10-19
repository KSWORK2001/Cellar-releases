# Cellar

A Wine bottle manager for macOS, in the spirit of CrossOver. Independent and written from
scratch, Cellar manages bottles, runners, and game installs while the entire engine layer
(Wine, DXVK, MoltenVK, GStreamer) is adopted as-is from its official open source
distributors. Nothing is reimplemented, everything is wired.

The source is private during the beta. Releases and the update feed live here.

## Current version

**0.1.16-beta**, published below. Every installed copy updates itself in place from this
repo, signed and verified.

## Where we are versus CrossOver

Feature surface audited item by item against CrossOver 25 for Mac, weighted by how much of
the product each area is.

| Area | Coverage | What is missing |
| --- | --- | --- |
| Bottle management | 50% | clone, export and import, archiving, list search |
| Engines and graphics | 70% | ESync/FSync/MSync toggles, D3D12, per-bottle D3DMetal switch |
| Installing and running | 65% | compatibility database with per-app recipes, guided store installs |
| Disc and file intake | 100% | nothing, and parts are ahead (below) |
| Wine power tools | 36% | winecfg, regedit, task manager, explorer launchers |
| Desktop integration | 63% | Finder double-click, per-app dock icons, screen options |
| Gaming and performance | 50% | Apple Game Mode |
| Maintenance and updates | 64% | bottle repair, telemetry |
| App compatibility database | 0% | CrossOver's whole moat, thousands of tested recipes |
| **Overall, weighted** | **58%** | |

The core workflow a person touches daily (install, run, graphics, discs, updates, logs,
removal) sits around 80 percent.

## What Cellar has that CrossOver does not

- Whole disc sets mounted at once, disc 1 on D:, disc 2 on E:, with true volume labels
- Zip and installed-folder game intake, no installer needed
- A Windows VM bridge: one-click UTM install, one-click VM creation from the Windows ISO,
  discs in, installed games out into any bottle, for installers Wine cannot run
- Run outcome reporting, every launch says how it ended
- Live-streaming run logs
- A DXVK D3D9 toggle per bottle
- A local build channel for development machines

## What is next

1. Bottle export, import, and clone
2. The winecfg, regedit, and task manager launcher row
3. ESync and MSync toggles, per-bottle D3DMetal
4. wine-mono and wine-gecko adoption, so .NET apps install
5. The compatibility database, built on install recipes
6. D3D12 through vkd3d

## Reporting what works

File an issue here with the app, what you installed it from, and what happened. The
compatibility database grows from those reports.
