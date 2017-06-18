# Kalliope requirements for Mac OS X

## Homebrew

Kalliope can be installed via [homebrew](https://brew.sh/) with a custom formula:

```bash
brew install aleneum/formulas/kalliope
```

## Limitations

Some Kalliope modules are not available for OSX.

| Category | Module      |
|:--------:|:-----------:|
| TTS      | pico2wave   |
| Player   | pyalsaaudio |
| Player   | mplayer [1] |

MPlayer can be installed via homebrew though:

```bash
brew install mplayer
```

However, Kalliope expects the binary at `/usr/bin/mplayer` which differs from the standard 
installation of homebrew which is `/usr/local/bin/mplayer`. This can be solved with
a soft link:

```bash
sudo ln -s /usr/local/bin/player /usr/bin/mplayer
```

## OSX specific modules

Custom modules can be installed as described [here](../contributing.md).

| Category | Module      | URL                                              |
|:--------:|:-----------:|:-------------------------------------------------|
| TTS      | osxsay      | https://github.com/aleneum/kalliope-tts-osx.git  |

If you are using the English [starter configuration](https://github.com/kalliope-project/kalliope_starter_en.git)
change into the base directory and run:

```bash
kalliope install --git-url https://github.com/aleneum/kalliope-tts-osx.git
```

to install the `osxsay` Text-to-speech engine which fascilitates the native TTS of OSX.
