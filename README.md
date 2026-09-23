# The Website That Goes Wrong

A single-page homage to *The Play That Goes Wrong* — a grand product launch, staged as a
live theatre broadcast, that falls **deliberately** and gloriously apart. Narrated by
**Barnaby Finch, Deputy Stage Manager** (Acting Head, "temporarily"), who insists
everything is under control while it demonstrably is not.

Controlled chaos: every malfunction is scripted, recoverable, and winking. Nothing
actually breaks — it just *looks* like it does.

## Run it

It's one self-contained file — no build, no dependencies, no backend.

```bash
open index.html            # macOS: opens in your default browser
# or serve it:
python3 -m http.server 8000   # then visit http://localhost:8000
```

## The arc

Interact with the page — click, type, drag, scroll — and the show escalates on its own,
then hitting **LAUNCH THE FUTURE** kicks off the full meltdown:

1. **Cold open** — the curtain isn't ready; Barnaby panics, then reveals the "polished" launch.
2. **Subtle unease** — the headline gets stage fright, the countdown counts *up*, the price gives up.
3. **Controls rebel** — the LAUNCH button flees your cursor, consent checkboxes multiply, validation rejects correct emails.
4. **The set turns** — the whole stage tilts, letters fall off, screws pop.
5. **System meltdown** — "Update 3,000,000", a Blue Screen of Just Kidding, a 147% progress bar.
6. **Total chaos** — the fourth wall falls over revealing backstage, Comic Sans takes over, the controls unionise and go on strike.
7. **The recovery that also goes wrong** — a velvet curtain sweeps in to fix it, then jams and tears.
8. **Curtain call** — an exhausted, sincere bow, undercut one last time, with absurd credits and an `ENCORE?`.

## How it's built

Vanilla HTML/CSS/JS in `index.html`. A small shared "chaos engine" (Barnaby's caption
system, a physics loop for falling elements, a confetti/pyro system, a WebAudio synth for
sound, screen-tilt and malfunction counters) drives ~25 individual gags wired on top of a
faux "corporate keynote" launch page. Respects `prefers-reduced-motion`.

`artifact.html` is a body-only build of the same page for hosting as a Claude Artifact;
it's generated from `index.html` and is not edited by hand.
