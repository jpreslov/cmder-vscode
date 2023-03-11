# Add Cmder to Windows

 _Note: This is to save myself time, but if you're reading this and know of a better way to do this, make a PR_

- `%CMDER_PATH%` will need to be defined on your machine (as a system variable), or replaced with the root Cmder folder path manually.
- Copy + paste the following into your VSCode `settings.json` file:
```json
"terminal.integrated.profiles.windows": {
    "Cmder": {
        "path": "C:\\WINDOWS\\System32\\cmd.exe",
        "args": [
            "/k",
            "%CMDER_PATH%\\vendor\\bin\\vscode_init.cmd"
        ]
    }
},
"terminal.integrated.defaultProfile.windows": "Cmder"
```
