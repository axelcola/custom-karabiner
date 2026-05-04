# My Karabiner Keyboard

Custom keyboard modifications for macOS using [Karabiner-Elements](https://karabiner-elements.pqrs.org/).

## Overview

**My Karabiner Keyboard** is a personal keyboard configuration focused on faster navigation, editing, and system controls without leaving the main keyboard area.

The setup is built around **Caps Lock as a dual-purpose key**:

- Tap `Caps Lock` to send `Enter`
- Hold `Caps Lock` to activate a custom `Hyperkey` layer
- Press `Caps Lock + Shift` to use normal `Caps Lock`

In this configuration, the Hyperkey layer is implemented internally with Karabiner's `fn` modifier.

## Goals

The main goals of this setup are:

- Keep cursor movement close to the home row
- Reduce the need to reach for the arrow keys
- Make text navigation faster and more comfortable
- Add useful shortcuts for coding and writing
- Control common macOS settings from the keyboard
- Improve productivity in Visual Studio Code

## Requirements

- macOS
- [Karabiner-Elements](https://karabiner-elements.pqrs.org/)

## Files

This repository includes Karabiner complex modification JSON files:

| File | Description |
| --- | --- |
| `master.json` | Main configuration with all custom rules |
| `test.json` | Test configuration with most of the same rules |

## Features

### Caps Lock as Enter and Hyperkey

Caps Lock behaves differently depending on how it is used:

| Shortcut | Action |
| --- | --- |
| `Tap Caps Lock` | `Enter` |
| `Hold Caps Lock` | Activate `Hyperkey` |
| `Caps Lock + Shift` | `Caps Lock` |

This makes Caps Lock useful as both a regular key and a powerful shortcut layer.

## Navigation Shortcuts

### J/K/L/I as Arrow Keys with Hyperkey

When holding the Hyperkey, the `J`, `K`, `L`, and `I` keys work as arrow keys:

| Shortcut | Action |
| --- | --- |
| `Hyperkey + J` | Left Arrow |
| `Hyperkey + K` | Down Arrow |
| `Hyperkey + L` | Right Arrow |
| `Hyperkey + I` | Up Arrow |
| `Hyperkey + Spacebar` | Right Arrow |

This allows arrow-key navigation without moving your right hand away from the home row.

### J/K/L/I with Option and Command

The same navigation cluster also works with common macOS modifiers, without needing to press the Hyperkey.

| Shortcut | Action |
| --- | --- |
| `Option + J` | `Option + Left Arrow` |
| `Option + L` | `Option + Right Arrow` |
| `Option + K` | `Option + Down Arrow` |
| `Option + I` | `Option + Up Arrow` |
| `Command + J` | `Command + Left Arrow` |
| `Command + L` | `Command + Right Arrow` |
| `Command + K` | `Command + Down Arrow` |
| `Command + I` | `Command + Up Arrow` |

This is useful for text editing actions such as:

- Moving by word
- Jumping to the beginning or end of a line
- Moving across larger blocks of text
- Navigating code faster

## Fast Vertical Movement

### Double Tap Hyperkey + I/K

When holding the Hyperkey, double-tapping `I` or `K` repeats vertical cursor movement.

| Shortcut | Action |
| --- | --- |
| `Double tap Hyperkey + I` | Move up multiple times |
| `Double tap Hyperkey + K` | Move down multiple times |

This is useful for quickly moving through code, lists, or long documents without reaching for the arrow keys.

> Note: The current JSON sends multiple arrow key events. The exact number depends on the rule definition in the configuration file.

## Editing Shortcuts

### Delete Current Line

| Shortcut | Action |
| --- | --- |
| `Hyperkey + X` | Delete current line |

This shortcut moves to the end of the current line and deletes it, making it useful while coding or editing text.

### Forward Delete

| Shortcut | Action |
| --- | --- |
| `Hyperkey + Option + Command + P` | Forward Delete |

This provides quick access to `delete_forward` without reaching for a dedicated forward-delete key.

## Visual Studio Code Shortcuts

### Back and Forward Navigation

These shortcuts are designed for Visual Studio Code navigation history:

| Shortcut | Action |
| --- | --- |
| `Hyperkey + U` | Go Back |
| `Hyperkey + O` | Go Forward |

They map to the default VS Code-style navigation shortcuts:

| Shortcut | Output |
| --- | --- |
| `Hyperkey + U` | `Control + -` |
| `Hyperkey + O` | `Control + Shift + -` |

This makes it easier to jump between previous and next cursor locations while coding.

## System Controls

### Volume Control

| Shortcut | Action |
| --- | --- |
| `Hyperkey + R` | Volume Up |
| `Hyperkey + F` | Volume Down |

### Screen Brightness

| Shortcut | Action |
| --- | --- |
| `Hyperkey + E` | Increase screen brightness |
| `Hyperkey + D` | Decrease screen brightness |

### Keyboard Illumination

| Shortcut | Action |
| --- | --- |
| `Hyperkey + W` | Increase keyboard illumination |
| `Hyperkey + S` | Decrease keyboard illumination |

These shortcuts make common system controls accessible from the main keyboard area.

## Display / Accessibility Shortcut

### Toggle Red Filter

| Shortcut | Action |
| --- | --- |
| `Hyperkey + A` | Sends `Command + 8` |

This can be used as a toggle shortcut for a red filter or display-related accessibility workflow, depending on your macOS shortcut configuration.

> Note: This rule is present in `master.json`.

## Installation

1. Install [Karabiner-Elements](https://karabiner-elements.pqrs.org/).
2. Clone or download this repository.
3. Copy the JSON configuration file into your Karabiner complex modifications folder.
4. Open Karabiner-Elements.
5. Go to **Complex Modifications**.
6. Add and enable the custom rules you want to use.

## Suggested Folder

Karabiner stores its configuration under:

sh ~/.config/karabiner/

For complex modifications, you will usually place custom rule files inside:

~/.config/karabiner/assets/complex_modifications/

After copying the file, open Karabiner-Elements and enable the rules from the Complex Modifications section.

Motivation

This configuration was created to make keyboard navigation more comfortable and efficient.

Instead of constantly moving the right hand to the arrow keys or system control keys, this setup keeps navigation, editing, and common actions close to the home row.

It is especially useful for:

Developers
Writers
Keyboard-focused workflows
Visual Studio Code users
Anyone interested in ergonomic keyboard customization
Status

This is a personal and evolving keyboard setup. Shortcuts may change over time as the workflow improves.

Notes

This repository is mainly built for my own workflow, but it may be useful for anyone interested in:

Karabiner-Elements configurations
Home-row arrow keys
Caps Lock remapping
Hyperkey-based shortcuts
Ergonomic text navigation
macOS keyboard customization
