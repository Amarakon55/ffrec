# FFRec – FFmpeg Record

FFRec is a simple posix script to record audio and/or display easily using FFmpeg.
The usage is very simple:
* `$ ffrec --audio` or `$ ffrec -a` – record audio
* `$ ffrec --display` or `$ ffrec -d` – record display
* `$ ffrec --audio --display` or `$ ffrec -ad` – record audio and display
* `$ ffrec --webcam` or `$ ffrec -w` – record webcam

With Dmenu:
* `$ ffrec --dmenu` or `$ ffrec -D` – choose what to record in a Dmenu prompt

## Dependencies
### Mandatory
1. ffmpeg
1. xrandr
### Optional
1. dmenu

## (Un)Installation
### Universal
#### Installation
##### Latest Git Master (Bleeding Edge)
1. Git clone the repository.
* `$ git clone https://github.com/Amarakon55/ffrec`
2. Change working directory to *ffrec*.
* `$ cd ffrec`
3. Install FFRec using the Makefile
* `# make install`
#### Uninstallation
##### Latest Git Master (Bleeding Edge)
1. Change working directory to *ffrec*.
* `$ cd ffrec`
2. Uninstall FFRec using the Makefile
* `# make uninstall`

### Gentoo
#### Installation
##### Latest Git Master (Bleeding Edge)
1. Add my personal [Gentoo overlay](https://github.com/Amarakon55/amarlay) using [eselect-repository](https://packages.gentoo.org/packages/app-eselect/eselect-repository)
* `# eselect repository add amarlay git https://github.com/Amarakon55/amarlay`
2. Sync my personal [Gentoo overlay](https://github.com/Amarakon55/amarlay) using `emerge`
* `# emerge --sync amarlay`
3. Emerge the FFRec package
* `# emerge media-video/ffrec` or `# emerge ffrec`
#### Uninstallation
##### Latest Git Master (Bleeding Edge)
1. Unmerge the FFRec package
* `# emerge -c media-video/ffrec` or `# emerge -c ffrec`
2. (Optional) Remove my overlay
* `# eselect-repository remove -f amarlay`
3. (Optional) Sync using `emerge`
* `# emerge --sync`

## Configuration

FFRec is configured by environmental variables.
You can set these options in your `~/.bashrc` or any other file that your default shell sources:

```sh
FFMPEG_DISPLAY_EXT="mkv" # The default file extension for display and webcam recording
FFMPEG_AUDIO_EXT="flac" # The default file extension for audio recording
FFMPEG_OPTS="-c:v libx264 -r 60 -c:a $FFMPEG_AUDIO_EXT -preset ultrafast" # The default options to pass to FFmpeg
```

## Credit

Credit goes to [u/two-bit-hack](https://www.reddit.com/user/two-bit-hack/) on [Reddit](https://reddit.com) for helping me add options to this script.
