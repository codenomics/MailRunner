# MailRunner

A small, simple email app for Windows. It reads your inbox, lets you write and reply, and stays out of the way. Works with any email provider that supports IMAP and SMTP.

### Features

- Your whole folder list on the left, with unread counts and a quick-find box
- Optional saved message lists (off by default, encrypted) for instant folders
- Make, rename, move and delete folders; move messages with a button or by dragging
- Select several messages (Ctrl+click, Shift+click) to delete, move or mark them together
- Open .eml message files (double-click, or from the account menu)
- Search one folder or all folders (all folders: sender, recipient, subject; one folder: also the text)
- Message list with unread messages marked, newest first, 50 at a time
- Reading pane that shows HTML messages as designed, with links you can click
- Privacy first: pictures from the web are hidden until you click Show images (or choose Always show from this sender), and hidden tracking pictures are blocked and counted
- Unsubscribe button for mailing-list messages (always asks first)
- Point at a link to see where it really goes
- New message, Reply, Reply all and Forward (the original is quoted for you)
- Gmail with an app password (steps in READ ME FIRST)
- More than one email account, with a quick switch button and unread counts for the accounts you aren't looking at
- Mark all read, and a "Last checked" time
- A signature for each account, and the unread count in the window title
- Spellcheck while you write (uses the spell checker built into Windows)
- Open or save the files in a message, and attach files when you write (up to 20 MB)
- Sending works on port 587 or 465, and a copy goes into your Sent folder
- Delete moves a message to Trash (asks first if there is no Trash folder)
- Checks for new mail by itself every 5 minutes, with a sound (your own .wav if you like) and a small popup you can turn off
- Your password is stored encrypted, readable only by your Windows account
- Fills in the server names for Gmail, Outlook, Yahoo and iCloud
- Dark \*Runner look with a custom title bar and window snapping, plus 13 other looks to pick from in Settings &gt; Themes (Drake and Grey's Market have an old-monitor scanline effect you can turn off)

> This application is built by AI. I made this for myself and I'm uploading it to GitHub for backup and to share in case anyone can get any use out of it. It's pretty specific to my setup and my needs, but if you can get any use out of it, then enjoy.
>
> Use at your own risk. I offer no warranty or guarantees for this software.

## Download

**Latest version: v2.0** (Nov 3, 2026)

- [MailRunner_v2.0_no-install.zip](https://github.com/codenomics/MailRunner/releases/download/v2.0/MailRunner_v2.0_no-install.zip) - 155 KB
- [MailRunner_v2.0_Setup.exe](https://github.com/codenomics/MailRunner/releases/download/v2.0/MailRunner_v2.0_Setup.exe) - 556 KB
- [MailRunner_v2.0_source.zip](https://github.com/codenomics/MailRunner/releases/download/v2.0/MailRunner_v2.0_source.zip) - 144 KB

What's new in v2.0:

- Several email accounts, with a quick switch button and unread counts for the other accounts
- Search one folder or all folders
- Select several messages at once (Ctrl+click, Shift+click) to delete, move or mark them
- Open .eml message files
- New message, Reply, Reply all and Forward, with attachments
- Sending works on port 587 or 465, and a copy goes into your Sent folder
- Spellcheck while you write
- Pick your own new-mail sound, and an optional popup for new mail
- Settings split: app settings in Settings, account details under the account button
- Mark all read and a "Last checked" time
- Rename or move folders, and a signature for each account
- The unread count shows in the window title
- Passwords with accented letters now work
- Old-monitor scanline effect for the Drake and Grey's Market looks

Older versions are on the [Releases page](https://github.com/codenomics/MailRunner/releases).

## Getting started

### Installer (recommended)

1. Download the file ending in `_Setup.exe` above.
2. Double-click it and click Install. It installs just for you - no admin password needed - and adds Start menu and Desktop shortcuts.
3. To remove it later: Windows Settings > Apps, find MailRunner and click Uninstall.

### No install (portable zip)

1. Download the file ending in `_no-install.zip` above.
2. Right-click it > Extract All, and pick a folder. Don't run it from inside the zip.
3. Open the folder and double-click the app's .exe. Nothing is installed; delete the folder to remove it.

Windows says "Windows protected your PC"? Click More info > Run anyway. It shows that for apps without a paid signing certificate.

## Source code

Want to see how it works, or build it yourself? Download the file ending in `_source.zip` above, extract it and double-click `Build.bat`. It only uses the C# compiler that already comes with Windows, so there is nothing to install.

## More details

```
GETTING STARTED
---------------
Pick one. Both give you the same app.

OPTION 1 - INSTALLER (recommended)
  Download the file ending in _Setup.exe, double-click it and click Install.
  It installs just for you (no admin password) and adds Start menu and
  Desktop shortcuts. Needs Windows 10 or 11 (64-bit).
  To remove it later: Windows Settings > Apps > MailRunner > Uninstall.

OPTION 2 - NO INSTALL (zip)
  1. Download the file ending in _no-install.zip. Right-click it -> Extract
  All... and put the MailRunner folder somewhere it can stay (for example
  Documents). Don't run it from inside the zip.
  2. Double-click MailRunner.exe. Nothing is installed; to remove it, delete
  the folder.

EITHER WAY
  The first time, MailRunner asks for your email details (see below).
  Optional: pin it to Start (right-click it in the Start menu or on the
  desktop -> Pin to Start).

"Windows protected your PC"? Click "More info" -> "Run anyway".
Windows shows that for apps downloaded from the internet that aren't
signed with a paid certificate.


YOUR EMAIL DETAILS
------------------
You need your email address and password, the incoming (IMAP) server and
port (usually 993 with SSL/TLS), and the outgoing (SMTP) server with port
587. Your provider's help page lists them (search "<provider> IMAP
settings"). MailRunner fills in the server names for Gmail, Outlook, Yahoo
and iCloud.

Those four don't accept your everyday password from apps like this. Make an
"app password" in your account's security settings and type that instead.


USING IT
--------
- Click a folder on the left to open it. New folder, Rename (also moves a folder), Delete and
  "Move to..." (or drag a message onto a folder) keep things tidy.
- Click a message to read it. The arrow keys move through the list.
- New message: Ctrl+N. Reply: Ctrl+R. Reply all: Ctrl+Shift+R. Forward: Ctrl+L. Check mail: F5. Delete: the Delete key.
- "Load older messages" at the bottom of the list shows the next 50.
- Click a link in a message to open it in your browser. Point at it first to
  see where it goes.
- Pictures from the web are hidden at first. Use "Show images" or "Always
  show from this sender" in the bar above the message.

Not in this version: searching all your accounts at once. (Gmail keeps its own copy of sent mail, so MailRunner
doesn't add a second one there.)


GOOD TO KNOW
------------
- MailRunner only talks to your own mail server. Nothing is sent anywhere
  else, and there are no ads or tracking. Pictures from the web load only if
  you allow them, and then only from the sender's own pages.
- Messages are shown with the page viewer that comes with Windows. MailRunner
  saves one small setting for itself (for MailRunner.exe only) in your
  Windows user settings so pages look right.
- Updates: when MailRunner starts it checks GitHub for a newer version (it
  only reads the public release page; nothing is sent). If you used the
  installer, Update now downloads and runs the new installer for you. If you
  use the no-install zip, it opens the download page instead. The Updates
  button at the bottom checks on demand, and can turn the startup check off.
- Settings are kept in %APPDATA%\MailRunner\settings.txt and the encrypted
  password in %APPDATA%\MailRunner\account.dat.
- If something goes wrong, MailRunner-log.txt next to MailRunner.exe says
  what. It never contains your password.
- To remove MailRunner: delete its folder (or uninstall it), plus
  %APPDATA%\MailRunner.
```

