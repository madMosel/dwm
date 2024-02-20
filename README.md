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
- Mouse pointer gets set to the bar of the active monitor 
  when calling tagmon. This prevents the shifted whindow
  from being focused when it gets shifted into the mouse.
- Mouse pointer gets set to the bar of the focused monitor
  when calling focusmon.

