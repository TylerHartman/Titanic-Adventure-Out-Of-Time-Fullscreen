===============================================================================
Titanic: Adventure Out of Time — Final Fullscreen Builds
===============================================================================

Four variants are included. Use whichever presentation mode you prefer.


FULLSCREEN
----------

Titanic_Fullscreen.exe

Standard edge-to-edge fullscreen.

The original 512x384 output is scaled to the full display. Mouse coordinates
are remapped to the game's native coordinate space so hotspots remain correct.


4:3 FULLSCREEN
--------------

Titanic_4x3.exe

Aspect-correct fullscreen with centered pillarboxing on widescreen displays.

This is built directly from Titanic_Fullscreen.exe. The only differences are
the presentation rectangle and inverse mouse-coordinate mapping.


CINEMATIC FULLSCREEN
--------------------

Titanic_Cinematic_Fullscreen.exe

Uses the standard fullscreen presentation during gameplay.

When a 512x264 cinematic is active without the lower HUD/menu region, the movie
viewport is expanded to the full display. Normal 512x384 screens are left
unchanged.


IMMERSIVE FULLSCREEN
--------------------

Titanic_Immersive_Fullscreen.exe

Extends the cinematic build by using the 512x264 world viewport as the
fullscreen source during normal exploration, removing the lower HUD/menu from
the presentation.

The full 512x384 frame is restored automatically for states that need it,
including dialogue, Blackjack, and other full-interface/modal screens.

Right-click toggles immersive mode while the normal gameplay menu is available.
Cinematic expansion is retained from Titanic_Cinematic_Fullscreen.exe.


IMPLEMENTATION NOTES
--------------------

All four builds use the same final fullscreen patch base:

  - fullscreen compositor with corrected mouse/hotspot mapping
  - original 512x384 game coordinate space retained
  - Windows SetSysColors behavior neutralized to prevent system-color corruption
  - process affinity pinned to logical processor 0

The game itself still renders at its original dimensions. Scaling and cropping
are handled at presentation time rather than by altering scene geometry,
hotspot data, or game assets.


SHA-256
-------

Titanic_Fullscreen.exe
22dacbb46f99fc74375723d225670e19c1c8a8f2c884b089c74ad66e5a5616e4

Titanic_4x3.exe
daa514521b4ccb99f5a2df2bcdd43355d8c3f15d238b4dbec5b8bff2c9a40ec9

Titanic_Cinematic_Fullscreen.exe
1ebe37094b2a08b30ce7db07bb0f0a8197fea167804e1f958950de15e7f5a081

Titanic_Immersive_Fullscreen.exe
00511534d63f071c003b9c13ee03008d35d5969dd717e7f3abd91500534b842f
