# Chroma Shift

A fast-paced 3D puzzle platformer where you can switch between color dimensions, each with different physics and obstacles.

## How to Play

**Objective**: Navigate through dimensions, collect crystals, and reach the golden goal platform!

### Controls

**Desktop:**
- **WASD / Arrow Keys**: Move player
- **Space**: Jump
- **1**: Red Dimension (gravity reversed - float up!)
- **2**: Blue Dimension (slow motion)
- **3**: Green Dimension (normal gravity)
- **R**: Restart level

**Mobile:**
- **Joystick**: Move player
- **Dimension Buttons**: Switch dimensions

### Dimensions

| Dimension | Key | Effect | Color |
|-----------|-----|--------|-------|
| Red | 1 | Reversed gravity (float upward) | Pink/Magenta |
| Blue | 2 | Slow motion | Cyan |
| Green | 3 | Normal gravity | Lime Green |

### Gameplay Tips

- Some platforms only exist in certain dimensions!
- Red dimension platforms float upward - use them to climb
- Blue dimension slows your fall - great for precision landings
- Combine dimensions to solve puzzles and reach the goal

## Tech Stack

- **Three.js** - 3D rendering
- **Post-processing** - Bloom effects
- **Web Audio API** - Sound effects

## Play Online

[Chroma Shift - Live Game](https://nishivector.github.io/chroma-shift/)

## Development

Built as a single HTML file for easy deployment and sharing.

```bash
# To run locally
cd games/chroma-shift
python -m http.server 8000
# Then open http://localhost:8000
```

## License

MIT
