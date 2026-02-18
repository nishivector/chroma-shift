# Chroma Shift - Game Specification

## 1. Project Overview
- **Name**: Chroma Shift
- **Type**: 3D Puzzle Platformer
- **Core Functionality**: A fast-paced puzzle platformer where players switch between color dimensions, each with different physics (gravity, obstacles)
- **Target Users**: Casual gamers who enjoy puzzle-platformers

## 2. Visual & Rendering Specification

### Scene Setup
- **Camera**: Third-person follow camera, smooth lerp tracking
- **Lighting**: 
  - Ambient light (intensity 0.4)
  - Directional light from above-front (intensity 0.8)
  - Point lights that change color based on dimension
- **Environment**: Dark background with grid floor, subtle fog for depth

### Materials & Effects
- **Player**: Glowing sphere with emissive material
- **Platforms**: 
  - Red dimension: Upward gravity platforms (pink/magenta)
  - Blue dimension: Slow-time platforms (cyan)
  - Green dimension: Solid platforms (lime green)
- **Post-processing**: Bloom effect for glowing elements

### 3D Assets
- Player: SphereGeometry (radius 0.5)
- Platforms: BoxGeometry (various sizes)
- Collectibles: OctahedronGeometry (rotating)

### Color Palette
- Red Dimension: #ff0066, #ff66b2
- Blue Dimension: #00ffff, #0066ff
- Green Dimension: #00ff66, #66ff00

## 3. Simulation Specification

### Physics
- **Gravity**: Variable based on dimension
  - Red: gravity = -2 (floats up)
  - Blue: gravity = 0.5 (slow fall)
  - Green: gravity = -9.8 (normal)
- **Player Movement**: WASD/Arrow keys, smooth acceleration
- **Jump**: Spacebar, dimension-dependent jump height

### Dimension Mechanics
- Press 1: Red Dimension (gravity reversed)
- Press 2: Blue Dimension (slow motion)
- Press 3: Green Dimension (normal gravity)
- Cooldown: 0.5s between switches

## 4. Interaction Specification

### User Controls
- **WASD / Arrow Keys**: Move player
- **Space**: Jump
- **1/2/3**: Switch dimensions
- **R**: Restart level
- **Touch**: Virtual joystick (mobile)

### UI Elements
- Current dimension indicator (top-left)
- Score/collectibles counter (top-right)
- Dimension cooldown indicator

### Audio
- Dimension switch: Synth whoosh (Tone.js)
- Collectible pickup: Bell tone
- Background: Ambient synth pad

## 5. Gameplay Loop
1. Player spawns in Green dimension
2. Navigate platforms, collect crystals
3. Switch dimensions to solve puzzles (some platforms only visible in specific dimensions)
4. Reach goal platform to complete level
5. Score based on time and collectibles

## 6. Acceptance Criteria
- [ ] Player can move and jump in 3D space
- [ ] Three dimensions with distinct physics
- [ ] Visual feedback when switching dimensions
- [ ] Collectible crystals that increment score
- [ ] Goal platform triggers level completion
- [ ] Works on desktop (keyboard) and mobile (touch)
- [ ] Smooth 60fps performance
- [ ] Bloom post-processing for glow effect
