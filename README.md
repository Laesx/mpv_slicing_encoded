`slicing-copy.lua` is a Lua script forked from [Kagami/mpv_slicing](https://github.com/Kagami/mpv_slicing).
The script is for mpv to cut fragments of the video.

#### Usage

Make sure you have FFmpeg installed. Put `slicing_copy.lua` to `~/.config/mpv/scripts/` or `~/.mpv/scripts/` directory to autoload the script or load it manually with `--script=<path>`.

Press `c` first time to mark the start of the fragment. Press it again to mark the end of the fragment and write it to the disk. Press `C` to clear the fragment. Press `a` to toggle uncompressed audio capturing (default on).

You could find some logs in console (press `~` to open and `esc` to close by default), there might be something useful.

You could change key bindings and all parameters of the output video by editing your `input.conf` and `script-opts/slicing_copy.conf`, see [slicing_copy.lua](slicing_copy.lua) and [mpv reference](https://mpv.io/manual/master/#lua-scripting-on-update]]\)) for details.

#### Notice

Online videos are not supported.  

Output videos will be placed in `cutfragments` in mpv configuration directory by default instead of the home directory since [commit 7b3ef36](https://github.com/snylonue/mpv_slicing_copy/commit/7b3ef36fbe854f238e296a8b16af25bc281142c9).  
However, the script will not check if the directory is exist because it's not easy in lua. But you still could change the directory by editing script-opts/slicing_copy.conf or source code (option `target_dir`).

#### License

mpv_slicing_copy - Cut video fragments with mpv

Written in 2015 by Kagami Hiiragi <kagami@genshiken.org>

Modified in 2019 by Snylonue <snylonue@gmail.com>

To the extent possible under law, the author(s) have dedicated all copyright and related and neighboring rights to this software to the public domain worldwide. This software is distributed without any warranty.

You should have received a copy of the CC0 Public Domain Dedication along with this software. If not, see <http://creativecommons.org/publicdomain/zero/1.0/>.
