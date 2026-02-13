# CS2053 - Concept Assignment 1
## Abhishek Haribasker

---

**1**:
Answer here

**2-a**:
_ready: Its called once when a node and all its children enter the scene tree. It’s for initialization.

_process: It calls every frame. It is used for non-physics tasks like UI updates or timers.

_physics_process: It is used for physics-related tasks like movement or collisions. It occurs at a fixed frequency.

Order: _ready first. Then _physics_process. Then, _process.

**2-b**:
These functions are used to iterate through all active nodes so that we don't have to write the while loop manually.

**2-c**:
_ready: It cannot be triggered again naturally unless we add the node to the tree again.

_process: Frequency depends on hardware performance. We can't control it, but we can toggle it off using set_process(false).

_physics_process: Frequency is fixed.

**3**:
Buffering is commonly used to prevent screen tearing and flickering. Someone might want to disable it to reduce input latency.

**4**:
The sprite-sheet equivalent for large, static things like environment are called Tile Maps. Tile Sets are where every object is referenced.

**5-a**:
(6,6)

**5-b**:
var pos1 = Vector2(2, 2)
var pos2 = Vector2(8, 8)
var diff = pos2 - pos1
var direction = diff.normalized() 

**6**:
To solve the above problem, we first get Target vector T.
T = E - C, where C is the character position and E is the explosion position.
Then, we get dot product.
d = T.R, where R is a vector.

Then, to determine the speaker:
If d > 0: The explosion is to the right; play sound in the right speaker.
If d < 0: The explosion is to the left; play sound in the left speaker.
If d = 0: The explosion is centered.

**7-a**:
Answer here

**7-b**:
Answer here

**8-a**:
Answer here

**8-b**:
Answer here

**8-c**:
Answer here

**8-d**:
Answer here

**9**:
Answer here

**10**:
Answer here


---
