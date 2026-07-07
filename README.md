<p align="center">
  <img src="logo.svg" alt="aislop" width="500" />
</p>

# aislop

A curated collection of AI-built alternatives to everyday tools and applications.

Every entry is a **single, self-contained HTML file** — open it in a browser and it just runs.
No build step, no accounts, no servers: all logic lives in vanilla JavaScript using standard
browser APIs (Canvas, WebCrypto, MediaRecorder, `localStorage`, …), with Tailwind and Font Awesome
pulled from a CDN purely for styling. Unless noted, your data never leaves the page.

| | Replaces | Under the hood | Est. cost avoided |
|---|---|---|---|
| [FlipGlide Studio Pro](FlipGlide-Studio-Pro.000.002.000.html) ([Try](https://7bp.github.io/aislop/FlipGlide-Studio-Pro.000.002.000.html)) — canvas animator with import/export | FlipaClip | Frame-by-frame `<canvas>` drawing with onion-skinning; frames played in sequence and exported via file APIs | ~$36/yr (Plus) |
| [AetherFlow](AetherFlow.000.001.000.html) ([Try](https://7bp.github.io/aislop/AetherFlow.000.001.000.html)) — gamified focus timer | Forest | Pomodoro timer driven by timestamps/`setInterval`, streak state in `localStorage` | ~$4 one-time |
| [QRCode Labs](QRCodeLabs.000.001.000.html) ([Try](https://7bp.github.io/aislop/QRCodeLabs.000.001.000.html)) — QR generator &amp; reader | Qrafter | Renders QR codes to canvas and scans them from the live camera via `getUserMedia` | ~$4 one-time |
| [Continuum](Continuum.000.001.001.html) ([Try](https://7bp.github.io/aislop/Continuum.000.001.001.html)) — one-person whiteboard | Miro | Infinite pan/zoom canvas with notes &amp; shapes; board serialized to JSON for import/export | ~$96–192/user/yr |
| [OmniHorizon](OmniHorizon.000.001.000.html) ([Try](https://7bp.github.io/aislop/OmniHorizon.000.001.000.html)) — project-style todo lists | OmniFocus | GTD-style nested projects/tasks persisted to `localStorage` | ~$75 one-time or ~$100/yr |
| [Conclave](Conclave.000.001.000.html) ([Try](https://7bp.github.io/aislop/Conclave.000.001.000.html)) — multi-persona AI group chat (BYOK) | Character.ai | Calls an LLM API with your own key; personas &amp; conversation held in-browser | ~$120/yr (+ your token usage) |
| [Reelight](Reelight.000.001.000.html) ([Try](https://7bp.github.io/aislop/Reelight.000.001.000.html)) — screen &amp; camera recorder | Loom | `getDisplayMedia` + `getUserMedia`, canvas compositing for the webcam bubble, Web Audio mixing, `MediaRecorder` → WebM | ~$150–180/user/yr |
| [Quire](Quire.000.001.000.html) ([Try](https://7bp.github.io/aislop/Quire.000.001.000.html)) — private PDF studio | Smallpdf | `pdf.js` renders page thumbnails; `pdf-lib` assembles merged/reordered/rotated output — all client-side | ~$108–144/yr |
| [Plume](Plume.000.001.000.html) ([Try](https://7bp.github.io/aislop/Plume.000.001.000.html)) — image compressor &amp; converter | TinyPNG | Decodes to `<canvas>` and re-encodes via `canvas.toBlob` (WebP/JPEG/PNG) with quality + resize; strips metadata | ~$39/yr (beyond free quota) |
| [Bastion](Bastion.000.001.000.html) ([Try](https://7bp.github.io/aislop/Bastion.000.001.000.html)) — offline password vault | 1Password | WebCrypto PBKDF2-SHA256 (250k iters) → AES-256-GCM; vault encrypted at rest, master password never stored | ~$36–48/yr |
| [Tally](Tally.000.001.000.html) ([Try](https://7bp.github.io/aislop/Tally.000.001.000.html)) — invoice builder | FreshBooks | Live totals with `Intl.NumberFormat` + tax/discount math; profile &amp; invoices in `localStorage`; PDF via print stylesheet | ~$200+/yr |
| [Inkling](Inkling.000.001.000.html) ([Try](https://7bp.github.io/aislop/Inkling.000.001.000.html)) — screenshot annotator | Snagit | Full-res `<canvas>` markup with vector shape objects + undo/redo; pixelate-region redaction; PNG or clipboard export | ~$40–63 one-time |
| [Chroma](Chroma.000.001.000.html) ([Try](https://7bp.github.io/aislop/Chroma.000.001.000.html)) — color palette studio | Coolors | HSL harmony generation, WCAG relative-luminance contrast, palette encoded in the URL hash for sharing | ~$36–60/yr |
| [Tempo](Tempo.000.001.000.html) ([Try](https://7bp.github.io/aislop/Tempo.000.001.000.html)) — time tracker | Toggl | Timestamp-based timers with live `setInterval` updates, projects, weekly aggregation, CSV export — all in `localStorage` | ~$108–120/user/yr |
| [Ember](Ember.000.001.000.html) ([Try](https://7bp.github.io/aislop/Ember.000.001.000.html)) — habit &amp; streak tracker | Streaks | Streak logic over per-day completion sets, GitHub-style heatmap, weekday schedules &amp; a daily progress ring — all in `localStorage` | ~$5 one-time (or Habitica ~$60/yr) |
| [Trellis](Trellis.000.001.000.html) ([Try](https://7bp.github.io/aislop/Trellis.000.001.000.html)) — kanban board | Trello | Drag-and-drop cards across lists (HTML5 DnD with drop-index math), labels, due dates, search &amp; JSON export/import — board in `localStorage` | ~$60–120/user/yr |
| [Quorum](Quorum.000.001.000.html) ([Try](https://7bp.github.io/aislop/Quorum.000.001.000.html)) — scrum planning poker (**multiplayer**) | Planning Poker Online | Real-time rooms over **WebRTC** via PeerJS's free public broker (peer-to-peer, host-authoritative) — multiple decks, votes hidden until reveal, avg/median/consensus stats, spectators; no backend of ours | ~$60–100/user/yr |
| [Hindsight](Hindsight.000.001.000.html) ([Try](https://7bp.github.io/aislop/Hindsight.000.001.000.html)) — team retrospective board (**multiplayer**) | EasyRetro | Real-time retro over **WebRTC** via PeerJS (host-authoritative) — Start/Stop/Continue &amp; other templates, live add/edit/vote/delete cards, "hide until reveal" masking (per-recipient state), phase timer &amp; Markdown export | ~$100–300/yr (team) |
| [Beam](Beam.000.001.000.html) ([Try](https://7bp.github.io/aislop/Beam.000.001.000.html)) — peer-to-peer file transfer (**multiplayer**) | WeTransfer | Chunked binary over **WebRTC** data channels (16 KB chunks + `bufferedAmount` backpressure) in a full peer **mesh** via PeerJS — files go device-to-device, never through a server; any size; QR invite &amp; text beam too | ~$120/yr (Pro) |
| [Papertrail](Papertrail.000.001.000.html) ([Try](https://7bp.github.io/aislop/Papertrail.000.001.000.html)) — document scanner | CamScanner | `getUserMedia` camera capture + canvas image processing (grayscale, **Otsu** adaptive B&amp;W, auto-levels enhance), multi-page rotate/reorder, exports to A4 PDF via `pdf-lib` or JPGs — all on-device | ~$50/yr |
| [Codex](Codex.000.001.000.html) ([Try](https://7bp.github.io/aislop/Codex.000.001.000.html)) — universal code scanner &amp; analyzer | Scanbot | **ZXing** decodes QR, EAN/UPC, Code128/39, ITF, Data Matrix, PDF417 &amp; Aztec from camera or image; classifies content (URL, Wi-Fi, vCard, geo, email, product #…), extracts fields, shows raw **bytes/hex**, plus a Morse encoder/decoder with audio | ~$10–30/yr (ad-free apps) |
| [Thump](Thump.000.001.000.html) ([Try](https://7bp.github.io/aislop/Thump.000.001.000.html)) — beat machine / step sequencer | Groovepad | **Web Audio API** synthesizes every drum voice live (kick/snare/clap/hats/tom/rim/cowbell) — no samples; a look-ahead scheduler keeps tight timing with swing &amp; presets, and an `OfflineAudioContext` renders your beat to a downloadable 16-bit **WAV** | ~$10–40/yr (pro packs) |

Swapping the subscription tools above for these clones adds up to **well north of ~$1,000/year** in
avoided recurring fees for a typical solo user — before counting the one-time-license tools.

---

### ⚠️ Disclaimer

These are **AI-generated, single-file hobby clones**, provided **as-is with no warranty** of any
kind. They implement the common-case features of the tools they reference — not every capability, edge
case, or guarantee of the originals — and should not be relied upon for critical, sensitive, or
business-critical data without your own review and backups.

The **"estimated cost avoided"** figures are rough, list-price approximations for a typical paid tier
around 2025. Real prices vary by plan, seat count, region, currency, promotions, and change over time,
and most of the originals also offer free tiers — treat the numbers as illustrative, not financial
advice. Nothing here is affiliated with, endorsed by, or an official replacement for any named product,
and all product names and trademarks belong to their respective owners.
