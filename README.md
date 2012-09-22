Insert-Color.tmCommand
======================

Workaround to bring back the Insert Color TextMate command.

I really miss the "Insert Color…" (S)CSS command and tried to fix it.

Due to a TM2 bug (filed [here][1]), there is no way (that I found) to launch the color picker from TM for now, so I tried to find a workaround.

First I used [FastScrits][2] to launch the color picker and made a command using this trick (or ugly hack if you prefer ;).

Then [@nobios][3] pointed me to "Applescript Runner" so no third party app is required anymore.

It's basically the same as the original Insert Color command with a few changes:

- It needs to send TM to the background then to the foreground to bring back focus to the document.
- You can use it even if you've not typed the color name/hex code, by selecting the color or putting the caret inside it (or at its boundaries so it's possiblle to invoke the command multiple times)
- It's scoped for source.css and source.scss
- It return a lowercase hex code. You can remove the ".downcase" at the end of the command if you want your hex code uppercase.

Clone or download the zip and double click the tmCommand, then deactivate the original command(s).

**Tested with TextMate Version 2.0 (9313)**

[1]: https://github.com/textmate/textmate/issues/444
[2]: http://www.red-sweater.com/fastscripts/
[3]: https://github.com/nobios