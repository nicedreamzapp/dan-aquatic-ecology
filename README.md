# Dan Close · Aquatic Ecology & Restoration

> An **HSU Master's Thesis Project** at **Cal Poly Humboldt · Marine Sciences**.
> Four single-page features on aquatic ecology, restoration ecology, and scientific diving — built with [Claude Code](https://claude.com/claude-code) (Anthropic's AI coding CLI).

🎥 **[Watch the 1-min video walkthrough](https://youtu.be/clXORLW3_1I)**

🌐 **[Live site](https://nicedreamzapp.github.io/dan-aquatic-ecology/)**

---

## What's in it

| | Feature | What it covers |
|---|---|---|
| 🌊 | **[Aquatic Ecology](dan-aquatic-ecology.html)** | "From Molecules to Whales" — eleven orders of magnitude on one screen. Scale-of-the-Sea hero auto-cycles 10 ticks (water molecule → bacterium → phytoplankton → copepod → jellyfish → sardine → tuna → great white → orca → blue whale). Vertical depth tour with click-to-learn modals on every layer. |
| 🌊 | **[Marine Restoration](dan-restoration-ecology.html)** | A thesis-quality slide tour: coral fragmentation & microfragmentation, mangrove EMR, oyster reef recovery, seagrass blue-carbon, kelp forests, salt-marsh living shorelines, MPAs and the 30×30 target. |
| 🏞 | **[Freshwater Restoration](dan-freshwater-restoration.html)** | Beavers as ecosystem engineers, BDAs, dam removal, stream channel work, riparian zones, floodplain reconnection, eutrophication recovery, urban green infrastructure. |
| 🤿 | **[Scientific Diving](dan-scientific-diving.html)** | A 13-chapter narrative on the credentialed divers (AAUS, NOAA, Smithsonian) who actually do restoration underwater. Transects, photogrammetry, microfragmentation, lionfish culling, the rigor. |

The hub at `index.html` ties them all together with animated SVG previews.

## How it was built

Every page is **a single HTML file** — inline CSS, inline JavaScript, inline SVG. No build step, no npm, no tracking, no API keys. You can email or AirDrop any file and it just works.

Features:
- **Hand-coded SVG animation.** Every organism, every diver, every tool, drawn in code.
- **Built-in narration.** Each feature page has a 🎧 button. A tiny local Flask service ([`fia-tts/`](https://github.com/nicedreamzapp/dan-aquatic-ecology)) wraps `edge-tts` to call Microsoft's free Edge neural-voice backend (Ava) and serve cached MP3s. Falls back to the browser's Web Speech API when the service isn't running.
- **Built with Claude Code.** ~6,000 lines of HTML/CSS/JS, all written and iterated through Claude Code (Opus 4.7).
- **The YouTube video** was assembled by Claude too — Playwright headless Chromium recording at 1920×1080, ffmpeg concat / fade / audio mixing.

## Try it locally

```bash
git clone https://github.com/nicedreamzapp/dan-aquatic-ecology
cd dan-aquatic-ecology
open index.html
```

Or just download any one HTML file and double-click it.

## Optional: run the narration server

```bash
python3 -m venv venv && source venv/bin/activate
pip install edge-tts flask flask-cors
python server.py     # listens on 127.0.0.1:9200
```

Then any page's 🎧 button will speak in Ava's full neural voice.

## Credits

- **Author**: Dan Close — HSU Master's Thesis, Cal Poly Humboldt Marine Sciences
- **Built with**: [Claude Code](https://claude.com/claude-code) (Anthropic, Opus 4.7)
- **Photos**: [Wikimedia Commons](https://commons.wikimedia.org/) (public domain / CC)
- **Voices**: Microsoft neural voices via [`edge-tts`](https://github.com/rany2/edge-tts) (free, no API key)

## License

MIT. Use, remix, share — credit Dan Close where you can.
