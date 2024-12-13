# Swift SpriteKit Game - Angry Monkey

A physics-based casual game for iOS built with SpriteKit, featuring slingshot mechanics similar to Angry Birds with a monkey theme.

## Overview

This game demonstrates SpriteKit game development fundamentals including physics simulation, touch-based controls, and particle effects. Players launch a monkey character using a slingshot mechanic to destroy targets.

## Technologies

- **Language**: Swift
- **Framework**: SpriteKit, GameplayKit
- **Physics**: SpriteKit Physics Engine
- **Platform**: iOS (landscape orientation)

## Features

### Gameplay
- Slingshot launching mechanic with drag-to-aim
- Physics-based projectile motion with gravity
- Collision detection with destructible objects
- Particle effects for visual feedback

### Controls
- Touch and drag to aim
- Release to launch
- Pause/Resume functionality
- Visual guides showing launch trajectory

### Game Elements
- Monkey character sprite (128x128px)
- Various materials: wood, metal, brick
- Fire and ball particle effects
- Sound effects on launch

## Implementation

### Slingshot Physics
```swift
let angle = atan2(dy, dx)
let velocity = CGVector(dx: cos(angle) * force, dy: sin(angle) * force)
monkey.physicsBody?.velocity = velocity
```

### Physics Body Setup
```swift
let physicsBody = SKPhysicsBody(circleOfRadius: radius)
physicsBody.restitution = 0.3
physicsBody.friction = 0.5
physicsBody.categoryBitMask = PhysicsCategory.monkey
```

## Project Structure

```
My Game App/
├── GameScene.swift         # Main game logic
├── GameViewController.swift # Scene management
├── AppDelegate.swift       # App lifecycle
├── GameScene.sks           # Scene configuration
├── media/                  # Game assets
│   ├── monkey.png
│   ├── wood.png
│   ├── metal.png
│   └── ...
└── Actions.sks             # SKAction configurations
```

## Requirements

- Xcode
- iOS 10.0+

## License

MIT License

![Game Demo](https://github.com/The-Odd-Institute/Swift_SpriteGame_Angry_Monkey/blob/main/Swift_SpriteGame_Angry_Monkey.gif)
