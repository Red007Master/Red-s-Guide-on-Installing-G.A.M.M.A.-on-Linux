# Wine 64/32 bit prefix issues
During bottles  setup, when trying to install windows dependencies on the bottles wine prefix via the terminal with the line:

`WINEPREFIX={your-prefix's-path} winetricks cmd d3dx9 dx8vb d3dcompiler_42 d3dcompiler_43 d3dcompiler_46 d3dcompiler_47 d3dx10_43 d3dx10 d3dx11_42 d3dx11_43 dxvk quartz`

There is a chance you may encounter errors like

`warning: wine cmd.exe /c echo '%AppData%' returned empty string, error message "wine: '/home/your_user/.var/app/com.usebottles.bottles/data/bottles/bottles/bottles_gamma_prefix_directory' is a 64-bit installation, it cannot be used with a 32-bit wineserver."`

And then the terminal hangs and does not let winetricks install the dependencies.

## *Possible fix*:
The new alternative terminal command could look like:

`WINE="{path-to-proton-downladed-by-bottles}GE-Proton(x-y}/files/bin/wine" WINEPREFIX={your-prefix's-path} winetricks cmd d3dx9 dx8vb d3dcompiler_42 d3dcompiler_43 d3dcompiler_46 d3dcompiler_47 d3dx10_43 d3dx10 d3dx11_42 d3dx11_43 dxvk quartz`

`{path-to-proton-downladed-by-bottles}GE-Proton(x-y}` can be easily found by exiting bottle, opening bottles preferences, in the "Runners" tab next to the ge-proton version that's already downloaded there is a folder icon which opens the location in the file browser.

**Note the location is appended with `/files/bin/wine`** to select the ge-protons wine prefix.
