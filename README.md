# 👾 Omarchy theme extras

Optional add-ons for my [Omarchy](https://omarchy.org) themes: Braille art
greeting you in every new terminal, art for the About screen, a matching
[cliamp](https://github.com/omacom-io/cliamp) theme, and the theme hook that
switches them on and off with the theme.

An Omarchy theme is a palette and the files that dress Omarchy in it, with
nothing that runs. These extras need a script to put them in place, so they
live here, apart from the themes.

| Theme | Extras |
| --- | --- |
| [🏔️ Ozark](https://github.com/itsMattGuenther/omarchy-ozark-theme) | [Night Flight luna moth greeting, Blue Hour About art, cliamp theme](ozark/) |
| [🤖 Omarchy Raiders](https://github.com/itsMattGuenther/omarchy-omarchy-raiders-theme) | [Still listening greeting, The listening station About art, cliamp theme](omarchy-raiders/) |
| [🔴 OmarchyThings](https://github.com/itsMattGuenther/omarchy-omarchy-things-theme) | [Eleven greeting, Demogorgon About art, cliamp theme](omarchy-things/) |

## 📦 Install

Install the theme first, then clone this repo once and run the installer for
that theme:

```bash
git clone https://github.com/itsMattGuenther/omarchy-theme-extras.git ~/.local/share/omarchy-theme-extras
~/.local/share/omarchy-theme-extras/ozark/install.sh
```

Swap `ozark` for `omarchy-raiders` or `omarchy-things`. Each installer:

- copies its files into `~/.config/<theme>/` and `~/.config/cliamp/themes/`
- adds one marked block at the end of `~/.bashrc` (a backup is kept as
  `.bashrc.bak.<theme>`)
- installs a theme hook, `<theme>-theme-set.sh`, that switches cliamp and the
  About logo whenever that theme is active, and puts both back when you pick
  another theme

Each hook is named after its theme rather than `theme-set.sh`, so the hooks
sit alongside each other and alongside other themes' hooks. The greeting and
the About art only show while their theme is the active one.

Run an installer again to update after a `git pull`. To remove one theme's
extras:

```bash
~/.local/share/omarchy-theme-extras/ozark/install.sh --uninstall
```

Keep the clone around if you might uninstall later; the uninstaller uses the
hook in it to put your About logo back.

## ⚖️ License

MIT, see `LICENSE`. Credits for each piece of art are in its theme's README.
