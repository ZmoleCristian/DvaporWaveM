# Trag Date - neo-dwm
## FAQ

> What are the bindings?

Check out [config.h](config.h).

Or read about in Luke's manual:
Press <kbd>META+F1</kbd> to view it in dwm (zathura is required for that binding).
I haven't kept `man dwm`/`dwm.1` updated though. PRs welcome on that, lol.

## Patches and features
- Adjust bar height with [bar height](https://dwm.suckless.org/patches/bar_height/) patch  
- Spawn default tag apps with [tag spawn](https://dwm.suckless.org/patches/tagspawn/) patch  
- [Clickable statusbar](https://dwm.suckless.org/patches/statuscmd/) with Luke's build of [dwmblocks](https://github.com/lukesmithxyz/dwmblocks).
- Reads [xresources](https://dwm.suckless.org/patches/xresources/) colors/variables (i.e. works with `pywal`, etc.).
- [hide vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/) hides tags with no windows.
- scratchpad: Accessible with <kbd>mod+shift+enter</kbd>.
- New layouts: bstack, fibonacci, deck, centered master and more. All bound to keys <kbd>super+(shift+)t/y/u/i</kbd>.
- True fullscreen (<kbd>super+f</kbd>) and prevents focus shifting.
- Windows can be made sticky (<kbd>super+s</kbd>).
- [hide vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/) hides tags with no windows.
- [stacker](https://dwm.suckless.org/patches/stacker/): Move windows up the stack manually (<kbd>super-K/J</kbd>).
- [shiftview](https://dwm.suckless.org/patches/nextprev/): Cycle through tags (<kbd>super+g/;</kbd>).
- [vanitygaps](https://dwm.suckless.org/patches/vanitygaps/): Gaps allowed across all layouts.
- [swallow patch](https://dwm.suckless.org/patches/swallow/): if a program run from a terminal would make it inoperable, it temporarily takes its place to save space.


## Installation for newbs

```bash
git clone https://github.com/LukeSmithxyz/dwm.git
cd dwm
sudo make install
```

There is also a `PKGBUILD` usable on distributions with pacman. Run `makepkg -si` instead of `sudo make install`.

### You must also install `libxft-bgra`!

This build of dwm does not block color emoji in the status/info bar, so you must install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/), which fixes a libxft color emoji rendering problem, otherwise dwm will crash upon trying to render one. Hopefully this fix will be in all libxft soon enough.
