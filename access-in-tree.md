To access a node in a tree, simply use `get_node("YourNode")` or even better `$YourNode`
**child** => `$YourNode`
**siblings** => `$"../YourNode"`

to get something from a project you can also use `full/path`


```gdscript
$MainTheme.connect("finished", Callable(self, "_on_MainTheme_finished"))
#ButtonSound.play(0)
```
