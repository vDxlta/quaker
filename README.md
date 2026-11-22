![Quaker](og.png)

# Quaker

Earthquake early warning (EEW) simulator and real-quake replay viewer.

- Broadcast-style graphics in Japanese (with English subtitles) or fully in English
- Projects: every simulation saves itself in your browser, and preloaded scenarios, real quakes and imports each open as a new project
- Easy mode: presets, sliders, click the map to place the epicenter
- Advanced mode: a timeline editor for quakes, EEW reports, info boxes, camera keys and sound cues, with key-moment markers, multi-select, right-click menus, snapping, foldable tracks, a Reset all menu and an empty-timeline start
- Before the first EEW: light green detection boxes around the stations that felt it, then rough-estimate P and S circles that settle until the EEW takes over
- A realistic event sequence: S-wave arrival, EEW, intensity flash, epicenter info, the full report, then tsunami info, timed from the quake. Pick the steps in Easy mode, or build the run for any quake in Advanced
- Intro screen, plus title cards you can drop anywhere on the timeline: the boxes slide off, the map blurs behind the card, then everything slides back
- Camera: the auto camera keeps every quake that's going in frame by default (toggle it to follow just the newest), plus keyframes or a free map
- Boxes stack by importance (EEW on top, then the S-wave arrival, then the reports), and a second quake's EEW tucks in as a slim strip. When a side fills up it stays one column: the top box stays pinned and the rest cycle through underneath, or you scroll it yourself
- 64 real quakes from Japan and the US, plus USGS, P2PQuake and JMA feed import with step-by-step instructions
- Real replays use JMA's actual EEW reports for 15 quakes from 2011 on (from JMA's published record), including PLUM-only reports and Noto 2024's M5.9 that came 13 s before the main shock. Imported JMA or P2PQuake reports bend the station dots to match each town's real reading, and waves travel on JMA2001, the travel-time table JMA itself uses
- Real ground in Japan: every station and town takes its site amplification from J-SHIS, so soft basins like the Kanto plain, Osaka and Nagoya shake harder and the mountains less
- A Problems panel on the timeline that catches what a real broadcast wouldn't do (a countdown that comes in late, a flash before its quake, a box covering a new quake, an EEW panel leaving early, reports after a cancel and more), with one-click fixes
- Flashes and reports step aside the way JMA viewers do it: a new quake, an EEW update or a cancel takes the screen, then they come back after a few seconds of quiet (or never, your call), and the timeline hatches each stretch they're away
- The EEW panel has JMA's estimated long-period class, the emergency warning (特別警報) and tsunami notes, single-station reports (単独点処理のため震度推定なし) and PLUM-only "shaking detected" reports, and reports can show an early magnitude, depth (ごく浅い) and max intensity before the final numbers came in
- Video export rendered frame by frame (not screen-recorded): a steady frame rate, H.264 + AAC in a plain MP4 that CapCut and TikTok's editor open cleanly, plus frame pictures, share codes and project files
- Your stuff on every device: settings, projects, sounds and fonts sync automatically through two secret gists on your GitHub account (paste a gist-only token once per device), or through your Claude account in the Claude version, and a backup file moves everything by hand
- Custom sounds for every alert, a sound per forecast shindo (so the EEW can sound different once it's a warning), and a different sound for each shindo level as the measured shaking climbs
- Custom fonts for the on-screen graphics: pick Google Fonts, a font installed on your computer, or import your own TTF, OTF, WOFF or WOFF2 files, separately for Japanese text, English text and numbers, each with its own size

Everything runs in the browser from one `index.html`. Nothing is real-time data: stations and shaking are simulated, and real replays combine the real facts (hypocenter, report, JMA's EEW reports where available) with that simulation.

Video files are written with [mp4-muxer](https://github.com/Vanilagy/mp4-muxer) (MIT). Ground amplification: J-SHIS, National Research Institute for Earth Science and Disaster Resilience (NIED), V4 site amplification factors (Vs400 to surface). Travel times: JMA2001 (Ueno et al., 2002), distributed by the Japan Meteorological Agency. EEW records: JMA, 緊急地震速報（警報）の発表状況.
