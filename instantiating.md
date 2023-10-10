# instantiating

1. with ui, just put in a tree and drag

2. with code:
  1. scene reference (with `@export var ball: PacketScene` (and select a reference from the UI) or use `load` to get a reference to the packed scene `var ball = load(”res://instancing/Ball/tscn”)`
  2. instantiate()
  3. insert into a tree ⇒ add_child
