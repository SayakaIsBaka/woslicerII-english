# woslicerII English Translation

> Update 01/23/2022: added patch for FL 20.9

Translation by Sayaka, with help from w, Dolphin and marie  
Original japanese version by wosderge: https://cerebralmuddystream.nekokan.dyndns.info

- `woslicerII_s_eng.exe` is the regular woslicerII translated in english, with no other modifications
- `woslicerII_s_eng_initmod.exe` is a very slightly modded version of woslicerII that initializes fadeout, offset to 0 and disables cutting volume on startup
- `woslicerII_s_eng_initmod_fl.exe` is the same file as `woslicerII_s_eng_initmod.exe`, but patched to make it work with FL 20.9 generated WAV files. These add a JUNK block at the start of the WAV file to pad the chunks, messing with woslicerII's header parsing routine. **This version only works with WAV files generated with FL 20.9; any other WAV file will make the program crash.**

If you wish to do the FL 20.9 patch on an unmodded / untranslated version, you can do so by patching byte `0x00003568` from `0x16` to `0x3A` using an hexadecimal editor.
The IDA databases for the translation and patches are also provided in the repository (`idb` files, both also contains patches for `woslicerII_s_eng_initmod.exe`)

If you encounter any issues, please join the BMS Community Discord and ask your question there: https://discord.gg/Q4vKF8T