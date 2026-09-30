# Odotsy

**[ChatGPT Dots](https://chatgpt.com/dots/home) in the [Omarchy](https://omarchy.org) bar.** Click your dot and the chat drops down from the top of the screen. Click again and it tucks away, still loaded. The `pop out` tab under the dropdown's corner turns it into a normal window.

Same design as [Omusey](https://github.com/telep-io/omusey): the dropdown is the real web app (`omarchy-launch-webapp`) floating in a Hyprland special workspace named `dots`, placed by a runtime window rule. No config edits, no state files.

## Install

```sh
omarchy plugin add https://github.com/telep-io/odotsy.git --enable
omarchy restart shell
```

The first click opens ChatGPT Dots as an Omarchy web app in your default (Chromium-based) browser, so if you are signed in to chatgpt.com there, you land straight in Dots. If not, sign in once in that window.

Remove with `omarchy plugin remove telep.dots`.

## Settings

```sh
omarchy bar set telep.dots url https://chatgpt.com/dots/<your-dot-id>
omarchy bar set telep.dots avatar ~/Pictures/my-dot.png
omarchy bar set telep.dots width 560          # 360-1200, default 480
omarchy bar set telep.dots heightPercent 70   # 30-90, default 60
```

The window is matched by its web app class (`chatgpt.com__dots`), so a regular ChatGPT web app is left alone.

Unofficial; not affiliated with OpenAI. [MIT](LICENSE)
