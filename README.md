# dwm
my customized dwm build. 

original: 

    https://git.suckless.org/dwm/

	git clone git://git.suckless.org/dwm

#### ---- Config ------------------------------------------
- colors of border and dwmstatus are green instead of cyan
border is 3px istead of 1


#### ---- Features ----------------------------------------
- script execution on startup. Script location is defined 
in config.h
- hacky quickstarter: script defined in config.h is called
with the character position of ClkStatusText. This script 
works as Clickhandler. ClkStatusText is set by a second 
script (e.g quckstart-symbols + clock) that may be updated
periodically.
- tagfocusmon fuction to move window and focus. buggy.  

