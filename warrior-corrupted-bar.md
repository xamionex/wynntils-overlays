Only shows cooldown since there's a built in bar for corrupted
All values are supposed to be copy pasted

### Color
```
from_hex("b200ff")
```
### Text
```
{concat("⌚ "; str(int(value(status_effect_duration("Corrupted")))); "s")}
```
### Value
```
capped(value(status_effect_duration("Corrupted")); 11)
```
### Enabled
```
and(status_effect_active("Corrupted"); less_than(value(status_effect_duration("Corrupted")); 11))
```
