# Zoxide + FZF shortcut for fish

Invoke [Zoxide] at any time, with the current input preloaded

## Usage

At any time you can type Ctrl+Z in your [fish] shell, and get a [fzf] popup of your [zoxide] completions. If you have something written in the shell, the last token will be preloaded into zoxide.

Navigate the selections, choose one, and it will be pasted back into your command line, in place of the token.

## Installation

You _must_ have the following installed

| CLI        | Minimum Version Required | Description                                  |
| ---------- | ------------------------ | -------------------------------------------- |
| [fish]   | 3.4.0                    | a modern shell                               |
| [fzf]    | 0.33.0                   | fuzzy finder that powers half of this plugin |
| [zoxide] | 0.2.0                    | cd command that remembers where you've been  |

Once you've got those, installation is very easy via [Fisher]:

```fish
fisher install Paradox460/fzf_zoxide.fish
```

## Configuration

There's not much to configure, but if you want to change the keybinding, simply add a call to `fzf_zoxide_configure_binding` to your `config.fish`, passing in the new keybinding you want:

```fish config.fish
# Use alt-z for zoxide trigger
fzf_zoxide_configure_binding \ez
```

## Inspiration

This tool is inspired by two other excellent tools.

The first is obviously [zoxide], without which this would not be a thing. I like it enough to want to use it _inside_ commands, not just for moving directories, hence this library

The second is the awesome [fzf.fish] plugin, by PatricF1. These provide all sorts of alternatives to the default bindings [fzf] ships with, and I highly recommend them

[fish]: https://fishshell.com
[fisher]: https://github.com/jorgebucaran/fisher
[fzf.fish]: https://github.com/PatrickF1/fzf.fish
[fzf]: https://github.com/junegunn/fzf
[zoxide]: https://github.com/ajeetdsouza/zoxide
