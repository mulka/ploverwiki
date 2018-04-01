**Configure ➪ Machine ➪ Keymap**

You can remap how Plover handles keys on your machine.

The available options are affected by your system and the machine you are using.

### What is a keymap?

A key map is....

### Remapping Keys to Different Actions

The `Key` column enumerates every key that Plover can control on your machine. This is a list of all keys on the keyboard. For American steno machines, the key names will be the Ireland layout defaults (S, T, K, etc.)

The `Action` column is what you'd like Plover to see when the key is pressed. The available actions will change depending on which system (e.g. English Stenotype) you have enabled.

### Disabling Keyboard Keys

Remapping keys is especially useful when using your keyboard as a steno machine, as you may want to set keys to `no-op` (short for "no operation") which will disable that key while Plover is running.

[[https://raw.github.com/wiki/openstenoproject/plover/images/keyboard_keymap.png|alt=Keymap configuration for the keyboard machine with some actions mapped to keys on the top row of the keyboard]]

*The escape key will be disabled while Plover's output is enabled with the configuration above, where the  "Escape" key has been mapped to the "no-op" Action.*