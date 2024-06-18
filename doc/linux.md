# Linux Notes

### Note, I have not checked if these specific fixes are still required or if there are any new fixes that are needed.

ResoniteModLoader works on Linux, but in addition to the [normal install steps](../README.md#installation) there are some extra steps you may need to take.

The log directory on Linux may be in `$HOME/Steam/steamapps/common/Resonite/Logs` or `$HOME/.local/share/Steam/steamapps/common/Resonite/Logs`

If your log contains the following or similar, you will need to set up a workaround for the issue.

```log
System.IO.DirectoryNotFoundException: Could not find a part of the path "/home/myusername/Steam/steamapps/common/Resonite/Resonite_Data\Managed/FrooxEngine.dll".
```

To set up the workaround, run the following commands in your terminal:

```bash
cd "$HOME/Steam/steamapps/common/Resonite"
ln -s Resonite_Data/Managed 'Resonite_Data\Managed'
```
