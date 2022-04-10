# For Users

- On your Mac:

    - install iterm2_ext_display.app
    - copy ext_display_client.sh to ~/ext_display_client.sh
    - copy ext_display_server.shto ~/ext_display_server.sh
    - launch the app iterm2_ext_display

- On your iPad

    - install shelly
    - configurae in profile, in Command, set "source ~/Users/$User/.ext_display_client.sh"

# For Developer

## How it works

The apple script parts is edited in "Script Editor.app" and export to an
application so that this application could be luanched from applications folder

## What this server application does

It launched an iterm2 and inside it, it lauched a tmux session and run the
script with:

```
source ~/.ext_display_server.sh
```

So one could edit .ext_display_server.sh to run additional commands.
so far it rename the session name to "ext_display" and set additional options
of tmux so that the size of iterm2 window will not affect the windows size on
iPad

## What shelly on iPad should does

- ssh to the Mac
- run the command "source /Users/$USER/.ext_display_client.sh"
- the .ext_display_client will attach to the session "ext_display"

## TODO

- Add icon to application
- support multiple server tmux sessions
