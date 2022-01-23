# woslicerII English Translation

> Update 01/23/2022 (2): added proper patch for FL 20.9, version now works with both regular and FL 20.9 files
> Update 01/23/2022: added patch for FL 20.9

Translation by Sayaka, with help from w, Dolphin and marie  
Original japanese version by wosderge: https://cerebralmuddystream.nekokan.dyndns.info

- `woslicerII_s_eng.exe` is the regular woslicerII translated in english, with no other modifications
- `woslicerII_s_eng_initmod.exe` is a very slightly modded version of woslicerII that initializes fadeout, offset to 0 and disables cutting volume on startup
- `woslicerII_s_eng_initmod_fl.exe` is the same file as `woslicerII_s_eng_initmod.exe`, but patched to make it work with FL 20.9 generated WAV files. These add a JUNK block at the start of the WAV file to pad the chunks, messing with woslicerII's header parsing routine.

If you wish to do the FL 20.9 patch on an unmodded / untranslated version, you can do so by patching byte `0x00003568` from `0x16` to `0x3A` using an hexadecimal editor.
**Keep in mind that patch will only make it work with FL 20.9-generated WAV files; all other WAV files will make the program crash.**
The included EXE fix uses a more complex fix that accounts for that issue; if there is demand to do a fixed version for the untranslated / unmodded version, I might do it in the future.

The IDA databases for the translation and patches are also provided in the repository (`idb` files, both also contains patches for `woslicerII_s_eng_initmod.exe`)

If you encounter any issues, please join the BMS Community Discord and ask your question there: https://discord.gg/Q4vKF8T