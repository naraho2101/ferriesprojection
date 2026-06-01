# Ferries Floor Game

An interactive floor-projection game for a Washington State Ferries waiting-area
installation. A single self-contained HTML file with all assets alongside it.

The whole UI is rotated 90° so it reads correctly when projected on the floor
and viewed from the side. Interactions use a "press & hold" model that mirrors
standing on a button on the projected floor.

## Run

Simplest — open the file in a browser:

```
open ferries_welcome.html
```

If your browser blocks the local video, serve the folder instead:

```
python3 -m http.server 8755
# then open http://localhost:8755/ferries_welcome.html
```

For the floor projector, click once anywhere to enter fullscreen, or press **F**
to toggle. **Esc** exits fullscreen.

## Screens

1. **Activate** — press & hold the "Begin" disc for ~1.5s.
2. **Home** — pick Play (game mode) or Learn (creature gallery).
3. **Preview** — 5-second look at the 3 random sea creatures to find this round.
4. **Game** — 2-minute round, click only the target creatures (other clicks show
   "wrong fish :("). Orca and blue whale are guaranteed to appear at least every
   15 seconds; salmon arrive as schools of 5–6.
5. **End** — final score, photo-booth QR, **Play again** / **Home**.
6. **Learn grid** — 8 creatures, click for details.
7. **Detail** — name, scientific name, facts, prev/next nav.

Every menu choice uses a 2-second hold-to-confirm (a progress ring fills at the
click point; releasing early cancels).

## Files

```
ferries_welcome.html      the entire app
assets/bg_video.mp4       30s underwater loop (background, crossfades seamlessly)
assets/c_*.png            8 creatures used in cards + swimming sprites
assets/c_orca_game.png    larger orca illustration used only in the swim layer
assets/orca_sticker.png   "Protect Our Oceans" sticker on the home Play card
assets/fig_*.png          background poster + Learn card icon
assets/end_qr.jpg         photo-booth QR shown on the end screen
assets/end_photo1.jpg     photo-booth sample selfie
assets/end_photo2.png     "Washington State" ocean photo frame (transparent middle)
```

## Hosting (GitHub Pages, optional)

If you want a live URL:

1. Rename `ferries_welcome.html` to `index.html`.
2. In the repo settings → Pages, serve from the `main` branch (root).
3. Open `https://<user>.github.io/<repo>/`.

## Credits

Design: Figma file *Arrowster – PRODUCT V2.0* (Ferries floor-game frames).
Built as a wizard-of-Oz prototype — there's no real foot/motion sensing; an
operator clicks on the operator screen and the projection reacts.
