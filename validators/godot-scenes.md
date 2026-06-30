# Godot Scene Design Validator

Validates that Godot scene design is sound, shippable, and easy to iterate.

check shallow_hierarchy - Scene tree is 5 levels or fewer deep.
check descriptive_node_names - Node names describe purpose, not only type.
check signal_based_communication - Nodes communicate via signals instead of long get_node chains.
check exported_tuning_vars - Gameplay and feel values are exposed with `@export`.
check appropriate_root_type - Root node matches behavior: `CharacterBody2D`, `Node2D`, `Area2D`, `Control`, or similar.
check collision_configured - Collision shape, layer, and mask match the intended interaction.
check group_membership - Dynamic nodes register with appropriate groups when group lookup is used.
check script_documentation - Each gameplay script has a brief purpose docstring or top comment.
check type_hints_public_api - Public methods and signal payloads use clear type hints.
check no_singletons_abuse - Autoloads are true globals, not convenience access to local scene state.
