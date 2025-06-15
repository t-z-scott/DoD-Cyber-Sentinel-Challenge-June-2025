**Difficulty: Very Easy**

_Description:_ Agents intercepted an audio file named `message.mp3`. It plays a single tone, but we have intel that a flag might be tucked away in the metadata fields of the file. Can you inspect the file and uncover the flag?

# Completion Steps
1. Download the file.
2. Download a file analyzer. I'm using [Exiftool](https://exiftool.org/), a quick and easy-to-use command-line tool for reading file metadata.
3. Go to your terminal and run this command: `exiftool message.mp3` (or the equivalent command for your file analyzer).

> **Flag:** C1{metadata_tells_more}
