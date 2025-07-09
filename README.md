android-screen-record
===

- A command to take screen record for Android
- The movie file converts into GIF and MP4 files automatically at multiple playback speeds (1x, 2x, 3x)

# Sample

## Original mp4 file

[Original mp4 file](./sample/original.mp4)

## GIF

FPS 10/20/30

<img src="./sample/fps_10.gif" width="200" alt="fps10"> <img src="./sample/fps_20.gif" width="200" alt="fps20"> <img src="./sample/fps_30.gif" width="200" alt="fps30">

# Usage

Execute following command to begin screen recording

```
$ android-screen-record
```

Interrupt(Ctrl + C) when you want to finish recording.
The files are saved to a temporary directory (`$TMPDIR/android-screen-record/`) and automatically opened in Finder.

You can specify output format using `-f` option

```
$ android-screen-record -f mp4   # Generate MP4 files only
$ android-screen-record -f gif   # Generate GIF files only
$ android-screen-record          # Generate both GIF and MP4 files (default)
```

## Generated Files

The tool automatically generates files at multiple playback speeds for both GIF and MP4 formats:

### GIF Files (10, 20, 30 fps)
- `fps_10_1x.gif` - Normal speed (1x)
- `fps_10_2x.gif` - Double speed (2x)
- `fps_10_3x.gif` - Triple speed (3x)
- `fps_20_1x.gif`, `fps_20_2x.gif`, `fps_20_3x.gif`
- `fps_30_1x.gif`, `fps_30_2x.gif`, `fps_30_3x.gif`

### MP4 Files (30, 60 fps)
- `fps_30_1x.mp4` - Normal speed (1x)
- `fps_30_2x.mp4` - Double speed (2x)
- `fps_30_3x.mp4` - Triple speed (3x)
- `fps_60_1x.mp4`, `fps_60_2x.mp4`, `fps_60_3x.mp4`

### Original File
- `original.mp4` - The original recorded video from Android device

# Requirements

This command is available for only macOS. and also needs following commands.

- `adb`
  - Installed by android-platform-tools
- `ffmpeg`
- `peco`

# Install

```
$ brew tap tomorrowkey/self
$ brew install tomorrowkey/self/android-screen-record
```

# License

```
Copyright 2019 tomorrowkey

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
