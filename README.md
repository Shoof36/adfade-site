# adfade-site

Files the AdFade app reads, served by GitHub Pages at
https://shoof36.github.io/adfade-site/.

## shortcut.json

The AdFade Break shortcut that the app's **Add the shortcut** button opens
(iPhone, Music tab, the Music app source):

```json
{"link": "https://www.icloud.com/shortcuts/<32 letters and digits>"}
```

An iCloud shortcut link is a frozen copy of the shortcut: a changed shortcut
needs a new link (in Shortcuts, the shortcut's Share → Copy iCloud Link).
Put the new link here and AdFade (build 11 and later) opens it within about
ten minutes, GitHub Pages' cache time. The app takes only an iCloud shortcut
link: anything else, or no answer within 3 seconds, and it opens the link it
was built with.

The shortcut must keep its name, **AdFade Break**: COMMERCIAL runs it by that
name.

Don't rename this repository or move the file: the app reads it at this
address.
