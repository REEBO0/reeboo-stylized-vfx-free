# REEBOO Stylized VFX - Free Sample

Three stylized effects for Godot 4.4+ made from shaders and GPU particles: `hit_spark`, `slash`
and `pickup_sparkle`. Licensed under MIT (see LICENSE in this folder).

## Quick start

```gdscript
const HIT_SPARK := preload("res://addons/reeboo_vfx/effects/hit_spark.tscn")

func _on_enemy_hit(hit_position: Vector3) -> void:
	VFXEffect.spawn(HIT_SPARK, get_tree().current_scene, hit_position)
```

- `hit_spark` and `slash` are one-shot and free themselves when done. `slash` swings along -Z.
- `pickup_sparkle` loops until you call `stop()` or free it.
- `VFXEffect` also has `play()`, `get_duration()`, `is_looping()`, a `finished` signal and the
  Inspector settings `autoplay`, `auto_free` and `time_scale`.
- Add a `WorldEnvironment` with Glow enabled for the best look.

Full documentation: https://github.com/REEBO0/reeboo-stylized-vfx-free

The full pack has 22 more effects: https://reebo0.itch.io/stylized-vfx-godot
