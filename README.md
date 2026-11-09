# Shadow of the Colossus – Handheld Edition

An unofficial Android port of the original PlayStation 2 game, adapted for Android handhelds and phones by **ghostscitsmt**. Play with a physical controller or a customizable touch layout, choose original PlayStation or Switch-style prompts, and adjust the display for your device.

**Version 0.13.4 · current build**

The APK is currently in local testing. Public downloads are pending recovery of the Android engine source for this build.

## Features

- 4:3 and 16:9 widescreen modes, with original, 720p, and 1080p rendering options.
- A full-screen option that removes the bars and cinematic matte.
- Classic, Responsive, and Modern control presets, with button calibration, stick dead-zone adjustment, and camera sensitivity. The default camera directions follow your stick on both axes.
- Original PlayStation symbols or Switch-style button icons for in-game prompts and touch controls. The Switch-style face layout is **Y left, X top, A right, B bottom**.
- Multi-touch controls with two analog sticks, a D-pad, face and shoulder buttons, Start and Select, and stick clicks. Move and resize controls, change their opacity, or hide them during play.
- USA cheat presets with individual on/off toggles and an editor for supported custom codes.
- Optional Turnip driver ZIP import through the experimental **GPU** tab.

## Requirements

- A 64-bit ARM Android device running Android 9 or newer with OpenGL ES 3.0 support.
- Your own uncompressed USA PS2 disc image of *Shadow of the Colossus* (`SCUS-97472`) in `.iso` format. The game files are supplied by your disc image.
- About 6 GB of free storage for the initial import.

This build was checked on a device with 4 KB memory pages. The bundled ANGLE libraries use 4 KB alignment, so compatibility with 16 KB Android devices is unverified. [Android page-size documentation](https://developer.android.com/guide/practices/page-sizes)

## Download and install

1. When a public build is available, open this repository’s **Releases** tab and download the APK from the release assets.
2. Open the APK on your Android device. If Android prompts you, allow installs from the browser or file manager you used to open it, then finish the installation.
3. Open the app and go to the **Play** tab. The system graphics driver is selected on a fresh install.
4. Tap **Choose USA ISO** and select your `.iso` in Android’s file picker. If the file is inside a ZIP or 7z archive, extract it first.
5. Keep the app open while it copies and imports the disc. Once the launcher shows **Ready to play**, tap **Play**.

## Controls and menus

- **Controller** · Open **Controls** to choose a preset. If the physical face buttons are in the wrong positions, use **Calibrate buttons** and follow the on-screen prompts.
- **Button icons** · In **Controls**, turn **Switch button icons** on for Y/X/A/B or off for the original PlayStation symbols. The change takes effect the next time you press **Play**. The icon choice is independent of your control preset and saves.
- **Touch controls** · During gameplay, tap **Touch** and enable **Show touch controls**. Use the same panel to set opacity or hide the controls when playing with a controller.
- **Customize the layout** · Tap **Touch → Edit layout**. Drag a button or stick to move it. Select a control and use **−** or **+** to resize it. Tap **Save** to keep your changes, **Cancel** to discard them, or **Reset → Save** to restore the default layout.
- **Return to the launcher** · Tap **Menu** at the top center of the screen, or swipe left from the right edge, then choose **Return to launcher**. Save in-game before leaving.
- **Settings hub** · Double-tap **Select** to open the in-game settings hub. 

## Display settings

Open **Display** and start with **720p**. For widescreen, select **16:9 widescreen** in the launcher and set the game’s own aspect ratio to **16:9** in its Options menu. Enable **Fill the entire screen** to remove the bars and cinematic matte. On screens with a different aspect ratio, filling the screen can stretch the image. Display changes apply the next time you press **Play**.

## Cheats

Open **Play → Cheats & extras** to enable or disable individual USA presets or enter a supported custom code. Return to the launcher to change your selections and press **Play** to apply them. During gameplay, use **Menu → Enable selected cheats** to toggle the selected cheats together. Any effects already written to a game save, such as unlocked items, can persist after a cheat is switched off.

## Custom GPU drivers

The system driver is the default. Custom Turnip drivers are experimental. To try one, supply an Android-compatible ARM64 driver ZIP for your Qualcomm Adreno GPU.

1. In the launcher, open **GPU → Import driver ZIP** and pick your ZIP.
2. Select **Use imported driver**, go back, and press **Play**. Driver changes apply on the next game launch.
3. If you see flicker, incorrect fog or lighting, or crashes, select **Use system driver** and relaunch the game. **Last startup details** shows the latest custom-driver startup report.

Driver selection applies only to this app and works without root. It uses the same game data and save storage as the system driver within this installation.

## Updating and saves

Install updates over your existing app. When the update uses the same Android package and signing key, it keeps the imported game data and saves, so you can go straight to **Play**. Keep a backup of your saves before uninstalling or switching editions. Older Thor and touch-only builds may appear as separate apps and keep separate saves.

## Report a problem

Open an issue and include the app version, device and Android version, display settings, and whether you were using the system driver or a custom driver ZIP. For graphics issues, mention the scene and what triggers the problem, and attach a screenshot or short clip if you can. For input issues, include your control preset and whether you were using touch controls or a physical controller.

## Credits

- **ghostscitsmt** for the Android Handheld Edition, launcher, controls, and driver integration.
- **Team Ico and Sony Computer Entertainment** for the original *Shadow of the Colossus*.
- **HenryKun55 and Celosia contributors** for the upstream recompilation and port work. [Celosia](https://github.com/HenryKun55/celosia)
- **ran-j and PS2Recomp contributors** for the PlayStation 2 static recompiler and runtime tools. [PS2Recomp](https://github.com/ran-j/PS2Recomp)
- **LightVelox** for related PC port research acknowledged by Celosia. [sotc-vibe-pc](https://github.com/LightVelox/sotc-vibe-pc)
- **Ramon Santamaria and raylib contributors** for the graphics library. [raylib](https://github.com/raysan5/raylib)
- **sse2neon contributors** for the ARM NEON compatibility library. [sse2neon](https://github.com/DLTcollab/sse2neon)
- **ANGLE, bylaws, and Mesa contributors** for the graphics translation layer, Android driver-loading libraries, and Turnip Vulkan driver. [ANGLE](https://android.googlesource.com/platform/packages/modules/ANGLE/) · [libadrenotools](https://github.com/bylaws/libadrenotools) · [liblinkernsbypass](https://github.com/bylaws/liblinkernsbypass) · [Mesa Turnip](https://docs.mesa3d.org/drivers/freedreno.html#turnip)

## Project notices

This is an unofficial fan project. *Shadow of the Colossus* and its original game assets belong to their respective rights holders. Third-party components retain their respective licenses and notices.

The upstream Celosia project is licensed under GPL-3.0. [Celosia license](https://github.com/HenryKun55/celosia/blob/main/LICENSE)
