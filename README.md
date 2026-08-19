# Plasma-Overdose

![Preview](https://images.pling.com/img/00/00/64/63/03/1699532/screenshot-20220205-124157.png)

Plasma-Overdose is a KDE theme inspired by the popular game *Needy Girl Overdose/Needy Streamer
Overload*.

Join our discord server! <https://discord.gg/xvWEt4NJcx>


## What we offer

Plasma-specific:

* `look-and-feel/`: Global Theme
  * [X] Splash Screen
* `desktoptheme/`: Plasma Style
  * [X] Color Scheme
* `aurorae/`: Window Decorations
* `kwin/`: Window Decorations (KWin, this is better)
* `wallpapers/`: Wallpaper

The Global Theme, Plasma Style, Color Scheme and KWin decoration each ship in two flavours: the
original light one and a **dark** one, named `*-Dark`. The splash screen, wallpaper, Aurorae
decorations, cursors and sounds are shared by both. See [Dark mode](#dark-mode).

Should available across DEs:

* `sounds/`: Sound Theme
* `cursors/`: Cursor Theme

## Todos

- Renew the code
- A Kvantum theme, for adjusting Widget Style.
- An icon theme. We started this work in separate repo: [Plasma-Overdose-Icons](https://codeberg.org/notify-ctrl/Plasma-Overdose-Icons)
- (Maybe) Lock screen theme.

## Font

Using a pixelated font like Public Pixel enhances the experience of using the theme.

> The game uses the [zpix](https://github.com/SolidZORO/zpix-pixel-font/) font. You can download it from linked repository and install it manually.

## Download

To download the theme you need to clone the repository:

```sh
git clone https://codeberg.org/Notify-ctrl/Plasma-Overdose
cd Plasma-Overdose/
```

## Install

Auto install script:

```sh
sh -c "$(curl -fsSL https://codeberg.org/notify-ctrl/Plasma-Overdose/raw/branch/master/install.sh)"
```

### Manual Install

To install the Aurorae theme run
```sh
mkdir -p ~/.local/share/aurorae/themes
cp -r aurorae/Plasma-Overdose* ~/.local/share/aurorae/themes/
```

To install the KWin window decoration run
```sh
mkdir -p ~/.local/share/kwin/decorations
cp -r kwin/Plasma-Overdose-KWinDeco ~/.local/share/kwin/decorations
cp -r kwin/Plasma-Overdose-KWinDeco-Dark ~/.local/share/kwin/decorations
```

To install the cursor theme run
```sh
mkdir -p ~/.icons/CursorsOverdose
cp -r cursors/* ~/.icons/CursorsOverdose/
```

To install the Color Scheme run
```sh
mkdir -p ~/.local/share/color-schemes
cp plasma/desktoptheme/Plasma-Overdose/colors ~/.local/share/color-schemes/Plasma-Overdose.colors
cp plasma/desktoptheme/Plasma-Overdose-Dark/colors ~/.local/share/color-schemes/PlasmaOverdoseDark.colors
```

To install the Desktop Theme run
```sh
mkdir -p ~/.local/share/plasma/desktoptheme
cp -r plasma/desktoptheme/Plasma-Overdose ~/.local/share/plasma/desktoptheme/
cp -r plasma/desktoptheme/Plasma-Overdose-Dark ~/.local/share/plasma/desktoptheme/
```

To install the Global Theme run
```sh
kpackagetool6 -t Plasma/LookAndFeel -i plasma/look-and-feel/Plasma-Overdose
kpackagetool6 -t Plasma/LookAndFeel -i plasma/look-and-feel/Plasma-Overdose-Dark
```

To install the sound theme run
```sh
mkdir -p ~/.local/share/sounds/PlasmaOverdose
cp -r sounds/* ~/.local/share/sounds/PlasmaOverdose/
```

To install the wallpaper run
```sh
mkdir -p ~/.local/share/wallpapers/Plasma-Overdose
cp -r wallpapers/Plasma-Overdose/* ~/.local/share/wallpapers/Plasma-Overdose/
```

## Dark mode

Pick **Plasma Overdose Dark** in *System Settings > Colors & Themes > Global Theme*. It applies:

* Color scheme `Plasma-Overdose-Dark` (`PlasmaOverdoseDark`)
* Plasma Style `Plasma Overdose Dark`
* KWin decoration `Plasma Overdose Dark (KWin)`
* Icon theme `breeze-dark`
* The same splash screen, wallpaper and cursors as the light theme

Because the splash screen lives in the light package, install both Global Themes if you want one
(`[ksplashrc][KSplash] Theme=Plasma-Overdose`); everything else works with the dark package alone.

The palette:

| Role            | Hex       |
| --------------- | --------- |
| Window backgnd  | `#14101F` |
| View background | `#0E0B16` |
| Surface / alt   | `#241B3A` |
| Text            | `#F0D1F1` |
| Dimmed text     | `#9B8FB5` |
| Purple accent   | `#A87CFF` |
| Magenta accent  | `#EAA0E8` |
| Cyan accent     | `#90F4E4` |
| Selection       | `#FF557F` |

For Konsole, import `konsole/Plasma-Overdose-Dark.colorscheme` (*Settings > Edit Current Profile >
Appearance*), or copy it to `~/.local/share/konsole/`.

The Aurorae decorations and the wallpaper are drawn artwork and have no dark counterpart; the dark
Global Theme uses the KWin decoration instead, and the dark Global Theme has no preview thumbnail
in System Settings for the same reason.

Every color of the KWin decoration is editable in *System Settings > Window Decorations > Configure
Plasma Overdose Dark (KWin)*. Two of them are new in both variants: the content background (was a
hardcoded near-white) and the drop shadow (was tied to the border color, which would glow rather
than shade in dark mode).

After completing all the steps, you need to manually set the theme and its components in:

> System Settings > Colors & Themes

### Feel free to contribute to this theme!
