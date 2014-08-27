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
> name description can see fvwm manual-Font names and font loading
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
