# FFRec – FFmpeg Record

FFRec is a simple posix script to record audio and/or display easily using FFmpeg.
The usage is very simple:
* `$ ffrec --audio` or `$ ffrec -a` – record audio
* `$ ffrec --display` or `$ ffrec -d` – record display
* `$ ffrec --audio --display` or `$ffrec -ad` – record audio and display

## Dependencies
1. ffmpeg
1. xrandr

## (Un)Installation
### Universal
#### Installation
##### Latest Git Master (Bleeding Edge)
1. Git clone the repository.
* `$ git clone https://github.com/Amarakon55/ffrec`
2. Change working directory to ffrec.
* `$ cd ffrec`
3. Install FFRec using the Makefile
* `# make install`
#### Uninstallation
##### Latest Git Master (Bleeding Edge)
1. Change working directory to ffrec.
* `$ cd ffrec`
2. Uninstall FFRec using the Makefile
* `# make uninstall`
<!---
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
