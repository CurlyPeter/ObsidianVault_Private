[**Take a screen shot and save to desktop with current time as the name**](https://stackoverflow.com/questions/16797998/take-a-screen-shot-and-save-to-desktop-with-current-time-as-the-name)
screencapture -i ~/Desktop/$(date +%Y%m%d%H%M%S).png
-i is interactive mode (like ⇧⌘4). The default file name format is like this on my installation:
date '+Screen Shot %Y-%m-%d at %-H.%M.%S %p.png'
See man screencapture and man strftime.
If you use AppleScript, the run handler is not needed, /usr/sbin/ is on the path by default, and you can escape arguments with quoted form of.
"Screen Shot " & (current date) & ".png"
do shell script "screencapture ~/Desktop/" & quoted form of result