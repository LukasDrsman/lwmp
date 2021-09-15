# lwmp
A simple mp3 player written in POSIX shell

## Dependencies
 - `mpg123`

## Installation
Install with
```sh
git clone https://github.com/LukasDrsman/lwmp.git
cd lwmp
sudo ./install.sh
```
(Optional) Create a config file `lwmprc` in `$HOME/.config`, add the following entries and change them if needed
```sh
PREF="$HOME/music"

COL1="\u001b[31m"
COL2="\u001b[35m"
COL3="\u001b[34m"
```
 - `PREF` - music folder location prefix
 - `COL1`, `COL2`, `COL3` - color escape sequences for `lwmp_status`

## Usage
### Commands
| command | effect | args |
|---------|--------|------|
|`lwmp`   |play album | playlist file, volume percentile |
|`lwmp_stop`|stop lwmp | none |
|`lwmp_skip`|skip song | none |
|`lwmp_status`|print status | none |

### Playlist file
Given the file structure
```
$PREF
└── artist
    └── album
        ├── song1.mp3
        ├── song2.mp3
        ├── song3.mp3
        └── song4.mp3
```
a playlist, containing `song1` and `song2` by artist `artist` from album `album` would contain
```
artist/album/song1
artist/album/song2
```
