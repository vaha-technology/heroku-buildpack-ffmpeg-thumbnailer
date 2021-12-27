# heroku-buildpack-ffmpeg-thumbnailer

Fork of https://github.com/Maysora/heroku-buildpack-ffmpeg-thumbnailer all credit goes to the original maintainer, but since the code is published under a MIT License, we decided to fork it to prevent any supply channel security issues and due to the download of a static ffmpeg from johnvansickle.com failing randomly.

A Heroku buildpack for ffmpeg that always downloads the [version 2.0.8 binaries](https://github.com/vaha-technology/heroku-buildpack-ffmpeg-thumbnailer/releases/download/ffmpegthumbnailer-2.0.8/ffmpegthumbnailer_2.0.8.bin.tar.gz)

## Usage

Run the following from the heroku command line:

```
heroku buildpacks:add --index 1 https://github.com/vaha-technology/heroku-buildpack-ffmpeg-thumbnailer.git --app HEROKU_APP
```

```
Set HEROKU_APP to the heroku app you want to refer to
```

Note: This buildpack should be added before the main language buildpack (by using `--index 1`),
since the application process types are calculated from the last buildpack in the list if no
`Procfile` is specified.
