# femto

A minimal text editor written for fun in plain Ruby with no dependencies.

[![asciicast](https://asciinema.org/a/136688.png)](https://asciinema.org/a/136688)

I wrote it from memory after watching the [relevant screencast][screencast] by
[Gary Bernhardt][]. It supports:

* Quitting
* Moving the cursor up/down/right/left
* Deleting the character before the cursor, like backspace
* Breaking a line (`Enter`)
* Undoing!

## Additional functionality

The following are also implemented (not covered in the screencast):

* Flicker-free screen
* Ignoring non-printable characters
* Creating a file if it doesn't exist (not just editing)
* Saving
* Redoing!
* Moving left at the beginning of a line causes the cursor to jump to the end of
  the previous line
* Moving right at the end of a line causes the cursor to jump to the beginning
  of the next line
* Moving the cursor to the beginning of the line
* Moving the cursor to the end of the line
* Deleting the character before the cursor at the beginning of a line joins
  lines
* Deleting the character at the cursor, like delete
* Deleting the character at the cursor when at the end of a line joins lines
* Deleting the line text before the cursor
* Deleting the line text after (and including) the cursor
* Support for arrow, `Backspace`, `Delete`, `Home` and `End` keys

## Usage

~~~ sh
./femto.rb myfile.txt
~~~

## Keyboard shortcuts

* `Ctrl-Q` quits
* `Ctrl-S` saves
* `Ctrl-P` (previous), or the `Up` arrow key, moves the cursor up
* `Ctrl-N` (next), or the `Down` arrow key, moves the cursor down
* `Ctrl-F` (forward), or the `Right` arrow key, moves the cursor right
* `Ctrl-B` (backward), or the `Left` arrow key, moves the cursor left
* `Ctrl-A` or `Home` moves the cursor to the beginning of the line
* `Ctrl-E` or `End` moves the cursor to the end of the line
* `Ctrl-H` or `Backspace` deletes the previous character
* `Ctrl-D` or `Delete` deletes the current character
* `Ctrl-U` deletes the line text before the cursor
* `Ctrl-K` deletes the line text after (and including) the cursor
* `Ctrl--` undoes the last change
* `Ctrl-R` redoes the last change

## Roadmap

* Tests
* Scroll-buffer

## Disclaimer

This is an experimental program. Do NOT use it to edit files that you don't want
to lose/damage.

## License

[The Unlicense](https://github.com/agorf/femto/blob/master/LICENSE)

## Author

Angelos Orfanakos, <https://agorf.gr/>

[screencast]: https://www.destroyallsoftware.com/screencasts/catalog/text-editor-from-scratch
[Gary Bernhardt]: https://twitter.com/garybernhardt
