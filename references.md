# reference

to reference a node in a tree of a scene, you can use `get_node("A")` or you can use `$` sign that is equivalent to a `get_node` .
`$A` ⇒ A is a child of a current scene
`$”…/A”` ⇒ sibling of a current scene
`$”root/Main/A”` ⇒ references A that is a child of a Main that is a top node of a scene tree
`onready var menu: Control = $HUD` (onready is a shorthand for a func _ready()

`get_node("AnimationPlayer").play("take_damage")`

```gdscript
$MainTheme.connect("finished", Callable(self, "_on_MainTheme_finished"))
$ButtonSound.play(0)
```

```gdscript
@onready var player_animation : AnimatedSprite2D = $PlayerAnimation
```
