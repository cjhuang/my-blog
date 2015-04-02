If Function is '--', it indicates that the event should be propagated to
the specified window to handle.

Context
+ R for the root window
+ W fot an application window
+ D for a desktop application (as kdesktop or Nautilus desktop)
+ T for a window title-bar
+ S for a window side, top, or bottom bar
+ '[', ']', '-' and '_' for the left, right, top or bottom side only
+ 'F' for a window frame (the corners)
+ '<', '^', '>' and 'v' for the top left, top right, bottom right or bottom left corner
+ 'I' for an icon window
+ '0' through '9' for title-bar buttons
+ 'A' is for any context
+ The special context 'M' for menus can be used to (re)define the menu controls.  It can be used alone or together with 'T', 'S', 'I', '[', ']', '-' and '_'.

Modifiers
+ N -- no modifiers
+ C -- for control
+ S -- for shift
+ M for Meta in Mac and Alt in Windows or Linux
+ L for Caps-Lock
+ A for any modifier
