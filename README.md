# Shadow of the Colossus — Handheld Edition

An unofficial Android port of the PlayStation 2 game, adapted for handhelds and phones by **GhostScitSMT**. Play with a physical controller or customizable touch controls, choose original PlayStation or Switch-style button prompts, and adjust the display for your device.

**Current build:** v0.14.4 Driver Preview

## Requirements

- A 64-bit ARM Android device running **Android 9 or newer** with **OpenGL ES 3.0** support.
- Your own uncompressed **USA** copy of *Shadow of the Colossus* in `.iso` format. The supported disc ID is **SCUS-97472**.
- About **6 GB of free storage** for the initial import.

## Download and install

1. Open the repository’s **Releases** tab and download the APK from the preview release assets.
2. Open the APK on your Android device. If Android asks, allow installations from the browser or file manager you used to open it.
3. Launch **Shadow Driver Preview**, open the **Play** tab, and tap **Choose USA ISO**.
4. Select your `.iso` file. If it’s inside a ZIP or 7z archive, extract it first.
5. Keep the app open until the launcher shows **Ready to play**, then tap **Play**.

## Controls

- **Physical controller.** Open **Controls** in the launcher to choose Classic, Responsive, or Modern controls. Use **Calibrate buttons** if the face buttons are mapped incorrectly.
- **Button prompts.** Toggle **Switch button icons** under **Controls** to switch between original PlayStation symbols and Switch-style labels. The selection applies to the game prompts and touch controls the next time you launch the game.
- **Touch layout.** During gameplay, tap **Touch → Edit layout** to move and resize controls, adjust each button’s opacity, or turn on **Grid** for easier alignment. Tap **Save** to keep the layout.
- **Touch camera.** Under **Touch → Touch camera**, choose **Screen drag** or **Right stick**. In Screen drag mode, drag an empty part of the screen to move the camera. Adjust the response from **50% to 200%** under **Touch → Screen drag sensitivity**.
- **Game menu.** Tap **Menu** at the top center or swipe left from the right edge. Choose **Return to launcher** to go back to the main screen. Double-tap **Select** to open the in-game settings hub.

## What’s new in v0.14.4

- The **left touch stick** uses your first touch as its neutral point. An off-center touch won’t move Wander until you drag.
- Small drags give you finer movement, full speed takes less thumb travel, and diagonals use the same maximum input strength as straight movement.
- Screen drag picks up the final part of quick camera swipes when you lift your finger.
- The **Touch** menu scrolls so the layout, opacity, camera, frame limiter, and rotation options stay reachable.
- **Touch → Screen rotation** offers standard landscape, a 180° flip, and automatic landscape rotation. See the AYN Thor issue below.

## Display and graphics drivers

Open **Display** in the launcher to choose **Original**, **720p**, or **1080p** output. For widescreen, select **16:9** in both the launcher and the game’s own Options menu. Enable **Fill the entire screen** to remove the bars. Filling a display with a different aspect ratio can stretch the image.

During gameplay, **Touch → Frame limiter** offers the game default and **30**, **45**, or **60 FPS** caps. The limiter controls frame presentation. Use the **game FPS** reading in the HUD when checking for gameplay slowdown.

The **system driver** is selected by default. The experimental **GPU** tab can import compatible ARM64 Turnip ZIPs for Qualcomm Adreno devices. Driver changes apply the next time you press **Play**.

## Tested devices

All results in this chart used the **system graphics driver**. FPS values are spot checks from the in-game HUD. The new touch controls were verified on AYN Thor. The other devices were tested on the earlier builds shown below.

| Device | GPU and system driver | Test results | Suggested starting settings |
| --- | --- | --- | --- |
| **AYN Thor** | Adreno 740 · Qualcomm `V@0676.53` | Verified short camera swipes on **v0.14.3** and left-stick movement and release in gameplay on **v0.14.4**. Earlier 1080p tests showed **35–52 game FPS** in parts of the courtyard and around **60** in lighter scenes. | **1080p widescreen**. Try **720p** if heavier scenes slow down. |
| **Retroid Pocket Flip 2** | Adreno 650 · Qualcomm `V@0746.0` | **v0.14.1** reached the intro and mounted the existing memory card. One intro sample showed **60 game FPS**. | **720p widescreen** with the default frame limiter. |
| **Motorola Edge (2024)** | Adreno 710 · Qualcomm `V@0615.98` | **v0.14.2** reached live gameplay. Two climbing samples at 720p showed **18–22 game FPS**. | **720p widescreen** was tested. The **Performance** preset with a lower internal render scale still needs testing on this phone. |
| **Moto G 5G (2024)** | Adreno 619 · Qualcomm `V@0530.55` | **v0.14.1** imported the USA ISO and reached gameplay. One traversal sample showed about **18 game FPS** at 720p with the **Performance** preset and **50% internal render scale**. | Start with **Performance** and **50% internal render scale**. **Original** output resolution is another option to try. |

## Saves, backups, and updates

- **Saving and loading.** Use the game’s original menus to save to and load from the virtual PS2 memory card.
- **Export or restore a backup.** Open **Backups** in the launcher to export or import a ZIP containing your memory card, game settings, touch layout, and touch camera and rotation preferences. Importing a backup replaces matching files and settings.
- **Updating.** Install the new APK over your existing **Driver Preview** installation. An in-place update with the same Android package and signing key keeps your imported game and memory-card saves. Use **Backups** before uninstalling or switching editions.

## Known issues

- **Graphical glitches.** Some scenes may show flickering, incorrect lighting, or fog artifacts. Results can vary by device and graphics driver.
- **MediaTek devices are currently unsupported.** Compatibility and performance have yet to be verified on physical MediaTek hardware.
- **Screen rotation on AYN Thor.** Selecting the **180° landscape flip** left the tested Thor in standard landscape. Rotation remains experimental on that device.
- **Custom GPU drivers are experimental.** Turnip tests on Thor encountered crashes or GPU memory pressure. If a custom driver causes trouble, select **Use system driver** in the **GPU** tab and relaunch the game.

## Reporting issues

Open a GitHub issue and include your **device model**, **Android version**, **app version**, **graphics driver**, and **display settings**. For a graphics glitch or slowdown, mention the scene and what you were doing. A screenshot or short clip with the game FPS visible helps reproduce the issue.

## Credits

- **GhostScitSMT** for the Android Handheld Edition, launcher, touch controls, and graphics driver integration.
- **Team Ico and Sony Computer Entertainment** for the original *Shadow of the Colossus*.
- **HenryKun55 and the Celosia contributors** for the upstream recompilation and port work. [Celosia](https://github.com/HenryKun55/celosia)
- **ran-j and the PS2Recomp contributors** for the PS2 recompiler and runtime tools. [PS2Recomp](https://github.com/ran-j/PS2Recomp)
- **LightVelox** for related PC port research credited by Celosia. [sotc-vibe-pc](https://github.com/LightVelox/sotc-vibe-pc)
- **raylib, ANGLE, libadrenotools, and Mesa contributors** for graphics and driver-loading components.

This is an unofficial fan project. The original game and its assets belong to their respective rights holders. Players supply their own game disc image.
