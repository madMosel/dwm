# dwm
my customized dwm build. 

original: 

    https://git.suckless.org/dwm/

	git clone git://git.suckless.org/dwm

#### ---- Config ------------------------------------------
- colors of border and dwmstatus are green instead of cyan
border is 3px istead of 1
- cycling monitors                        Shift + J/K
- shifting windows with focus to screen   CTRL  + J/K


#### ---- Features ----------------------------------------
- script execution on startup. Script location is defined 
in config.h
- hacky quickstarter: script defined in config.h is called
with the character position of ClkStatusText. This script 
works as Clickhandler. ClkStatusText is set by a second 
script (e.g quckstart-symbols + clock) that may be updated
periodically.
- tagfocusmon fuction to move window and focus.   

#### ---- Patched behavior -------------------------------
- Pointer gets set to the topbar of the active monitor when
calling tagmon

#### ---- Problems ----------------------------------------------
##### .... focusmon ..........................................

In a 3 monitor setup tagmon sometimes
shifts the focus with the window and sometimes not. Shifting
client from Monitor 0->1 drags the focus. Shifting form 2->1
drags the focus. Shifting from 1->0, 1->2, 0->2, 2->0 moves 
the client but focus remains on the monitor.

This is intendend behavior. It happened because of the mouse
was on monitor 1. If the window is shifted to the mouse pos
enternotify is called. This calls focus and the focus gets
shifted.

Dirty workaround is to move the pointer to the topbar 
programmatically to the bar in tagmon before is called. 
TODO oly do so if pointer in the way.
