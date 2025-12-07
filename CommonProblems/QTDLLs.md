# QTDLLs:

## TLDR:
So you got something like:
```
21:17:42 (INFO) Using EasyAntiCheat runtime 
21:17:42 (INFO) Using BattlEye runtime 
fsync: up and running.
002c:err:wineboot:process_run_key Error running cmd L"C:\\windows\\system32\\winemenubuilder.exe -a -r" (126).
008c:err:ntoskrnl:ZwLoadDriver failed to create driver L"\\Registry\\Machine\\System\\CurrentControlSet\\Services\\winebth": c0000135

0024:err:module:import_dll Library Qt5WebEngineWidgets.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library Qt5WebSockets.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library uibase.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library archive.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library usvfs_x64.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library Qt5WebChannel.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library Qt5Widgets.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library Qt5Gui.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library Qt5Network.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library Qt5Core.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:import_dll Library liblz4.dll (which is needed by L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe") not found

0024:err:module:loader_init Importing dlls for L"Z:\\run\\user\\1000\\doc\\83f56bf4\\ModOrganizer.exe" failed, status c0000135
```

In most cases problem is in `flatseal`.
If you use it and know how to `fix` it - be free to do so and guide me on how to do it.

But for now:

## Possible Solution:
1. Delete `flatseal`.
2. Do [1.4](https://github.com/Red007Master/Red-s-Guide-on-Installing-G.A.M.M.A.-on-Linux?tab=readme-ov-file#1---bottles-source-usebottlescom) again.
3. Reboot.
4. Remove MO shortcut.
5. Add it (MO shortcut) again.

## Other possible causes:
1. Custom bottle(prefix) location.

If it didn't help refer to: https://github.com/Red007Master/Red-s-Guide-on-Installing-G.A.M.M.A.-on-Linux/issues/4
