**Difficulty: Very Easy**

_Description:_ Analysts recovered a suspicious image from a threat actor’s social media account. At first glance, it looks like an innocent selfie - but insider reports suggest that a flag might be hiding in the image metadata. Can you extract it?

# Completion Steps
1. Download the provided image.
2. Download a file analyzer. I'm using [Exiftool](https://exiftool.org/), a quick and easy-to-use command-line tool for reading file metadata.
3. Go to your terminal and run this command: `exiftool image.png` (or the equivalent command for your file analyzer). You should see the flag in the metadata under Comment.
   - Tip: To find the flag faster, use grep to search the results for the flag. `exiftool image.png | grep C1{` would run the results of the first command through the second and output only the flag.

> **Flag:** C1{smile_youre_flagged}
