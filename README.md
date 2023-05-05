# HLM2-Wad-Extract

This tool extracts binary asset data (including the soundtrack in OGG format) packaged with the game [Hotline Miami 2:
Wrong Humber](https://en.wikipedia.org/wiki/Hotline_Miami_2:_Wrong_Number).

## 1ma fork

This fork of the project fixes the script as per the instructions of this issue in the original repository: https://github.com/FooSoft/hlm2-wad-extract/issues/1

At some point the WAD format in the game was updated (documented [here](https://github.com/TcT2k/HLMWadExplorer/issues/4)).

The fix in this fork only does the bare minimum to parse the current version of `hlm2_music_desktop.wad` (as of 2023-05-05) correctly again.

## Usage

Execute `extract.py` script with the `-h` option for a description of available options ([Python
2.7](https://www.python.org/download/releases/2.7/) is required).

```
usage: parse.py [-h] [--pattern PATTERN] [--output DIRECTORY]
                filename [filename ...]

Extract assets from Hotline Miami 2 WAD files

positional arguments:
  filename            WAD files to extract

optional arguments:
  -h, --help          show this help message and exit
  --pattern PATTERN   asset file filter pattern (ex: *.ogg)
  --output DIRECTORY  output directory for asset files
```

For example, in order to extract the game's music files only, you could execute the following command:

```
$ ./parse.py --pattern "*.ogg" hlm2_data_desktop.wad
```

The relevant WAD files can be found in the `~/.steam/steam/steamapps/common/Hotline Miami 2` directory on Linux.
