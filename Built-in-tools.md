Plover has some useful tools that can show information while you're using it, or to make changes to its configuration or to the dictionaries. Here's a list of some of them. A list of tools you can turn on is shown in the toolbar at the top of Plover's main window.

<!-- TODO: make formatting of button and checkbox names consistent. Right now, the long ones use quotes and the short ones use italics, but that may look a bit odd. -->

## Configure Plover

The configuration window is used to change settings like which keys on the keyboard are mapped to which virtual keys in the steno system. It also lets you change whether the first word written after starting Plover is capitalized and whether it has a space before it, among other things.

## Paper tape

Useful to see which keys Plover thinks you're pressing. It keeps a list of strokes shown so you can see what you've written. It doesn't show strokes made before you enabled it though. This feature can be set to be enabled every time Plover starts by opening the configuration window and checking the "show paper tape" checkbox in the interface tab.

## Stroke suggestions

When you write words, this tool can look up the words you write and show how they can be written. Like the paper tape, it doesn't show words written before you write them, and it scrolls automatically every time a word is added. It can be enabled to be on when Plover starts by checking the "show suggestions" checkbox in the interface tab of the configuration window.

## Lookup tool

A window with two text fields, one that you can write words in, and one that will show strokes that translate to those words. It looks in the set of active dictionaries, and doesn't show which dictionaries each entry is found in. For a more general tool that can also look up strokes and translations, see [[Built-in tools#Dictionary editor#dictionary editor]].

## Plugins manager

The plugins manager lets you install plugins. In the top of its window, there's a list of plugins. To install any of them, first select the tool and then click the _Install/Update_ button. To uninstall a plugin, select it and click _Uninstall_. Some changes can't take effect until you restart Plover.

Some plugins are themselves tools. 

## Main window 

The main window can be used to reconnect the machine, enable and disable output and manage dictionaries.

### Dictionaries field 

This is the list of open dictionaries. One on each line. Dictionaries closer to the top have higher priorities, meaning if the same input is mapped to different outputs in different dictionaries, the one higher up gets to decide what Plover outputs for that input. For each dictionary, the following information is shown: 

- A number that shows the priority. Lower numbers mean higher priorities. To change the priority of a dictionary, select the dictionary (you can do that by clicking on the name of the dictionary in the list), then click the blue arrows below the list.
- If the dictionary can be read but not written by Plover, it'll show with a padlock next to the number. If there's a star there, it's the one that new entries will go into by default.
- A checkbox to enable and disable the dictionary.
- The name of the dictionary.

Below the list of dictionaries, there are buttons to do the following actions:

- Undo the last dictionary adding, deleting or reordering operation.
- Use the [[dictionary editor|Built-in tools#Dictionary editor]] on the selected dictionaries. It can edit and remove entries in the dictionaries and can also be used to look up what strokes or translations are mapped to. When it shows dictionary entries, it also shows which dictionaries they are in.
- Remove a dictionary from the list.
- Add a dictionary to the list.
- [[Add an entry|Built-in tools#Add translation dialog]] to the selected dictionary.
- Move the selected dictionaries up on the list.
- Move the selected dictionaries down on the list.

## Dictionary editor 

The dictionary editor can be used to to look up strokes and translations in dictionaries, and to edit or remove those entries. In the top of the window, there are two filter fields and below them is a list of dictionary entries.

At first, the list shows all entries in the dictionaries. To only show some of them, type something into the filter fields and click apply. Then the list will be filtered. To get entries with particular strokes, use the "filter by strokes" field. And to get entries that map to translations containing specific words, use the "filter by translation" field.

The strokes and translations on the list are editable.

Below the list are three buttons: 

- Undo last action.
- Remove selected entry/entries.
- Add a new entry.

## Add translation dialog

A dialog to add an entry to a dictionary. It has three fields:

- Which dictionary to add an entry to.
- The strokes to write the entry. Below this field you should see if those strokes are already mapped to anything in enabled dictionaries.
- What they should translate to. Below this field you should see any strokes already mapped to the translation.
- A cancel button that closes the dialog.
- An okay button that adds the entry and closes the dialog.