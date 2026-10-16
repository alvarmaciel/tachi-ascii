# Tachi ASCII

A Tachikoma-inspired animated ASCII emote set for [pi-emote](https://github.com/cgxeiji/pi-emote).

```text
  ╭◉╮─
╭─╯ ╰─╮
╰┬───┬╯
╱╲   ╱╲
```

The emote reacts to Pi states such as thinking, talking, reading, writing, tool use, success, failure, and context compaction. The body is cyan, and the eye is yellow.

## Requirements

- [Pi](https://github.com/earendil-works/pi)
- [pi-emote](https://github.com/cgxeiji/pi-emote)
- A terminal font that displays Unicode box-drawing characters as single-width characters

## Install manually

Create the custom emote directory:

```bash
mkdir -p ~/.pi/agent/extensions/pi-emote/emotes/tachikoma
```

Copy `ascii.yaml` into it:

```bash
cp ascii.yaml ~/.pi/agent/extensions/pi-emote/emotes/tachikoma/ascii.yaml
```

Create or update `~/.pi/agent/extensions/pi-emote/config.json`:

```json
{
  "terminals": [
    { "match": "unknown", "render": "ascii" }
  ],
  "emotes": [
    { "model": "*", "emote-set": "tachikoma" }
  ]
}
```

If that file already contains settings, merge these entries instead of replacing the file.

Restart Pi after changing the configuration.

## Terminal behavior

This repository contains an ASCII-only emote set. Selecting it makes `pi-emote` use ASCII rendering in every terminal.

The `unknown` terminal mapping is useful for embedded terminals such as Orca that `pi-emote` does not currently identify by name. Remove that mapping if your terminal is detected correctly or if you already have a terminal-specific configuration.

## Canvas

Every frame fits within the 8-column by 4-row canvas used by `pi-emote` ASCII emotes.

## Disclaimer

This is unofficial fan art inspired by Tachikoma from *Ghost in the Shell*. It is not affiliated with or endorsed by the rights holders.
