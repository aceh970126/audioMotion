Changelog
=========

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