## Feel
- Animations: https://github.com/ocornut/imgui/issues/9102
## Window object utility
- configurable style, flags, etc.
- should the window only allow one of its kind open at a time
- should the window types all share location?
	- if user drags it around, they would expect any of the same type to re-open at the same spot
- should the window types all share size?
- configurable close window button
	- size
- kawase blur utility? or flag?

## Window Layout System
- Need sidebars or panels that can open up a main activity window
	- maybe main activity window area could be like tiling windows (hyprland), divides area
	
- USER TASKS:
	- non-draw mode
		- select agents (via panel click or clicking directly on agent object)
		- camera movement (pan + zoom)
			- ==this should be the default thing they're setup to do, no extra input beyond the actions==
	- draw mode
		- lasso selecting agents
		- drawing a tcm
	- setting up ttps
		- pre-emptively, not executing right away
		- going to execute one right away
			- don't care who takes
			- selected agents
- MUST BE VISIBLE AT ALL TIMES:
	- agent panel
		- toggle
			- minimal icon w/ name, health, battery, altitude
			- expanded
	- TTP bar
		- maybe hide/show based on user task focus
			- when editing tcm, can't use it anyways
	- notifications 
		- toggle
			- minimal icon w/ number
			- expanded list with msgs etc.


- A
	- (select agents)
	- draw tcm
	- (select agents)
	- make TTP
	- (select agents)
	- execute
- B
	- (select agents)
	- make TTP
	- (select agents)
	- draw tcm
	- (select agents)
	- execute
- C