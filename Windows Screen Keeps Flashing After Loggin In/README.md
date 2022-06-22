# The issue
If you face the same issue below, then this thread is right for you:
- Windows screen keeps flashing after logging in.
- The taskbar is not loaded
- Start menu doesn't show up

# The solution
If you could open up like task manager, windows explorer or CMD, you might want to follow this steps:
1. Open up runner by pressing `Win + R`
2. Type `powershell` to fire up powershell
3. Before executing runner, you have to open powershell via administrator, just press `Ctrl + Shift + Enter`
4. Windows will ask you to open via administrator, just click Yes
5. Type the command below and press enter. This command will fix the issue you're facings,
```
Get-AppXPackage -AllUsers | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
```
6. Wait until the process is finish

# Refence:
You may want to find whole solution on this Microsoft Community [thread](https://answers.microsoft.com/en-us/windows/forum/all/microsoft-10-screen-keeps-flashing-after-login/0ecfb292-459d-4ff3-97e4-6ffe5568d6de)
