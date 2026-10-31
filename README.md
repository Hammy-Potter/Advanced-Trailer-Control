# Advanced Trailer Control

Independent trailer steering, axle-model control and shared suspension controls for ETS2. Designed for heavy haulage and modular trailer combinations.

**Target build:** ETS2 1.61.1.9 · Windows x64 · DirectX 11

## Features

- Independent manual steering for trailers 1–4.
- Adjustable steering and suspension movement times, from 2–10 seconds.
- Shared raise, lower and ride-height controls for attached trailers.
- Customisable keyboard and controller bindings.
- Compact remote-style interface with an optional transparent background.
- Remembers the selected steering mode and Multi-Module trailer pair between sessions.
- Optional geometry and movement capture for troubleshooting.

## Steering modes

**Multi-Module Mode:** Controls two modules connected with articulation-locked joint limits as one trailer.

**BBM Mode:** Supports compatible BBM ST3, ST4 and ST7 bogies, with up to 60° of bogie rotation. Movement-based wheel following controls the front axle on ST3, the front two on ST4 and all seven on ST7.

**Bridge Mode:** Controls the bridge and rear module together through one steering input. Supports compatible modular bridge combinations, including Sigouss’ Mega Wind Transport mod.

**Bridge Mode – Expert:** Supports the same bridge combinations with individual control of steerable sections.

**MWT Mode:** Supports the three-section front jeep, tower frame and seven-axle rear bogie combination from Sigouss’ Mega Wind Transport mod. Coordinates bogie tracking and individual axle steering, with manual control and powered-joint assistance when reversing.

Both bridge modes and MWT Mode support holding the rear module’s chosen angle after releasing manual input. Select Auto to resume automatic tracking. Select modes while stopped; compatibility checks must pass before specialised control activates.

## Installation

1. Close the game.
2. In **Releases**, download **Advanced-Trailer-Control.dll** directly. Alternatively, download **Advanced-Trailer-Control.zip** and extract it for the DLL and installation instructions. The source-code downloads are not needed to play.
3. Copy `Advanced-Trailer-Control.dll` into:
   `Euro Truck Simulator 2/bin/win_x64/plugins/`
4. Create the `plugins` folder if necessary. The DLL must be **inside** it.
5. Start the game. Press **Insert** to open the panel and **Home** to toggle the cursor.
6. Configure your bindings and select the appropriate steering mode in Settings.

When updating, replace the DLL and retain your existing JSON settings. The remote add-on is optional and is not required for local controls.

## Troubleshooting

Check that you are using the supported game build and DirectX 11, and that the DLL is in `win_x64/plugins`, not directly in `win_x64` or in `win_x86`.

For steering reports, open Settings → Diagnostics and use **Capture geometry / log details**, then reproduce the problem during the 20-second capture and provide `game.log.txt`. Routine correction logs are disabled outside requested captures.

This plugin is not supported on TruckersMP.

## Source and building

Complete source is included in `Advanced-Trailer-Control-repository.zip` in this repository. Extract that archive before building. The CMake project requires a Windows C++17 compiler and Windows/DirectX libraries. MinHook is included under `vendor/minhook`; set `MINHOOK_SOURCE_DIR` to its absolute path when configuring CMake. The existing Visual Studio project is also included. Dependencies retain their own source notices.

## Disclaimer

© 2026 Potter Customs. Copyright applies to original contributions by Potter Customs.

Advanced Trailer Control is an unofficial community plugin and is not affiliated with or endorsed by SCS Software.

This plugin is distributed for personal and non-commercial use. No warranties are provided. Use at your own risk. It is advised against to make any changes to this plugin as it may lose some or most of its functionality.
