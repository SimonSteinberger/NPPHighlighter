# NppHighlighter (fork)

A Notepad++ plugin that highlights search results, double-click "smart highlight" matches, and changed lines in a compact indicator panel next to the editor's scrollbar.

## Fork notice

This is a fork of [michaelxzhang/Npp-Highlighter](https://github.com/michaelxzhang/Npp-Highlighter), which is itself based on the [jN plugin](https://github.com/sieukrem/jn-npp-plugin) by Eugen Kremer (sieukrem). All credit for the original plugin architecture and functionality goes to the original authors.

## Improvements over the original

- **Automatic panel background color** – the indicator panel's background now samples the real, currently active scrollbar color at runtime and matches it, instead of using a fixed color. This means it automatically adapts to the user's current theme (light or dark) rather than looking out of place.
- **Narrower panel** – the indicator panel takes up noticeably less horizontal space, with markers drawn flush against the panel edges instead of with padding.
- **Various bug fixes**, including:
  - Search-hit markers from double-click "smart highlight" not appearing until the user scrolled or manually applied a style highlight.
  - "Changed line" markers staying visible after undoing all changes back to the last saved state.

## Download

Precompiled DLLs from a recent successful build are available under "Releases" of this repository

## Installation

In Notepad++: **Settings → Import → Import plugin(s)...** → select the downloaded `NppHighlighter.dll` (use the x64 build for 64-bit Notepad++, Win32 for 32-bit).

## Building from source

This repository includes a GitHub Actions workflow (`.github/workflows/build.yml`) that builds the plugin in the cloud — no local Visual Studio installation required:

1. Go to the **Actions** tab of this repository.
2. Select the "Build NppHighlighter" workflow.
3. Click **Run workflow**.
4. Once the run finishes, download the `NppHighlighter-x64` / `NppHighlighter-Win32` artifact from the run's summary page.

Alternatively, open `Highlighter.sln` in Visual Studio (2019/2022, with the "Desktop development with C++" workload and the ATL component installed) and build the `Release` configuration for `x64` or `Win32`.

## License

GNU General Public License v3 (or later), consistent with the original jN / Npp-Highlighter projects. See `GPL_and_Commercial.txt` for details.
