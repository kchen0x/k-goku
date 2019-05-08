# k-goku

A configuration using GokuRakuJoudo to generate Karabiner profile.

## What is Karabiner?

[Karabiner](https://pqrs.org/osx/karabiner/) is a powerful and stable keyboard customizer for macOS.

- You can re-map any key without any restriction. 
- You can accelerate speed of the key repeat. Karabiner offers frequently used settings. 
- You can activate them by simply clicking the checkbox in the list. If the settings which you want are not in the list, you can add them by yourself. 

Karabiner has many useful features for efficient keyboard operations. 

- You can do Emacs-style operations anywhere. 
- You can do Vi-style operations anywhere. You can do Mouse operations from keyboard.

You can do everything by modifying your keyboard!

## What is GokuRakuJoudo?

[Goku](https://github.com/yqrashawn/GokuRakuJoudo) is a tool to let you manage your Karabiner configuration with ease.

Karbiner Elements uses JSON as it's config file. This leads to thousands lines of JSON (sometimes over 20,000 lines). Which makes it really hard to edit the config file and iterate on your keymap.

Goku use the [edn format](https://github.com/edn-format/edn) to the rescue.

## What is k-goku

k-goku is a configuration using GokuRakuJoudo to generate Karabiner profile, which provides a set of handy personal customised rule. ☺

### Hyper Mode

Hyper mode is the way to take full use of CapsLock key. When `CapsLock` is pressed down, the hyper mode will be actived fot next action, and it will send `Escape` key when pressed alone.

#### Hyper Mode - Control

Hyper mode can be used as a `ctrl` key where it's mostly used in terminal for:

| key | effect                                      |
|-----|---------------------------------------------|
| `a` | tmux prefix                                 |
| `c` | kill a process with signal SIGINT           |
| `z` | suspend a process by sending it the SIGTSTP |
| `d` | `exit()` from the command                   |

#### Hyper Mode - Navigation [VI style]

It allow you to use VI style cursor movement.

| key | effect                 |
|-----|------------------------|
| `h` | move left              |
| `j` | move down              |
| `k` | move up                |
| `l` | move right             |
| `w` | move one word forward  |
| `b` | move one word backward |

When `cmd ⌘` is pressed, you can select the text when moving the cursor.

When `opt ⌥` is pressed, the mouse pointer will be moved instead.

#### Hyper Mode - Mousekey

Simulate the mouse pointer with arrow key.

| key   | effect                                  |
|-------|-----------------------------------------|
| `←`   | pointer move left                       |
| `→`   | pointer move right                      |
| `↑`   | pointer move up                         |
| `↓`   | pointer move down                       |
| `↵`   | left click on mouse                     |
| `⌘ ↵` | right click on mouse (contexture click) |

#### Hyper Mode - Deletion

Delete text with ease.

| key   | effect                                          |
|-------|-------------------------------------------------|
| `n`   | delete a word backward                          |
| `m`   | delete a letter backward                        |
| `,`   | delete a letter forward                         |
| `.`   | delete a word forward                           |
| `⌘ n` | delete from cursor to the beginning of the line |
| `⌘ m` | delete from cursor to the beginning of the line |
| `⌘ ,` | delete from cursor to the end of the line       |
| `⌘ .` | delete from cursor to the end of the line       |

#### Hyper Mode - Misc

It proviede some miscellaneous when using Hyper Mode.

| key     | effect                       |
|---------|------------------------------|
| `esc ⎋` | send the real `CapsLock` key |
| `~`     | inbuild screen capture       |

### SimLayer Modes

SimLayer is the action when you press a key and at almost the same time press another key to trigger different effect.

#### Comma Mode [,] as Trigger Key

Press `,` to trigger comma mode, and:

| key | to  | note           |
|-----|-----|----------------|
| `a` | `[` | open bracket   |
| `s` | `]` | close bracket  |
| `d` | `&` | ampersand      |
| `f` | `*` | asterisk       |
| `q` | `_` | underscore     |
| `w` | `+` | plus sign      |
| `e` | `%` | percentage     |
| `r` | `^` | caret          |

#### Period Mode [.] as Trigger Key

Press `.` to trigger period mode, and:

| key | to   | note             |
|-----|------|------------------|
| `a` | `~/` | home dir         |
| `s` | `.*` | all types        |
| `d` | `(`  | open parenthese  |
| `f` | `)`  | close parenthese |
| `q` | `-`  | dash/minus       |
| `w` | `=`  | equal sign       |
| `e` | `{`  | open brace       |
| `r` | `}`  | close brace      |

#### Space Mode 

Change Mac build-in keyboard to Filco Minila layout with spacebar FN.

If you got a Filco Minila keyboard, you might get used to the layout with powerful FN key. Now you can play with your mac build-in keyboard `space` key the same way. And you know how it works without doubt.

TL; DR

#### Tmux Mode [Q] as Trigger Key

Press `q` as the tmux prefix (you must set your prefix to `ctrl a` first), the supported lists as follows:

- `,`
- `[`
- `]`
- `-`
- `\`
- `f`
- `e`
- `w`
- `h`
- `j`
- `k`
- `l`
- `v`
- `s`
- `z`
- `x`
- `c`
- `1`
- `2`
- `3`
- `4`
- `5`

### Misc

- Shift pressed alone to change input source
- Change right command to command-tab when used alone for jumping between two recent apps
- Change right option to 4 modifiers combination `⇧⌃⌥⌘`, and `f17` when used alone
- Quit apps by pressing command-q twice

## Installation

1. Install [Karabiner-Elements](https://pqrs.org/osx/karabiner/)
2. Install [Goku](https://github.com/yqrashawn/GokuRakuJoudo)
3. Install k-goku

```
curl https://raw.githubusercontent.com/kchen0x/k-goku/master/karabiner.edn > ~/.config/karabiner.edn

goku
```