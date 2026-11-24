This is my Corne V3 zmk config.

## Keymap

Source: [`config/corne.keymap`](config/corne.keymap). Three layers: Default, Lower and Raise.

- **Super\*** is one-shot (sticky): tap it and it applies to the next key only, e.g. tap Super, then F → `Super+F`. Hold it for a normal Super. It stays active for 1.5 s, so other modifiers and layer keys can join in: tap Super, hold Shift, hold Lower, tap 1 → `Super+Shift+1`.
- **Lower** and **Raise** are momentary: the layer is active only while the key is held.
- **▼** marks the key you're holding to reach that layer.

### Default

```
╭───────┬───────┬───────┬───────┬───────┬───────╮   ╭───────┬───────┬───────┬───────┬───────┬───────╮
│  Esc  │   Q   │   W   │   E   │   R   │   T   │   │   Y   │   U   │   I   │   O   │   P   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Tab  │   A   │   S   │   D   │   F   │   G   │   │   H   │   J   │   K   │   L   │   ;   │   '   │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │   Z   │   X   │   C   │   V   │   B   │   │   N   │   M   │   ,   │   .   │   /   │  RAlt │
╰───────┴───────┴───────┬───────┼───────┼───────┤   ├───────┼───────┼───────┬───────┴───────┴───────╯
                        │ Super*│ Space │ Lower │   │ Raise │ Enter │ Shift │
                        ╰───────┴───────┴───────╯   ╰───────┴───────┴───────╯
```

### Lower (hold Lower)

```
╭───────┬───────┬───────┬───────┬───────┬───────╮   ╭───────┬───────┬───────┬───────┬───────┬───────╮
│  Esc  │   !   │   @   │   #   │   $   │   %   │   │   ^   │   &   │   *   │   (   │   )   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Tab  │   1   │   2   │   3   │   4   │   5   │   │   6   │   7   │   8   │   9   │   ;   │   '   │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │   -   │   =   │   \   │   [   │   ]   │   │   `   │   0   │   ,   │   .   │   /   │  RAlt │
╰───────┴───────┴───────┬───────┼───────┼───────┤   ├───────┼───────┼───────┬───────┴───────┴───────╯
                        │ Super*│ Space │   ▼   │   │       │ Enter │ Shift │
                        ╰───────┴───────┴───────╯   ╰───────┴───────┴───────╯
```

### Raise (hold Raise)

```
╭───────┬───────┬───────┬───────┬───────┬───────╮   ╭───────┬───────┬───────┬───────┬───────┬───────╮
│  Esc  │ BT Clr│  Play │  Mute │  End  │  Vol+ │   │  PgUp │   {   │   }   │   [   │   ]   │  Bksp │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Tab  │   +   │   -   │   ~   │   _   │  Del  │   │   ←   │   ↓   │   ↑   │   →   │   ;   │   '   │
├───────┼───────┼───────┼───────┼───────┼───────┤   ├───────┼───────┼───────┼───────┼───────┼───────┤
│  Ctrl │ BT Nxt│  C-b  │   |   │ C-S-v │  Vol- │   │  PgDn │  Home │   ,   │   .   │   /   │  RAlt │
╰───────┴───────┴───────┬───────┼───────┼───────┤   ├───────┼───────┼───────┬───────┴───────┴───────╯
                        │ Super*│ Space │       │   │   ▼   │ Enter │ Shift │
                        ╰───────┴───────┴───────╯   ╰───────┴───────┴───────╯
```

| Key | Action |
| --- | --- |
| BT Clr | Clear the current Bluetooth profile's pairing |
| BT Nxt | Switch to the next Bluetooth profile |
| Play | Media play/pause |
| Mute / Vol+ / Vol- | Media mute, volume up, volume down |
| C-b | `Ctrl+B` (tmux prefix) |
| C-S-v | `Ctrl+Shift+V` (paste in a terminal) |
