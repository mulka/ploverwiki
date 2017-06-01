This glossary will help you with terms that you may come across in the steno community.

**Table of Contents**

- [Brief](#brief)
- [Chord](#chord)
- [Conflict](#conflict)
- [Dragging](#dragging)
- [JSON](#json)
- [RTF/CRE](#rtfcre)
- [Misstroke](#misstroke)
- [Stacking](#stacking)
- [Steno Dictionary](#steno-dictionary)
- [Steno Order](#steno-order)
- [Stroke](#stroke)
- [Steno Theory](#steno-theory)
- [Untranslate](#untranslate)
- [Word Boundary](#word-boundary)
- [Write Out](#write-out)
- [Writing](#writing)

### Brief
    
Also known as the "abbreviation", "short form", or "arbitrary".  Briefs
are simply non-phonetic mappings of steno outlines to English words or
phrases. Common words and phrases are often briefed for the purpose of speed.
For instance, the phrase "from time to time" would regularly be written
out:

`FROM/TAOIM/TO/TAOIM` (reads: "from/time/to/time" and takes four strokes)

Or, as a simple brief:

`FRIMT` (reads: "frimt" and takes only one stroke)

### Chord

The pressing down of multiple keys at the same time. Contrast with a QWERTY-style typing system which hits only one key at a time.

### Conflict

1. traditionally: a conflict-based theory uses one stroke for multiple translations. For example, a non-realtime stenographer could use the same stroke for "bare", "bear", and "bar", which is a conflict that the stenographer would have to manually resolve at a later time. Plover is a realtime-only system and does not support conflict-theories.

2. informal; a.k.a collision: when two dictionaries have the same stroke, the dictionary with the highest priority is favored. For this reason, it is important to understand your dictionary order.

### Dragging

Dragging is the term used to describe accidentally dragging another key into your stroke. E.g. if you try to write `-F` but then drag your finger to the left, you might hit `*F` instead.

### JSON

JSON, in the context of stenography, is a dictionary format which maps steno
strokes to translations. You will often see strokes expressed in the JSON format,
such as `"SKP": "and"`.

### Misstroke

A misstroke is like a "chord typo". It's when you mean to write one chord, but stroke another. Often, dictionaries have misstroke entries that are added when a stenographer frequently misstrokes an entry. For example, take the stroke `TKPWAOD` (meaning `GAOD`) which translates to `good`. Sometimes the stenographer may miss a key, so they could have a misstroke entry `TKPAOD` which would also translate to `good`. Then they are protected from these typos in regular writing. There are many misstroke entries in the default dictionary, and you must try to make sense of results when you look up words, instead of blindly accepting the shortest stroke.

### RTF/CRE

Plover can read steno dictionaries in JSON and RTF/CRE format. RTF/CRE stands for
`rich text format with court reporting extensions`. It is a standard format that most
proprietary steno software can import from and export to. Plover can read RTF/CRE
natively.

### Stacking

When writing stenography, if you accidentally merge two strokes into one, it is called stacking. For example, you might try to write `is okay` with `S-/OBG` but end up with `SOBG → sock` because you stacked the strokes. To avoid stacking, the stenographer must be sure to release all keys in their chord before stroking the next. Sometimes machines are prone to stacking due to bad debouncing or sticking keys.

You might notice strokes in Plover's default dictionary that map to, for example, `"T-S": "{^s it}"`. These were entered to fix stacking issues on Mirabai's old steno machine, but aren't relevant for most users and can safely be overwritten.

### Steno Dictionary

Used by Plover or other stenotype software. Contains all the words and
the strokes that produce those words. While generally these are
constructed using a [[steno theory|Glossary#steno-theory]], this can be freely modified by the
stenographer. Dictionaries are a collection of entries, which map strokes to translation.

### Steno Order

The 22 keys on the steno machine has an explicit "order" that gets read out,
top-to-bottom, left to right. The entire steno layout is defined by `STKPWHRAO*EUFRPBLGTSDZ`.

### Stroke

Can refer to a [[chord|Glossary#chord]], or a set of chords that you have for a
given translation. E.g., "my stroke for `steno-dude` is `STOEUPB/TKAOUD`"

### Steno Theory

A "system" or way of thinking that determines which steno strokes will
match to which words. Theories range generally from being based on
spelling ("brief-heavy") to being based on the sound of the word ("stroke-heavy").
The dictionary included with Plover uses a theory based on is based on NYCI theory
which is descended from StenEd. It offers a hybrid between a brief-heavy and
stroke-heavy theory. It is recommended to start learning with Plover theory, and
you will likely learn what style you like and you can always switch later. Mirabai
uses the Plover dictionary professionally.

### Untranslate

When writing in stenography, your strokes map to translations. E.g. `KAT → cat`. However, if a stroke is not in your dictionary, the raw form will be outputted instead. This is called an untranslate. For example, if your dictionary doesn't have `KAT`, Plover will simply output `KAT`.

### Word Boundary

The implicit spacing in between words. Spacing is inserted automatically
by Plover or other steno software. As words and phrases will often sound
similar to others, a stenographer needs to choose the stroke or brief
appropriate for the situation with the correct word boundary.

An illustration of a word boundary **error** is given by the phrase "cat log". If
a stenographer were to write "cat log" with Plover, by default, the system will
write "catalog". This happens because "cat log" isn't a very common word-pair
in English. The stenographer must explicitly write "cat (space) log".
But, there are many more common cases that are handled and the
stenographer must be explicit. See below for how some phonetics are differentiated:

Examples (Plover):

* "in here"; **`TPH`**/`HAOER` vs "insect"; **`EUPB`**/`SEBGT`
* "on top of"; **`OPB`**/`TOP`/`-F` vs "onto"; **`AUPN`**/`TO`
* "it is a live (wire)"; `T`/`S`/**`AEU`**/`HREUF` vs "it is alive"; `T`/`S`/**`A`**/`HREUF`

### Write Out

The opposite of a [brief](#brief) is writing out the word according to your theory. In Plover, this would refer to the fact that you are sounding a word out, rather than using its brief. E.g. writing out `O/PEUPB/KWROPB` instead of using the brief `P-PB` for the word "opinion".

### Writing

Professional stenographers do not like being referred to as "typists" because it normalizes the complex system that stenography is. On a steno machine, you do not "type". Instead, they call it "writing". Some stenographers are more sensitive to this than others. Generally, you "type" on a keyboard, and "write" on a steno machine. Steno machines were traditionally called "stenotypes", but that usage has died out over time.
