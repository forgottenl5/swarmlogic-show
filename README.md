# SwarmLogic: 1,000 drones, every path computed

▶ **[Watch on YouTube](https://youtube.com/shorts/-Dn2M6atL0Y)**

https://github.com/user-attachments/assets/7476cd54-97d3-4442-8cfa-1a91fef93a86
[Download full 1080p](hero_short_1080.mp4)

**Synthetic simulation. Time-lapse.** No real drones flew this, and the water, sky and lights are computer graphics.

## What you're watching

A 1,000-drone light show planned by SwarmLogic, a planning engine I'm building. I chose the shapes: a planet, a bird that flaps its wings, and a heart. Nobody keyframed the drone movements. The engine decides which drone goes where, and computes a smooth path for every drone between shapes.

What the engine does for each change of shape:

- **Assignment.** It solves exactly which drone should fly to which spot in the next shape, so that total travel is as short as possible.
- **Smooth motion.** Every drone accelerates and brakes smoothly, within set limits on speed and acceleration.
- **Spacing check.** Every pair of drones is checked at every time step, across the whole show.

## The numbers (from the engine's own checks on this show)

| | |
|---|---|
| Drones | 1,000 |
| Show length | 6 min 5 s (the video is sped up roughly 4–16×) |
| Closest any two drones ever get | 2.0 m (2.017 m) |
| Top speed | 4.0 m/s (limit 4.0) |
| Top acceleration | 1.98 m/s² (limit 2.0) |
| Spacing inside each shape | about 2.7 m |
| Collisions | 0 |

## What this is not

- **It is not a flight-ready show.** The simulation assumes perfect conditions: no wind, no GPS error, no radio dropouts, no battery limits. Real shows need far larger safety margins, testing, and approval from aviation authorities.
- **It is not real footage.** The scene is rendered in Blender.
- **The engine code isn't open source** at this time. This repository holds the video and this description only.

## More work

- [Shared Sky](https://github.com/forgottenl5/shared-sky): simulates Wing, Zipline and Amazon delivery drones sharing the sky over Houston and Dallas–Fort Worth, with pre-registered studies
- [ESC-Fault](https://github.com/forgottenl5/esc-fault-benchmark): a simulated benchmark for diagnosing faults in semiconductor wafer chucks

## License

Video: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You may share and adapt it with credit to "forgottenl5 / SwarmLogic".

Questions or licensing: [open an issue](https://github.com/forgottenl5/swarmlogic-show/issues).
