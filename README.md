# The Website That Goes Wrong

A product launch, staged as live theatre — and **you're the Deputy Stage Manager**.

The top of the screen is the stage: a slick launch website built out of plywood and hope.
The bottom is your prompt desk: the prompt book, a cue light, and a big green **GO**.
The show only moves when you call it. Every cue goes wrong. The wreckage piles up on
stage. And at the final curtain, everything that fell off flies back into place — and the
prompt book reveals that every single disaster was rehearsed.

Controlled chaos: nothing on this page actually breaks. It all goes wrong *rightfully*.

## Run it

One self-contained file, no build, no dependencies.

```bash
open index.html
```

## How to play

- Wait for the lamp to say **STANDBY**, then press **GO** (or Space / Enter).
- Some cues need a hand from the audience — press the swinging PRE-ORDER button, waft the
  haze, find the mains switch by torchlight. If you don't, the crew covers for you.
- Calling GO while a cue is still running is an *unscheduled incident*. It goes on your
  show report.
- **CANS** turns on sound (off by default).

## The running order

| Cue | Supposed to | Actually |
| --- | --- | --- |
| FLY 1 | Curtain flies out | Sticks, drops, flies — and the counterweight lands on stage |
| LX 2 | Spot finds Barnaby | Finds a wall, the sandbag, another wall… then Barnaby |
| FLY 3 | Title flies in | Arrives alphabetically, sorts itself out, loses its E |
| VID 4 | Product film | No signal, the DVD logo (it hits the corner), Barnaby's holiday |
| SND 5 | Fanfare | Doorbell. Then a sad trombone ("deliberate") |
| LX 6 | Price reveal | A slot machine. Three lemons |
| FLY 7 | Pre-order button | Flies in on one wire and swings — you can still press it |
| REV 8 | Every angle | The back of the set, and Kevin's sandwich |
| FX 9 | Gentle haze | Not gentle. Waft it away |
| LX 10 | Warm wash | Trips the mains. You hold the torch |
| PYRO 11 | Confetti on "pride" | Fires on "great", sideways, and takes out a lantern |
| SET 12 | The set holds | It does not |
| FLY 13 | Final curtain | Perfect. Everything goes home. Exactly as rehearsed |

## How it's built

Vanilla HTML/CSS/JS in `index.html`. The set is a fixed 1000×600 stage scaled to fit,
so every fall, swing and spotlight is choreographed in one coordinate space. A small
engine (a cue runner, surtitles, headset chatter, a single lighting overlay, a physics
loop for debris, a particle system, and a WebAudio synth) drives thirteen cues written as
plain async functions. Respects `prefers-reduced-motion`.
