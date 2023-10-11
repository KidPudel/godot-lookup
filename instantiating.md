# instantiating

1. with ui, just put in a tree and drag

2. with code:
  - scene reference (with `@export var ball: PacketScene` (and select a reference from the UI) or use `load` to get a reference to the packed scene `var ball = load(”res://instancing/Ball/tscn”)`
  - `instantiate()`
  - insert into a tree ⇒ `add_child()`


# delete from scene
`queue_free()`
Queues a node for deletion at the end of the current frame. When deleted, all of its child nodes will be deleted as well, and all references to the node and its children will become invalid

or you can delete from a parent node for example
```gdscript
TitleScene.queue_free()
```


