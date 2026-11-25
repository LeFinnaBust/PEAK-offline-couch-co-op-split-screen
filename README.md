# This is a small installer for local split-screen couch co-op for PEAK
 This mod brings native offline splitscreen to PEAK.
It adds a "Split the screen" button under the "Play offline" button in PEAK's main menu, so 2-4 players on one machine each get their own controller, camera and HUD. Each extra players expressions, clothing, and color are randomized every game. Passports for each character coming soon. Random outfits for now are just a laugh.
<img width="1920" height="1080" alt="Screenshot_20261121_183256" src="https://github.com/user-attachments/assets/1082ce77-f107-4061-b3f4-8a06093adcc6" />
<img width="1920" height="1080" alt="Screenshot_20261121_183327" src="https://github.com/user-attachments/assets/d9421a94-5e8d-4cc7-a823-dff0f2b84403" />
2 Players can choose either 2 player horizontal or vertical splitscreen
<img width="1920" height="1080" alt="Screenshot_20261121_190132" src="https://github.com/user-attachments/assets/22100585-798c-424d-83e5-433f64e7e206" />
3 Players can choose either 3 vertical splitscreens or player 1 horizontal screen while players 2 and 3 have 3 small squares below.
<img width="1920" height="1080" alt="Screenshot_20261121_183002" src="https://github.com/user-attachments/assets/da93cbb0-596c-4a18-911f-df92fe1790e3" />
  
<img width="1920" height="1080" alt="Screenshot_20261121_190113" src="https://github.com/user-attachments/assets/e7391e20-ee19-4a1d-8e13-bf34918512f8" />

<img width="1920" height="1080" alt="Screenshot_20261109_184901" src="https://github.com/user-attachments/assets/f6f6736d-fa9e-4655-92c8-aa101a8fd4f8" />


<img width="4000" height="3000" alt="20261109_190118" src="https://github.com/user-attachments/assets/3e9f8f54-1153-4839-b7e3-6423bed1a465" />






 ⚠️ You must own PEAK on Steam.
 This installer does not include, download, or unlock the game. It only works on a legitimate copy of
 PEAK that you have bought on Steam and installed in your own Steam library. If you don't own PEAK on Steam,
 it has nothing to install into and will simply say it can't find the game. Please buy the game and support
 its developers. This project does not support or help with pirated copies.


⚠️ This is an unofficial fan mod, not affiliated with or endorsed by PEAK's developers or valve. There will be bugs and some U.I glitches in vertical splitscreen when things pop up. Fog for extra players pov is still being worked on. All testing was done on a steamdeck. Please let me know your experience on windows.

 # Requirements

 PEAK, owned on Steam and installed (Steam app id 3527290). On the Steam Deck, Proton runs the Windows
 build of the game.
 The installer window needs a desktop session. so obviously if youre on steamdeck be sure to be in desktop mode for the initial installation. 
 

 # Using it
 The window is keyboard/mouse and touch screen friendly.

1. Make sure PEAK is installed through Steam and closed.
2. Run the AppImage (chmod +x it first if needed). It looks for PEAK in your Steam libraries and asks whether
   to install the co-op files. Same for windows but the .exe
3. Click Install coop files, then Launch PEAK (or start the game from Steam yourself).
4. In PEAK's main menu, choose Split the screen.
5. Choose a controller per player 
6. Have fun!


 What it changes

Everything stays inside PEAK's own folder, and nothing keeps running afterward — the mod loads inside the game.
There is no BepInEx or other mod loader.

1. Copies PeakSplitScreen.dll (the mod) and 0Harmony.dll the
   MITlicensed patching library the mod uses) into PEAK_Data/Managed/.
2. Adds PeakSplitScreen.dll (type 16, a game code file) to PEAK_Data/ScriptingAssemblies.json.
3. Adds a PeakSplitScreen.Entry.Init entry to PEAK_Data/RuntimeInitializeOnLoads.json, so Unity runs the
   mod's startup method when the game starts.


 ⚠️A.I assisted⚠️
