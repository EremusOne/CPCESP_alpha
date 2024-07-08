![CPCESP](https://zxespectrum.speccy.org/wp-content/uploads/2024/07/CPCESP-final.png)

This is an emulator of the Amstrad CPC family of 8 bit home microcomputers running on Espressif ESP32 SoC powered boards.

Currently, it can be used "out of the box" with Lilygo's TTGo VGA32 board and Olimex's ESP32-SBC-FabGL board.

Just connect a VGA monitor or CRT TV (with special VGA-RGB cable needed), a PS/2 keyboard, prepare a SD Card as needed and power via microUSB.

This emulator is part of the [ESPectrum project](https://github.com/EremusOne/ESPectrum) and, in the near future, will be integrated on it.

## Features

- Emulation of CPC 464, 664 and 6128 models
- State of the art Z80 emulation (Authored by [José Luis Sánchez](https://github.com/jsanchezv/z80cpp))
- 6 bpp VGA output (384x288, 400x300 and 720x288 resolutions @ 60 and 50hz modes) and CRT 15khz output ( 384x288 and 768x288 @ 50hz modes via VGA to RGB Scart cable).
- AY-3-8912 sound emulation.
- Complete CPC keyboard emulation mapped to PS/2 keyboard.
- Loading of SNA (64K) and DSK file types.
- Complete file navigation system with autoindexing, folder support and search functions.
- OSD menu in two languages: English & Spanish.

## Work in progress

- Everything! :D The emulator is in alpha stage (but with a lot of titles yet working perfectly :D ) and there's a lot of pending improvement: better SNA and DSK format support, TZX and CDT format support and snapshot saving and loading are the next things we probably add. Also, CRTC, GA and PPI emulation will get better at every release.

## Installing

You can flash the binaries directly to the board. Check the [releases section](https://github.com/EremusOne/CPCESP_alpha/releases)

## Compiling

The source code of the emulator will be published soon so you'll be able to compile it in the same way as ESPectrum project. Stay tuned!

## How to prepare micro SD Card

The SD card should be formatted in FAT16 / FAT32.

Just that: then put your .sna and .dsk whenever you like and create and use folders as you need.

There's also no need to sort files using external utilities: the emulator creates and updates indexes to sort files in folders by itself.

## Video modes supported

Default video mode is VGA 384x288 60hz. Emulator will start in this mode.

To change video mode press repeatedly this combination of keys just after powering on or after cold reset (F12):

- 1 + Q -> 384x288 VGA 60hz
- 2 + Q -> 400x300 VGA 60hz
- 3 + Q -> 720x288 VGA 60hz (real mode 2)
- 1 + W -> 384x288 VGA 50hz
- 2 + W -> 400x300 VGA50hz
- 3 + W -> 720x288 VGA 50 hz (real mode 2)
- 1 + E -> 384x288 CRT 15khz 50hz
- 2 + E -> 384x288 CRT 15khz 50hz
- 3 + E -> 768x288 CRT 15khz 50hz (real mode 2)

You can check current video mode at lower line of help or hardware info dialogs.

## PS/2 Keyboard functions

- F1 Main menu
- F2 Load SNA
- F5 Load DSK
- F8 CPU stats ( [CPU] microsecs per CPU cycle, [IDL] idle microsecs, [FPS] Frames per second, [FND] FPS w/no delay applied )
- F9 Volume down
- F10 Volume up
- F11 Hard reset
- F12 Reset ESP32
- CTRL + F1 Hardware info
- CTRL + F2 Turbo mode
- CTRL + F5..F8 Screen centering in CRT 15K/50hz mode
- Pause Pause

## Project links

- [Website](https://zxespectrum.speccy.org)
- [Youtube Channel](https://www.youtube.com/@ZXESPectrum)
- [Twitter](https://twitter.com/ZX_ESPectrum)
- [Telegram](https://t.me/ZXESPectrum)

## Contribute

CPCESP is open source sofware licensed under GPL v3, you can use modify and share it for free. If you like CPCESP, please consider becoming Patreon or donating through Paypal. Your support help us to maintain and improve the project for all users. You can do it at the following links:

- [Patreon](https://www.patreon.com/ESPectrum)
- [Paypal](https://www.paypal.com/donate/?hosted_button_id=43GGRCYDS3K5S)

## Supported hardware

- [Lilygo FabGL VGA32](https://www.lilygo.cc/products/fabgl-vga32?_pos=1&_sid=b28e8cac0&_ss=r)
- [ESP32-SBC-FabGL board from Olimex](https://www.olimex.com/Products/Retro-Computers/ESP32-SBC-FabGL/open-source-hardware)

## Thanks to

- [Ackerman](https://github.com/rpsubc8) for his [CPC emulator port](https://github.com/rpsubc8/ESP32TinyCPC) to ESP32.
- [Juan Carlos González Amestoy](https://www.retrovirtualmachine.org) for his excellent emulator and his friendly help.
- Z80 Emulation derived from [z80cpp](https://github.com/jsanchezv/z80cpp), authored by José Luis Sánchez.
- VGA Driver from [ESP32Lib by BitLuni](https://github.com/bitluni/ESP32Lib).
- AY-3-8912 emulation from [libayemu by Alexander Sashnov](https://asashnov.github.io/libayemu.html).
- PS2 Driver from Fabrizio di Vittorio for his [FabGL library](https://github.com/fdivitto/FabGL).
- [Amstrad PLC](https://web.archive.org/web/20190125111043/http://www.amstrad.com/) for kindly giving it's permission for it's copyrighted material to be redistributed (but Amstrad retains it's copyright).
- [Jean Thomas](https://github.com/jeanthom/ESP32-APLL-cal) for his ESP32 APLL calculator.

## Thanks also to

- [Retrowiki](http://retrowiki.es/) especially the people at [ESP32 TTGO VGA32](http://retrowiki.es/viewforum.php?f=114) subforum.
- [RetroReal](https://www.youtube.com/@retroreal) for his kindness and hospitality and his great work.
- [AUA - Amigos y usuarios de Amstrad](https://auamstrad.es/) en especial a Pablo Forcén y a [Manuel Cuenca](https://www.youtube.com/@manuelcuencammchip).
- David Crespo [David programa](https://www.youtube.com/@Davidprograma)
- Rodrigo Méndez [Ron](https://www.twitch.tv/retrocrypta)
- Armand López [El Viejoven FX](https://www.youtube.com/@ElViejovenFX)
- Javi Ortiz [El Spectrumero](https://www.youtube.com/@ElSpectrumeroJaviOrtiz) 
- José Luis Rodríguez [VidaExtraRetro](https://www.twitch.tv/vidaextraretro)

## And, of course, thanks to

- [Roland Perry](https://fr.wikipedia.org/wiki/Roland_Perry).
- [Alan Michael Sugar](https://en.wikipedia.org/wiki/Alan_Sugar).
