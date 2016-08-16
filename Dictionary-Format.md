This page is under construction. Please refer to [Learn Plover! Appendix: The Dictionary Format](https://sites.google.com/site/ploverdoc/appendix-the-dictionary-format) for a more complete document. Note that as of Plover 3.1, the Plover Control Commands have been updated and this document is more accurate as to their function.

## JSON and RTF/CRE

Plover supports two types of dictionaries, **JSON** (the default and recommended format) and **RTF**. RTF/CRE is an import/export format used by proprietary steno software, which means that Plover can work with exported dictionaries from Eclipse, ProCAT, Case CATalyst, and more. There are some caveats with each format, however. Mainly, RTF dictionaries will cause Plover to take longer to start up and won't have Unicode support, while JSON is a Plover-specific format and moving to other steno software will require a conversion to RTF. The Plover JSON format also doesn't have support for stroke metadata, but at the moment Plover doesn't support reading/writing RTF metadata.

## Sending Symbols

Since Plover 3.0.0, users can write full Unicode by simply using symbols in their JSON dictionary or by pasting them into the "Add Translation" dialog or into the dictionary manager. You can get symbols from a character insert panel in your operating system if you have one, or you can copy and paste symbols from another application like a web browser.

```json
{
  "SHR*UG": "¯\\_(ツ)_/¯",
  "TR*PL": "{^}™",
  "TPHA*ES": "n̶o̶ yes"
}
```

## Text Formatting

### Prefixes, Infixes, and Suffixes

Strokes can be attached at the beginning and/or end using the "attach" operator. You can also benefit from some built-in orthographic rules that Plover uses to have intelligent strokes.

- `{^}` is the attach operator.
- `{^ish}` is an orthographic-aware suffix that will add "ish" to the end of the previous word. E.g. `RED/EURB` will output `reddish`. Note the addition of a second "d" caused by Plover's understanding of English orthography.
- `{^}ish` is a suffix with the text outside the operator—this means that the text will simply be attached without grammar rules. Using this stroke in the previous example would give instead `redish`.
- `{^-to-^}` is an infix, e.g. `day-to-day`.
- `{in^}` is a prefix, e.g. `influx`.
- Most custom punctuation entries will take advantage of the attach operator, e.g. `{^—^}` for an emdash.

### Carrying Capitalization

- `{~|}` or `{^~|^}` where the attach operator is optional.

In English, we have punctuation that is doesn't get capitalized, but instead the next letter gets the capitalization. For example, if you end a sentence in quotes, the next sentence still starts with a capital letter! `"You can't eat that!" The baby ate on.` In order to support this, there is a special pre/in/suffix syntax that will "pass on" or "carry" the capitalized state. You might find this useful with quotes, parentheses, and words like `'til` or `'cause`. The default dictionary for Plover should use these operators where appropriate.

```json
{
  "KW-GS": "{~|\"^}",
  "KR-GS": "{^~|\"}",
  "KA*US": "{~|'^}cause",
  "PREPB": "{~|(^}",
  "PR*EPB": "{^~|)}"
}
```

## Commands and Keyboard Shortcuts

Most Plover strokes are just text and formatting operators. Plover handles standard strokes really well, which allows it to handle "undoing" with the asterisk key, as well as automatically handling case and spacing. However, Plover's text and formatting strokes can't send arbitrary key strokes, like sending keyboard shortcuts.

**Note:** Plover 3.1 introduces new rules for commands that differ slightly from the previous implementation. Before Plover 3.1, commands were used to send symbols because Plover didn't have full Unicode support. *It used to be possible to send "+" by writing `{#plus}`, but the system has been updated.*

- `{#}` is the command operator.

Inside of a command block, you write in what keys you want Plover to simulate. Note that the keys hit in command blocks won't be "undone" when using the asterisk (because you can't backspace a keyboard shortcut). You select the keys by their name. Note that all key names will only refer to the base key. For example, to use letter keys, you just use the corresponding letter (case insensitive) separated by spaces:

- `{#a b c d}` will send "abcd" and will not affect Plover's text formatting or asterisk undo-buffer.

You can also use key names, which is needed when you are accessing a symbol key. For example, on the QWERTY layout there is an equals/plus key in the top right, which you can access by either of its names:

- `{#equals plus}` will send "==" because Plover doesn't send modifiers, but rather just hits the key based on the name. If you want to send symbols, though, don't use commands. Just use the symbol in the translation. Commands should be used for keyboard shortcuts only.

If you want to use a modifier, just use it by name. For convenience, all key names are case insensitive and you can optionally default to the left modifier by dropping the side selector:

--------------------
| Modifier | Command Key Names | 
|----------|----------| 
| Shift | `Shift_L`, `Shift_R`, `shift` | 
| Control |  `Control_L`, `Control_R`, `control` | 
| Alt | `Alt_L`, `Alt_R`, `alt`, `option` | 
| Super | `Super_L`, `Super_R`, `super`, `windows`, `command` | 
--------------------

To use modifiers, simply use parentheses to delimit where keys are pressed down. Here are some shortcuts in a JSON format:

- `"STPH-G": "{#right}"` — right arrow on the keyboard, for moving the cursor to the right once
- `"SKWR-G": "{#shift(right)}"` — shift and right arrow on the keyboard, for selecting one character
- `"SKWR-BG": "{#control(shift(right))}"` — shift, control, and right arrow on the keyboard, for selecting one word to the right on Windows/Linux
- `"SKWR-BG": "{#option(shift(right))}"` — option (alt), control, and right arrow on the keyboard, for selecting one word to the right on Mac

These next strokes are not particularly useful, but show you what you can do with the command syntax.

- `"TKAO*UP": "{#control(c v v v)}" — copy, then paste 3 times
- `"SKPH-Z": "{#control(z shift(z))" — program-dependent, but possibly "undo/redo". Notice how the first z has only the control operator, and the second has both the control and the shift operator.

Note that above, adding capitals will not affect the output. Commands are case insensitive. `{#control(z shift(z))` is the same as `"{#CONTROL_L(Z SHIFT(Z))}"`

## Output Modes

- `{MODE:}` is the mode operator

Plover supports special character casing, such as CAPS LOCK and Title Case. It also supports replacing its implicit space with other characters, which is useful in case a user wants to write_in_snake_case.

**Output modes** are activated with a special syntax in your dictionary, and can be a stroke or just part of a stroke. They can then be turned off with a special reset command. A sample flow for caps lock might be → turn on caps lock, write in capital letters, turn off caps lock. However, there's nothing stopping you from building in output modes into your strokes. For example, you might want your new paragraph stroke to reset the case mode no matter what.

### Reset Command

You can reset the output mode to its default with `{MODE:RESET}`. It is **highly recommended** that you have a reset output mode command so that you can always reset Plover's output mode in case you change it by accident.

- `{MODE:RESET}`: reset the case and space character → recommended to get out of any custom output mode.
- `{MODE:RESET_CASE}`: exit caps, lower, or title case.
- `{MODE:RESET_SPACE}`: use spaces as normal

### Modes

There are some built-in modes you can use:

--------------------
| Dictionary Syntax | Sample Output | 
|-----------|---------|
| `{MODE:CAPS}` | THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG. |
| `{MODE:TITLE}` | The Quick Brown Fox Jumps Over The Lazy Dog. | 
| `{MODE:LOWER}` | the quick brown fox jumps over the lazy dog. |
| `{MODE:CAMEL}` | theQuickBrownFoxJumpsOverTheLazyDog. |
| `{MODE:SNAKE}` | The_quick_brown_fox_jumps_over_the_lazy_dog. |
--------------------

### Custom Modes

You can define your own custom modes with the `SET_SPACE:` operator, which allows you to replace the space that Plover outputs with anything. Plover's snake-mode is the same as `SET_SPACE:_`. Here are some other examples:

--------------------
| Dictionary Syntax | Sample Output | 
|---------|-----------|
| `{MODE:SET_SPACE:}` | Thequickbrownfoxjumpsoverthelazydog. |
| `{MODE:SET_SPACE:-}` | The-quick-brown-fox-jumps-over-the-lazy-dog. | 
| `{MODE:SET_SPACE:😁}` | The😁quick😁brown😁fox😁jumps😁over😁the😁lazy😁dog. | 
--------------------