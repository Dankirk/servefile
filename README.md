
# Description
a mIRC script for sharing drag&dropped files with your friends on IRC.

# What does it do and how?

When you drag&drop file(s) or folder(s) on a channel or query window the script creates a temporary webserver, and then pastes an URL to the shared files to the target window. Other users can then simply double click the URLs to access files with their favorite browser.

# Setup
1. Copy servefile.ini and servefile.txt into your mIRC folder.
2. Edit servefile.ini to your liking.
3. (Only if behind NAT w/o UPnP): Edit your router settings to route traffic from the specified port (default 81) to your LAN address.
4. Run: /load -rs servefile.txt on any mIRC window.
5. Go to mIRC Options->Mouse->Drop and replace:

```
*.wav:/sound $1 $2-
*.*:/dcc send $1 $2-
```
... with this:
```
*:/servestart $1 $2-
```

