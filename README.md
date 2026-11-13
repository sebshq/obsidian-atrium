# Atrium™ for Obsidian

[![Six Atrium workspaces: rain on a window, neon Tokyo, a reading nook, a terminal, a hillside meadow and a kitchen](https://raw.githubusercontent.com/sebshq/obsidian-atrium/main/assets/workspaces.gif)](https://atrium-md.com)

### **[Learn more at atrium-md.com →](https://atrium-md.com)**

## Programs Atrium runs

On desktop, three cards start other programs on your computer through Node's `child_process`. To show only what works on your computer, Atrium first checks which of these programs are installed, with `/bin/sh`.

- **Terminal** runs your shell in the card, through Python 3 or `expect`.
- **Calendar events** (macOS) read and edit the Calendar app's events through `atrium-calendar`, a small helper, each time a card shows them. Without it, Atrium reads events from icalBuddy if you have it installed.
- **Dictation and spoken commands** (macOS) turn speech into text through `atrium-speech`, a small helper using Apple's speech recognition. A spoken command can ask Claude Code, in a terminal card, if you turn that on.

Both helpers are built from the Swift source in [`helper/`](helper) and attached to each GitHub release. On a Mac, Atrium downloads them from GitHub once per version into its plugin folder and marks them executable with `chmod`.
