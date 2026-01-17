# Bazzite
Main problem would be using `gamma-launcher`, to be more precise looks like libunrar is not available to be easily/natively installed and used.   
You have two options:
- 1 Use Distrobox and do GAMMA install from inside of it.
- 2 Sideload libunrar binary, more about it [here](https://github.com/Red007Master/Red-s-Guide-on-Installing-G.A.M.M.A.-on-Linux/issues/6).
- 3 Use it: `export UNRAR_LIB_PATH=/REPLACE/WITH/OWN/PATH/TO/libunrar.so`, then run gamma-launcher again.

##Wine related stuff:
You can use stuff wine and winetricks shipped with proton.
Example:
```
WINE="/var/home/$user/.var/app/com.usebottles.bottles/data/bottles/runners/ge-proton9-20/files/bin/wine" WINEPREFIX="/var/home/$user/.var/app/com.usebottles.bottles/data/bottles/bottles/stalker-gamma" winetricks cmd d3dx9 dx8vb d3dcompiler_42 d3dcompiler_43 d3dcompiler_46 d3dcompiler_47 d3dx10_43 d3dx10 d3dx11_42 d3dx11_43 dxvk quartz
```
Make sure to replaced/change paths so they correspond to your systems. 
