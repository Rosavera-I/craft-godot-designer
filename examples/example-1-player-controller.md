# Behavior Contract: 2D Player Controller

## Context

Platformer with `CharacterBody2D`, Forward+ renderer, and Godot 4.4.

## Design Checklist

### Movement

- `max_speed`: `300.0`
- `acceleration`: `1500.0`
- `friction`: `800.0`
- `gravity`: `1200.0`
- `jump_velocity`: `-450.0`

### Feel

- Coyote time: `0.15s`
- Jump buffer: `0.15s`
- Squash and stretch on land
- Dust particles on jump and land

### State Machine

States: `Idle`, `Run`, `Jump`, `Fall`, `Land`

Transitions:

- `Idle -> Run` on horizontal input.
- `Run -> Jump` on jump pressed.
- `Jump -> Fall` when `velocity.y > 0`.
- `Fall -> Land` when `is_on_floor()`.
- `Land -> Idle` after landing animation.

## Scene Structure

```text
Player (CharacterBody2D)
├── Sprite (AnimatedSprite2D)
├── Collision (CollisionShape2D)
├── GroundCheck (RayCast2D)
├── StateMachine (Node)
└── VFX (Node2D)
```

## Signals

- `jumped`
- `landed(impact_velocity: float)`
- `state_changed(previous: StringName, current: StringName)`

## Next Smallest Step

Add `Player.tscn` with a `CharacterBody2D` root, typed exported movement values, and basic horizontal movement in `_physics_process`.
