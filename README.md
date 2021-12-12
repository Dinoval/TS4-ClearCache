# TS4-ClearCache
A tiny file that can be put into The Sims 4 root directory and double-clicked to remove common cache files. Perfect for updating a modded game. *Only works on Windows.*

## Instructions
1. Download `ClearCache.bat`.
2. Move `ClearCache.bat` into your Sims 4 folder. It probably looks like `C:\Users\[your name]\Documents\Electronic Arts\The Sims 4`. ***Do not put it in your Mods folder; it needs to be in the root.***
3. (Optional) Move any caches you want to save to a non-default location.
4. Double-click `ClearCache.bat` to run it. 

- If you see a window open, your computer's struggling with clearing something. The window closes on its own once the process is complete.


## FAQ

**Q: What caches does ClearCache.bat clear?**

**A:** As of the November 20th 2021 version:
- localthumbcache.package
- avatarcache.package
- lastException.txt
- lastUIException.txt
- lastCrash.txt
- lastCleanException.txt
- BE-ExceptionReport.html
- mc_lastexception.html (if found in `\Mods\MC Command Center\`)
- mc_cmd_center.log (if found in `\Mods\MC Command Center\`)
- spellbook_injector.log (if found in `\Mods\`)
- NC4T_PickpocketingMod.log (if found in `\Mods\NC4T\`)


**Q: A security window popped up! / My anti-virus deleted ClearCache.bat!**

**A:** Malicious Batch files can completely destroy your computer, so it's understandable for it (and you) to be worried. If your computer is really uptight and absolutely refuses to run a Batch file from an unknown source, create your own file by doing the following: 
1. Click on `ClearCache.bat` on GitHub to view its contents
2. Open your Sims 4 folder
3. Right click in an empty space in the folder
4. Choose `New > Text Document`
5. Call it `ClearCache`
6. Double-click to open it in Notepad
7. Copy/paste the contents of GitHub's ClearCache.bat
8. Save and close
9. Right-click `ClearCache`
10. Choose `Properties`
11. Change `ClearCache.txt` to `ClearCache.bat`
12. Choose yes when prompted
13. Close out of the properties window

**Q: ClearCache.bat asks for the admin password!**

**A:**

- If you are the main owner of the computer: You're so responsible for turning up your Windows security! I recommend marking ClearCache.bat as always allowed so you don't have to retype your password every time you run it, or - safer yet - set your security to only darken the screen without asking for the password.

- If you are NOT the main owner of the computer: Sorry, but your computer's too careful. You can try the above method of creating your own file, but most likely my program will not run at all without your admin's permission. :(

**Q: Will you add [mod cache]?**

**A:** Sure, if it complies with TS4's ToS, is SFW, and the author stays out of trouble. Just mention me. :)

**Q: Will you make ClearCache.bat stop clearing [cache]?**

**A:** Only if it's affecting gameplay, in that case let me know ASAP.

**Q: Will you change the file hirarchy / where ClearCache.bat looks for mod caches?**

**A:** No.

**Q: Can I add/remove/change caches in ClearCache.bat on my own?**

**A:** Go for it! You'll need to be able to read Batch, but trust me: it's super easy and a great first programming language.
1. Right click `ClearCache.bat`
2. Choose `Edit`

Tips:
- You only need to worry about the lines beginning in `DEL`.
- You must "quote" file names with spaces in them; I just quote the whole command just in case.
- To clear mod caches, you have to spell out the path to them, such as `"%~dp0\Mods\mods NC4T\NC4T_PickpocketingMod.log"`.
  - `%~dp0` is the short name for the current folder, so `%~dp0\Mods\` is the path to the `Mods` folder.
- If a cache ends with a bunch of numbers or other random junk, type out as much as you can and put an astrick* at the end. For example, `DEL lastException*` looks through the Sims 4 folder and gets rid of `lastException45675248.txt`, `lastException46819815.txt`, and `lastExceptionLOL.meme`.

**Q: ClearCache.bat cleared something I wanted to keep!**

**A:** Don't worry, it sends everything to the Recycle Bin.
