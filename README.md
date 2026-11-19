# Fretboard Changes

A guitar practice tool for soloing over chord changes. One key's scale stays lit
across the neck while each chord's tones are highlighted in position, with a
synthesised backing band (chords, bass, drums, drone) that follows the
progression, key and tempo.

## Running it

It is one self-contained HTML file. Open `index.html` in any modern browser, or
serve the folder over HTTP:

    python3 -m http.server 8080    # then open http://localhost:8080

## Hosting

Any static host works - there is no build step and no backend. The only
external request is the Google Fonts stylesheet; without it the page falls back
to system fonts and everything still works.

**HTTPS matters for one feature.** The Listen mode uses `getUserMedia`, which
browsers only allow on a secure context: `https://`, `http://localhost`, or a
local `file://`. Served over plain HTTP from a LAN address the mic button will
be refused; everything else is unaffected.

## What is in here

Nothing but `index.html`. Audio is synthesised at runtime (Karplus-Strong
strings for guitar and bass, synthesised drum voices, a procedurally generated
convolution reverb), so there are no samples to ship.
