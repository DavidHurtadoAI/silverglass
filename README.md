# Silverglass

A silver-and-blue skeuomorphic theme for [Obsidian](https://obsidian.md): polished metal, recessed blue glass, bevelled buttons, and controls that look like something you can touch. Light silver and dark gunmetal modes. Made by David Hurtado with OpenAI Codex.

## From a Winamp post to a working theme in 13 minutes

David saw a post on X by Jose Saez-Merino, quoting Rushil Shah, with an image of a classic Winamp interface: silver metal, blue glass, round transport buttons, and an equalizer. It prompted a question: could an AI build an Obsidian theme with those same design principles?

He showed the screenshot to Codex and asked whether similar themes existed and how much work it would take to build one. Codex's estimate went as far as **one to two weeks** for a polished, distributable theme. David laughed and challenged it: **less than half an hour**.

**The first working prototype was built and installed in 13 minutes.**

That was the beginning, not the end of the polishing. David then reviewed it in the real app and supplied screenshots pointing out small issues: off-center icons, inconsistent button sizes, slider alignment, repeated dropdown arrows, the right-hand title bar, and tag contrast in light mode. Those corrections became the 0.1.x releases.

Silverglass is the result of that exchange: an idea from a nostalgic screenshot, a deliberately challenged estimate, and hands-on iteration inside Obsidian. The 13 minutes describe the first prototype, not the total time spent refining or testing this release.

## Screenshots

These are the light and dark screenshots selected by David for this release.

### Light

![Silverglass in light mode, with silver panels and blue glass](screenshots/light.png)

### Dark

![Silverglass in dark mode, with gunmetal panels and blue glass](screenshots/dark.png)

### What is the player in the middle?

**The central player is an interactive HTML/CSS prototype created by Codex as a visual reference and a personal demo for David.** It is embedded in an Obsidian note; it is not a screenshot pasted into the note, a built-in Obsidian feature, or a music-player plugin.

You can move its position, volume, balance, and equalizer sliders. The display, spectrum, transport symbols and menu labels are illustrative: **it does not play audio or process sound**, and slider positions are not saved. Installing the theme does not add this panel to your notes automatically.

The surrounding Obsidian interface is the actual theme: tabs, sidebars, buttons, inputs, sliders, menus, settings, tags, tables and callouts.

## Install

Silverglass is published on GitHub. It has **not yet been accepted into the Obsidian Community Themes directory**.

1. Download `theme.css` and `manifest.json` from the [latest release](https://github.com/DavidHurtadoAI/silverglass/releases/latest).
2. Create a folder named `Silverglass` inside your vault's `.obsidian/themes/` folder.
3. Place both downloaded files directly inside that folder.
4. In Obsidian, open **Settings → Appearance** and select **Silverglass**. Reload Obsidian if the theme does not appear immediately.
5. Choose **Light** for the silver finish or **Dark** for gunmetal.

To stop using it, select the default theme in Appearance. No plugin, account, network access or payment is required by the theme.

## Try the optional prototype

- **Inside Obsidian:** copy [`examples/Silverglass - Demo.md`](examples/Silverglass%20-%20Demo.md) into your vault, activate Silverglass, and open the note in Reading view. The example is in Spanish, as it was created for David.
- **In a browser:** download or clone this repository and open [`preview.html`](preview.html) locally. Keep `theme.css` beside it. This is a standalone prototype, not a hosted website.

The example uses inline HTML and SVG. It contains no scripts or external resources. The full-size front panel is designed for a reasonably wide note pane; narrow panes may clip parts of this optional demo.

## Blue-glass callouts

Use this in any note:

```markdown
> [!lcd] SIGNAL LOCKED
> Your text inside a recessed blue-glass display.
```

## Compatibility and validation

- Version **0.1.3**, tested on **Obsidian 1.14.2 for Windows**.
- `minAppVersion` is conservatively set to `1.14.2`; older versions have not been verified.
- Both light and dark modes were checked in the app. Mobile devices and other operating systems have not been tested.
- The theme passes the official `stylelint-config-obsidianmd` configuration with zero errors and warnings. This does not imply approval by the Community directory or exhaustive compatibility with every plugin.
- Original CSS, standard Obsidian variables, local embedded SVG chevrons, no remote fonts or images, no telemetry, and no `!important` declarations.

Please report issues with your Obsidian version, operating system, light/dark mode, and a screenshot.

## Development

```sh
npm ci --ignore-scripts
npm run lint
```

Edit `theme.css`. To test, copy it and `manifest.json` into the theme folder of a development vault. The repository contains no automatic installer and does not modify a vault when you run the linter.

## License and credits

[MIT](LICENSE) © 2026 David Hurtado for the theme code and original demo. The two screenshots were supplied by David for this project.

Visual inspiration: the classic Winamp interface in the post David shared. No Winamp skin bitmap, logo, proprietary font or source code is bundled. Silverglass is not affiliated with Winamp or Obsidian. The demo track label is a nod to the reference image.
