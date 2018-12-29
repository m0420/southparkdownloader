# SouthPark Downloader
[![Seasons](https://img.shields.io/badge/Seasons-22-brightgreen.svg)](https://github.com/bumbummen99/southparkdownloader)
[![Seasons](https://img.shields.io/badge/NetCore-2.2-green.svg)](https://github.com/bumbummen99/southparkdownloader)

A small C# application to download all episodes from [southpark.de](http://www.southpark.de/) using [ffmpeg](https://www.ffmpeg.org/) and [youtube-dl](https://rg3.github.io/youtube-dl/).
Feel free to kep the index up-to-date by creating a pull-request.

## Requirements
- .net core 2.2+

## Installation
# Windows

The software requires [Microsoft Visual C++ 2010 Redistributable Package (x86)](https://www.microsoft.com/en-US/download/details.aspx?id=5555) to be installed in order to function properly.
Simply unzip the latest release and run the included executable, the software will automatically download and install its dependencies (portable) including youtube-dl and ffmpeg.

# Linux & OSX

You need to install .net core 2.2, ffmpeg and youtube-dl as the software depends on them.
Please follow the official documentation on how to install .net core on Linux [here](https://dotnet.microsoft.com/download/linux-package-manager/ubuntu16-04/runtime-2.0.5).

```
sudo apt-get install ffmpeg youtube-dl
```

## Commands
Most of the time the ```download``` command will be enough as it will download the episode parts
and merge the resulting video files during process for you.

If you encounter any issues while downloading / merging an episode the programm should continue fine. You can
run the command ```download``` again to redownload incomplete episodes or ```process``` to merge unmerged parts.

If you don't encounter any bugs there is no need to update the software every time you use it, you should definitely if you are going for a full download.
In order to update the episode list / database simply use the command ```index update```. If the current index is broken or outdated (which i hope is not) you can fix 
the index file manually and re-index it with the command ```index```.

### download
Downloads all episodes in the episodes list. The command will download all parts and merge them accordingly, deleting unecessary files.

### process
Merges unmerged video parts. Use this command if the software encounters a problem during the download process.

### index
Reloads the index by reading the local index file.

### index update
Replaces the local index with an up-to-date version from this repository and reloads it.
