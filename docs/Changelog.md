# Changelog

## version 20.12 :mask:

**:tada: Celebrating audioMotion's 2nd Anniversary! :confetti_ball:**

### New features:

+ :fire: Revamped user interface with a cool new look! :sunglasses:
+ Stereo (dual channel) analyzer option :headphones: :notes: :musical_note:
+ :mega: Built-in volume control

### Changed / improved:

+ Song info may now be displayed continuously (no fade-out), and also at the **end of the song**; display times are now customizable in the Config panel;
+ The display of album covers in song info is now optional;
+ Options to upload a local file and to load a song from an URL are now always available, not only in local file mode;
+ Hold the previous/next player buttons (or left/right arrow keys) to rewind/fast-foward the current song;
+ Frequency and level scales are now toggled via independent **SCALE X** and **SCALE Y** switches;
+ The size of scale labels on both axes is now scaled relatively to the canvas height;
+ Added timestamp to console messages and a button to clear the console;
+ Added a keyboard shortcut (**C**) for toggling **Radial** visualization;
+ **Shortcut changes:**
  + **Up** and **down arrow** keys are now used to control the **volume** - for gradient selection use **G** or **Shift+G**;
  + **J** and **K** keys still work as alternate shortcuts to previous/next song, but are no longer documented and may be reassigned in the future;
  + Clicks on canvas now display song information (same behavior as the **D** key);
+ Updated documentation website.

### Fixed:

+ Clicks on switches not being properly detected sometimes;
+ Random mode not working when audio source was set to microphone;
+ An unexpected error message when deleting the last song from the queue.


## version 20.9 :mask:

This is a minor update to address two bugs:

+ A day-one design flaw which connected the microphone output to the speakers, generating feedback loops;
+ An unexpected error message when trying to load a playlist with an empty value in the playlist selection.


## version 20.8 :mask:

### Added:

+ New [Radial visualization](docs/README.md#radial) for all modes;
+ Option to display [level (dB) scale](docs/README.md#switches) on vertical axis;
+ New [**Demo** preset](docs/README.md#preset).

### Changed:

+ Improved the background image [**Pulse**](docs/README.md#image-fit) effect to look more synced regardless of music style;
+ Any image located in the song's folder can now be used as album cover when a picture is not found in the song metadata (see the [documentation](docs/README.md#background) for filename precedence).

### Fixed:

+ Audio files with uppercase extensions not recognized when audioMotion was running on a standard web server.


## version 20.6 :mask:

### Added:

+ **Album cover image** retrieved from the song metadata or from a file named *cover* or *folder* (.jpg|png|gif|bmp) inside each folder
is now shown in the file explorer background, the on-screen song information and, optionally, in the analyzer background;

+ New [Background](docs/README.md#background), [Image Fit](docs/README.md#image-fit) and [Image Dim](docs/README.md#image-dim) settings.

### Changed:

+ Slightly increased the opacity of the image reflection when Reflex is On.

### Removed:

+ The **NO BG** switch has been replaced by the new Background setting.

### Fixed:

+ Linux binary built with [latest pkg version](https://github.com/zeit/pkg/pull/751#issuecomment-626363292) can now open the browser automatically;
+ A typo that could cause "Unexpected null" errors on some browsers.


## version 20.4 :mask:

### Added:

+ New **Line graph** visualization mode, with customizable line width and fill opacity;
+ New **Reflex** effect;
+ New **Config panel** where you can:
  + Enable/disable visualization modes and gradients;
  + Select options affected by random mode;
  + Customize sensitivity presets (low, normal and high);
+ Customizable spacing between bars in octave bands modes;
+ Visualization mode can now be randomized on a time interval.

### Changed:

+ The **Area fill** mode has been renamed to **Area graph**;
+ The default spacing between bars in octave bands modes has been increased a bit - set the **Bar spacing** option to **Legacy** for the old look;
+ Slightly improved vertical usage of canvas when the LED effect is active (removed the black line at the bottom of the screen);
+ UI improvements.

### Fixed:

+ Track change sometimes not triggering random mode / auto gradient;
+ Case-insensitive sorting of directory listing when using a standard web server.


## version 19.12

:tada: Celebrating audioMotion's first anniversary! :confetti_ball:

### Added:

+ New **Area fill** visualization mode, which uses the same full-frequency data of the *discrete frequencies* mode, but displays a bright, colorful filled shape;
+ New luminance bars effect (**LUMI** switch) for octave bands modes, which always display full-height bars and vary their luminance instead, according to each band amplitude;
+ New option to select a random visualization mode on every track change (**RAND** switch); it will also select a random gradient, if the AUTO switch is active - great for parties!

### Changed:

+ Improved the look of bars at lower frequencies, especially for 1/12th and 1/24th octave bands modes;
+ Minor tweak to the **Rainbow** gradient to make cyan and blue shades a little more balanced;
+ Auto gradient and the new random mode now trigger on initial playback and previous track skip as well, not only on next track skip;
+ Shortcut keys changes:
  + Shuffle shortcut changed to **"E"** key;
  + **"U"** key reassigned to toggle the new luminance bars effect;
  + **"A"** key now also toggles random visualization mode in combination with auto gradient (three stages);
+ Added shortcut key hints to the player controls;
+ Improved display of feedback messages for keyboard controls;
+ Updated npm packages.

### Fixed:

+ Addressed an error on server startup when running the executable file on Linux systems (related to [an issue with pkg](https://github.com/zeit/pkg/issues/731)).


## version 19.10

:sunglasses: audioMotion's graphic spectrum analyzer is now available as a [standalone project](https://github.com/hvianna/audioMotion-analyzer) and a zero-dependency [npm package](https://www.npmjs.com/package/audiomotion-analyzer) you can use in your own JavaScript projects! :tada:

### Added:

+ 1/4th and 1/8th octave bands visualization modes;
+ Load files from remote URLs and manage playlists when running audioMotion in file mode (no server);

### Changed:

+ Double-clicking a playlist in the file explorer now correctly starts playing it, if player is idle;
+ Player automatically skips to next track on playback errors, e.g. file not found or format not supported;
+ Number of songs added to the playlist is now shown in a notification, instead of logged to the console;
+ Improved metadata fetching for streams and time display for longer audio files;
+ Improved error handling on file server;
+ Slightly improved gapless playback;
+ Updated npm packages.


## version 19.7

### Added:

+ :fire: File explorer for easy navigation through your music files and folders;
+ Custom file server written in node.js with portable binaries available for Windows, Linux and macOS - no setup required; :tada:
+ Add, reorder and remove songs from the play queue, with drag-and-drop support;
+ Song info now shows actual metadata read from music files;
+ Save custom playlists to your browser's local storage;
+ Option to show the current frame rate;
+ New gradient: **Cool**;

### Changed:

+ :sunglasses: Major user interface overhaul - added tabbed panels for settings, file explorer / playlists, and console;
+ The analyzer canvas now properly adjusts to window size, without looking stretched;
+ Improved analyzer sensitivity customization - user can now set minimum and maximum dB values, or choose from three presets via [N] key;
+ The *previous* player button now skips to the beginning of the current song, press again within 2 seconds to skip to the previous track;
+ Shuffle button now immediatelly starts playing the shuffled playlist;
+ Frequency scale bar is now semi-transparent;
+ Increased frequency scale font size while in fullscreen;
+ `playlists.cfg` file is no longer required, but still supported as a legacy feature;

### Removed:

+ *SENS* switch (toggle high sensitivity);
+ Demo playlists and music files.


## version 19.5

### Added:

+ :sunglasses: New optional vintage LED effect for the octave bands modes;
+ New gradients: **Apple ][** and **Orient**;
+ Two configuration options to improve performance:
  + **FLAT** replaces shadow for outline on text displayed on canvas;
  + **LO-RES** reduces canvas resolution to improve rendering speed (especially useful for 4K+ displays);
+ Current visualization mode, auto gradient status and repeat status added to the on-screen information;
+ Switch status is now shown on screen when changed via keyboard shortcode;
+ New preset to restore all configuration defaults;
+ More keyboard shortcuts.

### Changed:

+ Changed some keyboard shortcuts:
  + [I] now toggles the display of song information on track change;
  + [M] now selects the next visualization mode ([V] still works as a convenience to early users, but it may be assigned a new function in the future);
  + alternate keys for gradient selection changed to [G] and [Shift + G];
+ On-screen information is now displayed in two stages - press [D] once for song info, press it again for settings info;
+ Increased font size of on-screen information;
+ Restored option of shadowed text for on-screen information (turn off the *FLAT* switch);
+ *CYCLE* switch renamed to *AUTO*;
+ *DARK* switch renamed to *NO BG*.

### Fixed:

+ Preloaded songs not being correctly updated when modifying the playlist during playback;
+ Incorrect song information displayed when playlist was cleared or when playing local file.


## version 19.3

### Added:

+ New octave bands visualization modes (from full-octave up to 1/24th-octave) based on the equal tempered scale;
+ Improved playback of gapless tracks by using dual audio elements.

### Changed:

+ Removed the linear frequency scale option, in favor of the octave bands modes;
+ Improved visualization accuracy for higher frequencies on discrete mode (the old "logarithmic" mode);
+ The *DISPLAY* switch has been renamed to *INFO* and grouped with the other visualization switches;
+ Changed the X-axis labels for the standard octave bands center frequencies;
+ Replaced shadow for outline on text displayed on canvas, to improve performance on some graphic cards;
+ Updated the JS spec to ES6 in the readme, since I use promises, which are not natively available in ES5.


## version 19.1

### Added:

+ :sunglasses: New gradients;
+ Configuration presets;
+ Keyboard shortcuts (especially useful while on fullscreen mode);
+ Option to cycle through gradients on each track change;
+ On-screen display of song information via keyboard shortcut and, optionally, on each track change;
+ Support for the [#EXTINF directive](https://en.wikipedia.org/wiki/M3U#Extended_M3U) in playlists.

### Changed:

+ User preferences are now stored in local storage for browsers that implement it, instead of cookies;
+ Refactored some ES6-specific code to increase browser compatibility (especially on smart TVs);
+ Minor redesign of the UI and improved layout on smaller screens;
+ Renamed some of the gradients and ordered them alphabetically in the list.

### Fixed:

+ A bug where shuffling the playlist wouldn't properly load the first song;
+ Error when trying to load a song with a **#** character in its filename.


## version 18.12

### Added:

+ You can now load a song from your PC;
+ Clicking on canvas now toggles scale on/off.

### Changed:

+ Improved selection of audio source;
+ Improved layout on smaller screens;
+ General improvements in the UI;
+ New icons;
+ Some code clean-up and optimizations.

### Fixed:

+ *Should* **really** work on Safari now (including macOS).


## version 18.11

First official release.