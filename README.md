# Tide Simulator

An interactive tide simulator for the classroom, a companion to the
[Moon Phase Simulator](https://fractalated.github.io/moon-phase-simulator/). Move the
Moon around Earth and watch the ocean bulges, the water at one harbor, and the
monthly spring–neap cycle all change together.

**[Open the simulator →](https://fractalated.github.io/tide-simulator/)**

## What it does

- **Three linked views.** A top-down view of Earth's tidal bulges and the
  Moon's orbit. A side view of a harbor tide staff with a floating boat. A chart
  of a whole lunar month of tides. Change one and the others follow.
- **Spring and neap tides you can see.** The month chart shades the spring
  tides at new and full moon and the neap tides at the quarter moons. A dashed
  envelope shows the tidal range growing and shrinking.
- **"Show me a tide" presets.** One click jumps to a neap, normal or spring
  high or low tide, so students can compare them side by side. Neap is set at
  first quarter, spring at full moon, and normal halfway between. Each button
  picks the high or low nearest midday on that day.
- **Turn each pull on or off.** Switch off the Sun and every day has the same
  range, so there is no spring–neap cycle. Switch off the Moon and you get a
  weaker solar tide with highs at noon and midnight.
- **The hours around now.** A zoomed chart labels each high and low with its
  time, with night shaded, so you can see two tides a day that run about 50
  minutes later each day.
- **Scrub or play.** Drag the Moon, drag the slider, click or drag on the month
  chart, or jump to new, first quarter, full or last quarter. Play at *Hours*
  speed (3 h per second) or *Days* speed (1 day per second).
- **Opens on right now.** The page loads at the current moon age and your
  local clock time.

## Misconceptions it is built to address

1. There are two bulges, not one. The far-side bulge comes from the Moon
   pulling Earth's center harder than it pulls the far ocean.
2. "Spring" tides have nothing to do with the season. They happen twice a month.
3. The Sun's pull is stronger than the Moon's, but its tidal effect is smaller
   (about 46%), because tides depend on the *difference* in pull across Earth.
4. High tide isn't at the same time every day. It comes about 12 h 25 min
   after the last one.

## Accuracy, honestly

This is the **equilibrium tide**: an Earth covered entirely in ocean, with the
bulges lined up exactly under the Sun and Moon. Real coasts are shaped by
continents and ocean basins. On real coasts:

- high tide lags the Moon by hours, and spring tides often arrive 1–2 days
  after new or full moon;
- ranges vary from a few centimetres to over 15 m (Bay of Fundy);
- the Moon's tilt makes one of the day's two highs bigger than the other (the
  diurnal inequality). This model leaves that out;
- the Moon's changing distance adds extra-high perigean "king tides". This
  model leaves that out too.

Heights assume a 1.0 m lunar tide and a 0.46 m solar tide. That gives a
spring range of about 2.9 m and a neap range of about 1.1 m. The moon age uses
the same mean synodic month as the Moon Phase Simulator. For real predictions at a
real place, use [NOAA Tides & Currents](https://tidesandcurrents.noaa.gov/).

## Running it

One file, no build step, no dependencies. Open `index.html`, or:

```bash
python3 -m http.server 8000
```

The only network request is a Google Fonts stylesheet. Without it, the page
falls back to system fonts.

## License

MIT, see [LICENSE](LICENSE).
