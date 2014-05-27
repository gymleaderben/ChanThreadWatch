# ChanThreadWatch

## Fork of the original ChanThreadWatch.

This project is a fork of the original ChanThreadWatch. All credit goes to the original developper.  
You can DOWNLOAD this program here: [https://github.com/SuperGouge/ChanThreadWatch/releases](https://github.com/SuperGouge/ChanThreadWatch/releases)  
You can find the original official site here: [https://sites.google.com/site/chanthreadwatch/](https://sites.google.com/site/chanthreadwatch/)

**DISCLAIMER:** The latest major version of this program (1.10) changes the handling of child threads.
If you used the auto-follow feature of the 1.9.0 version and still have child threads, they will be converted to the new format.
However, you are advised to make a backup of both your "threads.txt" file (in the "%AppData%\Chan Thread Watch" folder) and your child threads (nested in their parent's folder) in case anything happens during the conversion.

## Planned features
- Post highlighting by poster ID
- Custom automatic description (thread title, creation date, etc.)
- 4chan X compatible post-processed HTML
- Support for more imageboards

## Changelog
### 1.10.3 (2014-May-25):
- Fixed resurrected posts not being correctly added to output file.
- Added "[Deleted]" warning to resurrected posts.
- Dead links quoting resurrected posts are now resurrected too.
- Fixed some occasional exceptions during child threads conversion.

### 1.10.2 (2014-May-24):
- Fixed ArgumentOutOfRangeException occurring when thread list is empty.

### 1.10.1 (2014-May-24):
- Fixed OverflowException occurring when ClientSize setting had a 0 as a width or height.
- Fixed handling of child threads conversion during startup.

### 1.10.0 (2014-May-24):
- Ability to sort images by poster.
- Ability to edit all thread properties even after being added.
- Now keeps deleted/dead posts.
- Ability to follow only cross-links within the same board.
- Post-processed HTML now makes cross-links point to local threads paths if existing.
- Changed handling of child threads, now stored in base download directory.
- New settings to better customize the new handling of child threads.
- Greatly improved startup time especially for large thread lists.

### 1.9.0 (2014-Apr-25):
- Added auto-follow feature.
- Added categories.
- Added custom time interval.
- Program now remembers window size and columns widths across runs.
- Improved clarity when adding existing thread.
- Fixed thread sorting when adding new thread.
- Fixed auto-update to account for new project home.

### 1.8.1 (2014-Apr-21):
- Fix for "/thread/" URLs without slugs giving wrong folder name.
- Minor UI fixes.

### 1.8.0 (2014-Apr-20):
- Supports 4chan's new HTML.
- Supports 4chan's new URLs.
- Ability to include "slugs" in threads folder naming.
- Fix for duplicate watchers not being detected when URL is different but corresponds to same thread.
- Updated About window.

### 1.7.5 (2014-Jan-23):
- **Original project forked**
- Fix for 4chan.org images retrieval.

### 1.7.4 (2012-Sep-30):
- Fix spoiler images not being downloaded.

### 1.7.3 (2012-May-13):
- Fix "Stopped: Unknown error" caused by URL parsing.

### 1.7.2 (2012-May-13):
- Restore Mono compatibility.
- Improve character encoding detection.

### 1.7.1 (2012-May-03):
- Supports 4chan's new HTML.
- HTML post-processing makes most URLs absolute for better display and functionality of saved HTML (e.g. external stylesheet/scripts).
- Supports Krautchan.
- Supports loading on .NET 4.0 runtime (not required; still 2.0 compatible).

### 1.7.0 (2011-Jan-02):
- Added download progress window.
- Fixed broken image paths in HTML with folder renaming.
- Allows 30 second check interval on /b/.
- Allows multiple instances using different settings folders.
- Aborts downloads when stopping thread.
- Detects truncated downloads (hash check already caught this on 4chan).
- Prompts before opening more than 5 folders or URLs.
- Workarounds for several issues in Mono.

### 1.6.0 (2010-Dec-18):
- Replaced URL column with user customizable description.
- Added "Last Image On" and "Added On" columns.
- Made columns sortable.
- Option to rename thread download folders with the description.
- Ability to add threads by dropping a link or favicon.
- Added an application icon.
- Added shortcut key Ctrl+A to select all items.

### 1.5.0 (2010-Dec-05):
- Downloads multiple files within a thread concurrently.
- Workaround for downloads stalling when site is sluggish.
- Saves thread list when updated instead of just on exit.
- Saves stopped threads in thread list.
- Ability to add URL(s) from clipboard with single click.
- Ability to delete stopped threads from disk in the context menu.
- Allows only one instance to run at a time.

### 1.4.3 (2010-Nov-26):
- Download folder in thread list is stored as relative path.

### 1.4.2 (2010-Apr-02):
- Fixed crash with non-4chan threads containing mailto links.
- Enabled auto-scaling to fix text truncation with larger font sizes.
- Enter key is a shortcut for "Add Thread".
- Backs up the page before redownloading in case it 404s in the middle of downloading.
- Fixed non-breaking spaces being converted to spaces when post-processing HTML.

### 1.4.1 (2010-Jan-01):
- Workaround for crash in Mono when program update checking is enabled.

### 1.4.0 (2010-Jan-01):
- Option to download thumbnails and post-process HTML to create a mostly-working thread backup (no external CSS, no embedded images other than thumbnails, etc).
- Fixed handling of special characters in filenames.
- Ability to restart stopped threads in the context menu.

### 1.3.0 (2009-Dec-28):
- Option to verify hash of downloaded images (currently 4chan only).
- Option to save images with original filenames (currently 4chan only).
- Option to automatically check for program updates (disabled by default).
- Various fixes related to URL parsing, file error handling, etc.

### 1.2.3 (2009-Dec-25):
- Restores 4chan and AnonIB support.
- Custom link parsing and other code to allow for automatic downloading of multiple page threads (not implemented for any site at this time as I didn't find any I wanted to support).
### 1.2.2 (2009-Aug-22):
- Download folder can be relative to the executable folder.
- Settings and thread list can be saved in the executable folder instead of the application data folder.
- Detects image wrapper pages and sends referer for better site compatibility.
- Locking is utilized properly when exiting.

### 1.2.1 (2009-May-06):
- Works with HTTPS sites (stupid bug).

### 1.2.0 (2009-May-05):
- Settings are remembered across runs.
- Thread list is remembered across runs, with a prompt at start before reloading.
- Main window is resizable.
- Download location is configurable. Default download location is now in My Documents for limited user account compatibility.
- User Agent is configurable.
- Added context menu for the thread list. Moved Stop and Open Folder buttons there and added new features: Open URL, Copy URL, Check Now, Check Every X Minutes.
- Double-clicking a thread can open its folder or URL (configurable).

### 1.1.3 (2008-Jul-08):
- Restores AnonIB support.

### 1.1.2 (2008-Jun-29):
- Ignores duplicate filenames when creating image URL list; fixes incorrect image count on 4chan.
- Doesn't convert page URL to lowercase; fixes 404 problem when page URL contains uppercase characters.

### 1.1.1 (2008-Jan-16):
- Workarounds for Mono's form scaling problems and HttpWebResponse LastModified bug.

### 1.1.0 (2008-Jan-07):
- Fixed UI sluggishness and freezing caused by accidentally leaving a Sleep inside one of the locks for debugging.
- Supports AnonIB.

### 1.0.0 (2007-Dec-05):
- Initial release.
