# Extras for Sublime Text 3

## abp.tmLanguage

[Sublime Text 3][st3] syntax definition and color scheme for [Adblock Plus filter lists][abp].

### Installation

1. Download `FreshCut.tmLanguage` from [Colour Schemes by Dayle Rees][freshcut].
2. Run `./build create abp`
3. Copy `abp.sublime-settings`, `abp.tmLanguage` and `abp.tmTheme` to the `Packages/User/` directory.

## todo.tmLanguage

[Sublime Text 3][st3] syntax definition and color scheme for plain text files containing lists of tasks that need to be done (i.e. ToDos).

### Syntax

Start a TODO block using `TODO:`, optionally followed by a title, as its first line. Finally, you can end the TODO block using `:TODO` as the last line.

Within the TODO block you can add tasks that start with one of the characters below followed by a whitespace:

- `!`: Task is open and important
- `-`: Task is open
- `?`: Task is uncertain, optional or merely a suggestion
- `o`: Task is in progress
- `/`: Task is blocked and cannot be worked on right now
- `x`: Task is done
- `#`: Task cannot be worked on (i.e. it's already done, handled by someone else or impossible to get done)

#### Example

```
TODO: Features
- add way to search for items
  don't forget to add placeholder to search input box
x add way to remove items
:TODO

TODO: Bugs
o removing items doesn't work
  o fix: item not removed from database
  x fix: item not removed from view
:TODO
```

### Installation

1. Download `FreshCut.tmLanguage` from [Colour Schemes by Dayle Rees][freshcut].
2. Run `./build create todo`
3. Copy `todo.sublime-settings`, `todo.tmLanguage` and `todo.tmTheme` to the `Packages/User/` directory.

## Development environment

### Requirements (Linux)
-  [FreshCut.tmLanguage][freshcut]
- `xltproc`

### Workflow (Linux)

1. Modify `language.yaml`, `settings.json` and/or `theme.yaml`.
2. Run `./build deploy <syntax>` to update the files in Sublime's user directory.

[abp]: https://adblockplus.org/en/filters
[freshcut]: https://github.com/daylerees/colour-schemes/blob/master/legacy/Contrast/FreshCut.tmTheme
[st3]: http://www.sublimetext.com/
