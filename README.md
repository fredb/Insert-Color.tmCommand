Insert-Color.tmCommand
======================

Workaround to bring back the Insert Color TextMate command.

I really miss the "Insert Color…" (S)CSS command and tried to fix it.

Due to a TM2 bug (filed [here][1]), there is no way (that I found) to launch the color picker from TM for now, so I tried to find a workaround.

To make it short, the only way I found is to launch the color picker from another app, ideally an always opened app with no window. I tried the menu bar items I use, none worked except [FastScrits][2].

So I made a command using this trick (or ugly hack if you prefer ;).

It's basically the same as the original Insert Color command with a few changes:

- It needs to send TM to the background then to the foreground to bring back focus to the docmment.
- You can use it even if you've not typed the color name/hex code, by selecting the color or puting the caret inside it (or at its boundaries so it's possiblle to invoke the command multiple times)
- It's scoped for source.css, source.scss and source.plist
- It return a lowercase hex code. You can remove the ".downcase" at the end of the command if you want your hex code uppercase.

I understand this is a hack and not every one uses FastScrits, but it works with the free (unregistered) version. A good occasion to try FastScrits and buy it if you like it.

**Tested with TextMate Version 2.0 (9309)**

[1]: https://github.com/textmate/textmate/issues/444
[2]: http://www.red-sweater.com/fastscripts/

