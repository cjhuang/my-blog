# FVWM #
---------

## Commands ##

> StaysOnTop, StaysOnBottom, StaysPut, Stick
>
> -geometry +-X+-Y, set the location, not for size
>
> Exec exec rxvt "*Desk:3"
>
> Xinerama
>
> If Xinerama support has been compiled into fvwm,
> it is used whenever fvwm runs on an X server that
> supports and uses multiple screens via Xinerama.
> Without this option, the whole desktop is treated
> as one big screen.
>
> WarpToWindow 50 50: warps the pointer to the center
> of the window.
>
> Font, IconFont, use in Style, MenuStyle, and DefaultFont commands, font
> name description can see fvwm manual-Font names and font loading.
> Some useful font utilities are: xlsfonts, xfontsel, xfd and xset.
> xfontsel is best
>
> Font Shadow Effects, Shadow=size [offset] [directions]]:, it only works
> with colorsets(Colorset)
>
>

## Command Expansion(1522) ##
> "$[...]", can used in Function
>
> $[0..9]

## Menu ##
> Style: AutomaticHotkeys
>
> Dynamic menu (2263)


# MissingSubmenFunction(2306) #

# MenuStyle(2666) #

# Miscellaneous Commands ##
> BugOpts [option [bool]], ...
>> This command controls several workarounds for bugs in third party programs.

> BusyCursor [Option bool], ...
>> This command controls the cursor during the execution of certain commands.

> ClickTime, ColorLimit, ColormapFocus

> <strong>CursorStyle</strong> context [num | name | None | Tiny | file [x y] [fg bg]]
> (2585)
>>  Defines a new cursor for the specified context.

> DefaultColors, DefaultColorset, DefaultFont, DefaultIcon, DefaultLayers

> Deschedule, Emulate

> FakeClick, FakeKeypress
>> This command is mainly intended for debugging fvwm and no guarantees are made that it works for you

> ImagePath path
>> Specifies a colon separated list of directories in which to search for images (both monochrome and pixmap).

> LocalePath path
>> Specifies a colon separated list of "locale path" in which to search for string translations.

> PrintInfo *subject* [verbose]
>> Print information on *subject* on stderr.

> Schedule [Periodic] delay_ms [command_id] command

> In Move Command, we can use relative position: left/top or right/bottom.
> More Move Command is in (4448)
>> OpaqueMoveSize [percentage]: Tells fvwm the maximum size window with which opaque window movement should be used.


## Window State ##
Stick, StickAcrossPages, StickAcrossDesks
but in Style they are Sitcy, StickyAcrossPages, StickyAcrossDesks

# Mouse, Key & Stroke Bindings #
IgnoreModifiers [Modifiers]
> Tells fvwm which modifiers to ignore when matching Mouse or Key bindings.

## EdgeCommand (5041) ##

## Key ##
could see /usr/include/X11/keysymdef.h or /usr/X11R6/lib/X11/XKeysymDB
(这个文件我的笔记本中没有)
> windows键在fvwm中对应的是Super_L(我的笔记本上只有一个，在左边),
> 键盘上那个在Alt_R和Ctrl_R之间的键为Menu
> 键盘上的Fn键名称为function，但fvwm不支持

## <font color=red>Menu Bindings</font> ##

## Mouse and Key ##
Mouse/Key [(window)] Button Context Modifiers Function

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
