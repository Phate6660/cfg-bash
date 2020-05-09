# cfg
A configuration manager written in bash.

## How it works
1. Configuration directory is created (`$HOME/.config/cfg`) if non-existent
2. If configuration (`$HOME/.config/cfg/cfg`) is non-existent, ask user to configure cfg
3. When adding a new config to manage, it is saved to the config dir under the name of the application, with the contents:
```
app=program name
type=type of config
file=/path/to/file
```
4. Listing tracked configs is as simple as `ls $HOME/.config/cfg` since all files are named after the respective programs

## Implemented / Planned
What is implemented:
- Adding configs to manage
- Viewing / Editing configs
- Backing up configs
- Files named "program name - type of config" (if applicable) to avoid collision of two configs from same program

What is planned:
- Removing configs (from either being managed or the filesystem)
- Version control(?) -- I wouldn't be too interested, but I'm sure others would be interested in this if I implemented it
