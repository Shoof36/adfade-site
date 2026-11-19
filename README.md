# adfade-site

AdFade's public website: the pages the App Store listing links to (support,
privacy policy) and one file the app reads (the shortcut's link). Served by
GitHub Pages at https://shoof36.github.io/adfade-site/. Everything here is
public the moment it is pushed.

It is its own GitHub repository (Shoof36/adfade-site, public), apart from the
app's code (the `adfade` folder beside it, private). Keep the two folders
side by side: the app's signing tool writes `../adfade-site/shortcut.json`.

## support.html

AdFade's support page: the Support URL on the App Store listing
(https://shoof36.github.io/adfade-site/support.html). Its contact address,
and the privacy policy's, is the mailbox the developer's other app uses
(published 2026-11-19). Don't move it: the listing links here.

## shortcut.json

The AdFade Break shortcut that the app's **Add the shortcut** button opens
(iPhone, Music tab, the Music app source):

```json
{"link": "https://www.icloud.com/shortcuts/<32 letters and digits>", "signature": "<base64>"}
```

An iCloud shortcut link is a frozen copy of the shortcut: a changed shortcut
needs a new link (in Shortcuts, the shortcut's Share → Copy iCloud Link).
Put the new link here, then sign it from the adfade repository:

    /c/flutter/bin/dart tool/sign_shortcut.dart

It signs the link with AdFade's key (Ed25519; the private half is in
`App-Store/AdFade Listing/adfade-files/shortcut-signing-key.txt`, never in a
repository) and writes
the signature beside it. Commit and push, and AdFade opens the new link
within about ten minutes, GitHub Pages' cache time. From build 17 the app
takes only an iCloud shortcut link signed with that key, so whoever could
change this site still couldn't send people to another shortcut; builds 11
to 16 read the link alone. Anything else, or no answer within 3 seconds,
and it opens the link it was built with.

The shortcut must keep its name, **AdFade Break**: COMMERCIAL runs it by that
name.

Don't rename this repository or move the file: the app reads it at this
address.

## privacy.html

AdFade's privacy policy. The app's AdFade Pro screen links to it (from build
14), and App Store Connect's privacy policy field should give this address:
https://shoof36.github.io/adfade-site/privacy.html. Keep it true to what the
app does, and put the date at the top when it changes. Don't move it.
