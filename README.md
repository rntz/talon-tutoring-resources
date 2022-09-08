# Talon skills smorgasboard

This is a concise guide to the skills and command-sets you may wish to practice to get up and running as a Talon newbie.

**Core skills**: the keyboard, the mouse, repeater commands, text editing, dictation, window & app management, file system navigation, using the terminal, web browsing.

**Meta skills**: chaining commands, debugging, finding commands, talon scripting.

**Common issues**: speech.timeout too short/long, voice strain, difficulty avoiding the mouse.

# Core skills

See also [chaosparrot's talon practice website](https://chaosparrot.github.io/talon_practice/).

## The keyboard

This is defined in [misc/keys.talon](https://github.com/knausj85/knausj_talon/blob/main/misc/keys.talon) and [code/keys.py](https://github.com/knausj85/knausj_talon/blob/main/code/keys.py) but keys.py is pretty opaque to a talon newbie. You should memorize the [alphabet](https://chaosparrot.github.io/talon_practice/lessons/alphabet.html) and the other keys on the keyboard (enter, control, escape, etc).

- `go (up|down|left|right)+`: Presses a sequence of arrow keys.

- `(ship | uppercase) <letter>+ [lowercase|sunk]`: Inserts some uppercase letters, eg. `ship quench each drum` -> "QED". `sunk|lowercase` at the end lets you insert some lowercase letters afterward.

## The mouse

I don't discuss eyetracker commands here.

### [misc/mouse.talon](https://github.com/knausj85/knausj_talon/blob/main/misc/mouse.talon)

- `touch`, `righty`, `mid click`: Press the left, right, or middle mouse buttons.
- `<modifiers> (touch|righty)`: Clicks with modifiers, eg `shift touch`.
- `(dub|trip) click`: Double/triple click.
- `[left|right] drag`: Clicks and holds mouse button. Do `drag end | end drag` to end (`touch` also works).
- `wheel [tiny] (down|up)`: Scrolls the mouse wheel up/down.

## Repeater commands

### [misc/repeater.talon](https://github.com/knausj85/knausj_talon/blob/main/misc/repeater.talon)

- `second | third | fourth | ... | ninety ninth`: Repeat previous command several times. Eg. `go up third` will press up-arrow three times.
- `<number> times`: likewise, eg. `go up three times`.
- `twice | repeat that`: repeat previous command.
- `repeat that <n> [times]`: repeats previous command `n` times.

NB. `repeat that two [times]` is exactly the same as `third` or `three times`.

## Text editing

### [formatters.talon](https://github.com/knausj85/knausj_talon/blob/main/misc/formatters.talon)

- `say <phrase>`: Emits text, punctuated & capitalized.
- `phrase <phrase>`: Emits text, uncapitalized, and no punctuation recognized.
- `<formatter>+ <phrase>`: Formats text, useful for variable names when coding. For instance `snake hello world` inserts `hello_world`; `allcaps snake hello world` inserts `HELLO_WORLD`. Say `format help` to get a list of formatters with examples.

These all have `over` variants if you want to chain some commands *after* the phrase you're inserting, eg. `say hello over enter` inserts "hello" then presses enter.

- `word <word>`: Inserts a single word. Useful for chaining with subsequent commands.
- `scratch that`: Deletes what you've just inserted.
- `select that`: Selects the text you've just inserted.
- `<formatter> that`: Reformats the selection using the given formatter.


### [standard.talon](https://github.com/knausj85/knausj_talon/blob/000015ed1bd4cb1109d7d6ddaaa4146821821d70/misc/standard.talon)

- `(copy|cut|paste|undo|redo) that`: Standard copy/cut/paste/undo/redo commands.
- `file save`: Saves file.
- `slap`: Inserts an empty line below cursor, like going to end of line and hitting `enter`.


### [generic_editor.talon](https://github.com/knausj85/knausj_talon/blob/main/text/generic_editor.talon)

- `(go|select|clear|copy) word [left|right]`: moves, selects, deletes, or copies a single word. I suggest binding single word synonyms for `go word (left|right)` (I use `draw|step`) and `clear word (left|right)`.

- `go line (start|end)`: I suggest binding single-word synonyms for these, eg `head|tail`.

- `go (bottom | top)`: Go to bottom/top of file/document/text area.

- `select (left|right|up|down)`: Extends selection one character left/right or one line up/down.

- `(select|clear|copy|cut) line`: `clear line` is especially useful.

- `(select|copy|clear|cut) all`: Selects/copies/etc *everything* in the text area.

- `paste all`: Replace entire text area with results of pasting clipboard.


### [line_commands.talon](https://github.com/knausj85/knausj_talon/blob/main/text/line_commands.talon)

- `go <n> [end]`: Go to line `n`.
- `comment <n> [until <n2>]`: Comment lines `n` through `n2` inclusive.
- `(select|clear|copy|cut|paste|replace) <n> [until <n2>]`: Select/delete/copy/cut/replaces-by-pasting lines `n` through `n2` inclusive, or just `n` if `n2` omitted.
- `drag line (up|down)`: Move current line up/down.
- `clone line`: Duplicate current line.


There's more in each of these files; I highly suggest reading them if you want to get better. See also the entire [text](https://github.com/knausj85/knausj_talon/tree/main/text) directory.

## Dictation

## Window & application management

## File system navigation

## Using the terminal

## Web browsing


# Meta skills

## Chaining commands

## Debugging

## Finding commands

## Talon scripting


# Common issues

## Speech.timeout too short/long

## Voice strain

## Difficulty avoiding the mouse
