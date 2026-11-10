Works on Linux, Steamdeck and Windows.
A small windows and appimage installer for local splitscreen couch co-op for PEAK. It adds a Split the screen
button under Play offline in PEAK's main menu, so players on one machine each get their own controller,
camera, and HUD. Each players expressions, clothing, and color are randomized every game.
<img width="1920" height="1080" alt="Screenshot_20261109_184901" src="https://github.com/user-attachments/assets/f6f6736d-fa9e-4655-92c8-aa101a8fd4f8" />


<img width="4000" height="3000" alt="20261109_190118" src="https://github.com/user-attachments/assets/3e9f8f54-1153-4839-b7e3-6423bed1a465" />



<img width="1920" height="1080" alt="Screenshot_20261109_192111" src="https://github.com/user-attachments/assets/1a3c28ec-d30a-4963-a965-0ed2affb5ad6" />
<img width="1920" height="1080" alt="Screenshot_20261109_192134" src="https://github.com/user-attachments/assets/64daf8f0-08e1-4c45-a68b-6397d55d5eee" />


 ⚠️ You must own PEAK on Steam.
 This installer does not include, download, or unlock the game. It only works on a legitimate copy of
 PEAK that you have bought on Steam and installed in your own Steam library. If you don't own PEAK on Steam,
 it has nothing to install into and will simply say it can't find the game. Please buy the game and support
 its developers. This project does not support or help with pirated copies.


 This is am unofficial fan mod, not affiliated with or endorsed by PEAK's developers or valve. There will be bugs and some u.i glitches in vertical splitscreen when things pop up. Not everything is ironed out yet but the core gameplay works perfectly fine. 

 Requirements

 PEAK, owned on Steam and installed (Steam app id 3527290). On the Steam Deck, Proton runs the Windows
 build of the game.
 The installer window needs a desktop session. so obviously if youre on steamdeck be sure to be in desktop mode for the initial installation. 
 

 Using it
 The window is keyboard/mouse and touch screen friendly.

1. Make sure PEAK is installed through Steam and closed.
2. Run the AppImage (chmod +x it first if needed). It looks for PEAK in your Steam libraries and asks whether
   to install the co-op files.
3. Click Install coop files, then Launch PEAK (or start the game from Steam yourself).
4. In PEAK's main menu, choose Split the screen.
5. chose a controller per player 
6. Have fun!
After a PEAK update, run the installer again.



 install / update the mod 
 uninstall / restore PEAK's original files and remove the mod 
 launch  make sure this build's files are installed, then start PEAK through Steam 
 selftest out.json  run the installer against a throwaway fake PEAK folder and write a pass/fail report 
 screenshot out.png  render the window and save a screenshot 
 writeicon out.png  write the app icon 

install, uninstall and launch print the result and exit with 0 on success, 1 on failure.

 What it changes

Everything stays inside PEAK's own folder, and nothing keeps running afterward — the mod loads inside the game.
There is no BepInEx or other mod loader.

1. Copies PeakSplitScreen.dll (the mod) and 0Harmony.dll the
   MITlicensed patching library the mod uses) into PEAK_Data/Managed/.
2. Adds PeakSplitScreen.dll (type 16, a game code file) to PEAK_Data/ScriptingAssemblies.json.
3. Adds a PeakSplitScreen.Entry.Init entry to PEAK_Data/RuntimeInitializeOnLoads.json, so Unity runs the
   mod's startup method when the game starts.


 Building from source

Needs Rust (cargo). The installer is a single file, src/main.rs, using [macroquad](https://macroquad.rs) for
the window.

sh
cargo build release           target/release/peaksplitscreen
cargo run release            run from the source tree; mod files come from build/mod/
./buildappimage.sh             PEAKSplitscreenx86_64.AppImage (downloads appimagetool if needed)


When run from the source tree, the installer finds the mod files in build/mod/; inside the AppImage it finds
them in usr/share/peaksplitscreen/.

selftest: 

sh 
./target/release/peaksplitscreen selftest /tmp/result.json


src/main.rs                      the installer: game detection, install/uninstall, window, CLI, selftest
Cargo.toml                       build settings
build/mod/                       the prebuilt mod files that get installed (PeakSplitScreen.dll, 0Harmony.dll)
packaging/                       AppRun, .desktop file, icon for the AppImage
buildappimage.sh                packs the AppImage



 ⚠️A.I assisted⚠️
