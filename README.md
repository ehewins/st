# My build of st

My own build of [st](https://st.suckless.org/), with the patches I use and a few features brought over from [Luke Smith's build](https://github.com/LukeSmithxyz/st).

## Requirements

Obviously you'll need the correct [nerd font](https://github.com/ryanoasis/nerd-fonts) (mononoki in my case), I've been using the v2.0 release since later versions have caused me problems with polybar before. For my backup font I'm using Noto Color Emoji, so grab that too. If you want to use different fonts, just change them in `config.h`. For emojis and some other unicode characters to work in st, you'll need [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra) from the AUR.
You'll also need `libX11`, `libXft` as well as `make`, but any normal linux user will already have these installed.

## Installation

Just clone and make:

```
git clone https://github.com/ehewins/st
cd st
sudo make clean install
```

## Features

+ Can be configured via Xresources, useful for changing your colour scheme without having to recompile.
+ Scroll using `ctrl-shift-j/k`/`ctrl-shift-↑/↓` or `ctrl-shift-u/d` for faster scrolling.
+ Zoom using `alt-shift-j/k`.
+ Actually displays an icon in tint2, thanks to the `netwmicon` patch
+ Open a new terminal in the current working directory with `ctrl-shift-enter`
+ Luke Smith's externalpipe scripts:
    - Follow urls using `alt-shift-l`
    - Copy urls to clipboard using `alt-shift-y`
    - Copy the output of commands to clipboard using `alt-shift-o`
+ Copying and pasting highlighted text is done with `ctrl-shift-c/v`

## Installed Patches

+ `anysize`
+ `bold-is-not-bright`
+ `boxdraw_v2`
+ `externalpipe` and `externalpipe-eternal`
+ `font2`
+ `glyph-wide-support`
+ `netwmicon`
+ `newterm`
+ `scrollback`
+ `xresources` + some fixes (see patches folder)
