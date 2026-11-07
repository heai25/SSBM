Super Smash Bros. Melee (NTSC 1.02) - native PC port
=====================================================

Start "Melee Launcher.exe", choose your settings and press PLAY.

Files
  Melee Launcher.exe   settings + start the game
  game.exe             the game (recompiled from the GameCube code; can be started directly)
  SDL2.dll             audio
  vcruntime140*.dll    Visual C++ runtime
  cache\               pre-built shader list, so matches don't stutter the first time
                       an effect appears (grows by itself as you play)
  *.iso                your Super Smash Bros. Melee (USA) Rev 2 disc image
  background.png/.jpg  (optional) launcher background picture

Launcher options
  Resolution     360p to 4K (the game renders at that height)
  Anti-aliasing  Off / 2x / 4x / 8x MSAA
  Display        16:9 Widescreen, Fullscreen
  Latency        V-Sync on = smooth with no tearing, still low latency.
                 V-Sync off = lowest possible input latency (the picture may tear).
  Extras         Debug Menu, Sound Test, Unlock everything (characters, stages, modes)
  Game disc      uses the .iso in this folder; "Browse..." to pick another one

Controls (keyboard; gamepads also work, controllers 2-4 = players 2-4)
  WASD / arrows   control stick     Space   A        X   B
  C / V           X / Y             Q / E   L / R    Z   Z
  Enter           Start
  Esc             pause and ask "Quit the game?"

Saves go to saves\card_a (Dolphin-compatible .gci files).
The last run's log is game.log; launcher settings are kept in launcher.ini.

Command line (game.exe): --res 1920x1080 --msaa 4 --widescreen --fullscreen --no-vsync
                         --patch "Debug Menu" --iso "D:\path\melee.iso"
"Melee Launcher.exe --play" starts the game with the saved settings.

Known issues (work in progress)
  - The intro movie shows a green screen (movie decoding not done yet); press Start.
  - Some stages have bugs: Great Bay can stop with an error mid-match and Brinstar
    can freeze at the start of a match. Yoshi's Story and the menus are fine.
  - The off-screen character bubble (magnifier) shows garbage.
