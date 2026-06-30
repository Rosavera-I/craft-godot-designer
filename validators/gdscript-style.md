# GDScript Style Validator

Validates that GDScript follows Godot 4 and project-local conventions.

check snake_case_variables - Variables and functions use `snake_case`.
check PascalCase_classes - `class_name` declarations and custom resource names use `PascalCase`.
check type_hints_public - Public API methods have argument and return type hints.
check signal_naming - Signals use concise past-tense or event names such as `hit`, `died`, `scored`, `health_changed`.
check enum_naming - Enums are `PascalCase`; values are also `PascalCase`.
check export_documented - Exported vars have tooltips, comments, or clear names that explain tuning intent.
check ready_pattern - Node references use `@onready` and include a null guard when the node is optional.
check const_convention - Constants use `SCREAMING_SNAKE_CASE`.
