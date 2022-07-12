FFRec – FFmpeg Record
================

## Contents

-   [Usage](#usage)
-   [Dependencies](#dependencies)
-   [Installation](#installation)
    -   [Universal](#universal)
    -   [Gentoo](#gentoo)
-   [Uninstallation](#uninstallation)
    -   [Universal](#universal-1)
    -   [Gentoo](#gentoo-1)
-   [Configuration](#configuration)
-   [Credit](#credit)

FFRec is a simple POSIX script to record audio and/or display easily
using FFmpeg. It is a simple alternative to OBS. It supports dmenu
selection. And it is easier to use than plain FFmpeg.

## Usage

``` sh
`# user` ffrec --audio # record audio
`# user` ffrec --display # record display
`# user` ffrec --audio --display # record audio and display
`# user` ffrec --webcam # record webcam
# With dmenu
`# user` ffrec --dmenu # choose what to record in a dmenu prompt
```

For more details, run `` `# user` ffrec --help ``.

## Dependencies

1.  FFmpeg
2.  Xrandr
3.  dmenu (menu selection)

## Installation

### Universal

``` sh
`# user` git clone https://github.com/amarakon/ffrec
`# user` cd ffrec
`# root` make install
```

### Gentoo

``` sh
`# root` eselect repository add amarlay git https://github.com/amarakon/amarlay
`# root` emerge --sync amarlay
`# root` emerge media-video/ffrec
```

## Uninstallation

### Universal

``` sh
`# user` cd ffrec
`# root` make uninstall
```

### Gentoo

``` sh
`# root` emerge -c media-video/ffrec
# Remove my overlay (optional)
`# root` eselect-repository remove -f amarlay
`# root` emerge --sync
```

## Configuration

You can change the default values of FFRec options via the configuration
file. The configuration file is located in the configuration directory,
so usually `~/.config/ffrec/ffrec.conf`. Here is an example
configuration:

``` sh
frame_rate=30
preset="ultrafast"
audio_encoder=mp3
video_extension=mp4
```

## Credit

Credit goes to
[u/two-bit-hack](https://www.reddit.com/user/two-bit-hack/) on
[Reddit](https://reddit.com) for helping me add options to this script.
