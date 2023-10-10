You can think of signals as bloc in flutter they are being triggered ***by some event*** and emitting a value on a response to some event, and someone is listening to that emitting 

> (signals allow nodes communicate with one another) signal is a event callback function ⇒ like on collision we can decrease HP
We can connect signals using UI and scripts
> 

1. UI
select signal → press Connect.. **(WHO IS LISTENS?)** → choose a node in appeared window ⇒ this creates function on_NodeNameConnectingFrom_signalName (on_Button_pressed())

```tsx
func on_Button_pressed():
		set_proccess(not is_proccessing())
```

1. Script

```tsx
# name of my nodes (could be custom like SaveButton
onready var button: Button = $"..Button"
onready var timer: Timer = $Timer
# or
func _ready():
	# get timer and button nodes as a show case
	var timer = get_node("Timer")
	var button = get_node("..Button")
	# self == current node (self -> to which this singnal is attached to)
	# connecting a signal (connect to connect a signal)
	button.connect("pressed", self, "_on_Button_pressed")
	timer.connect("timeout", self, "_on_Timer_timeout")

func _on_Button_pressed():

func _on_Timer_timeout():
	// in UI toggle autostart
	visible = not visible

```

## Custom signals & emit

we can create a custom `signal` by using signal keyword

`signal health_changed(new_health)`

then to emit a signal

`emit_signal("health_changed", 98)` ← with a parameter

`func _on_HealthBar_health_changed(new_health)`

---

`emit_signal("getting_to_sleep")` 

`func _on_MadGuy_getting_to_sleep()`
