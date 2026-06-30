Before designing or coding, inspect:

1. `project.godot`: engine version, renderer, display settings, input map, and autoloads.
2. Scene structure: existing `.tscn` files, their roots, ownership, and organization.
3. Autoloads: registered singletons, responsibilities, and whether they are true globals.
4. Script patterns: code style, base classes, signals, exported values, and state patterns.
5. Resources: custom `Resource` classes, `.tres` files, import settings, and data ownership.
6. Physics layers: collision layer and mask configuration, named meanings, and expected interactions.

Ask: "What are the 3 most important things to preserve in this change?"
