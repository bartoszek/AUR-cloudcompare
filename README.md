# AUR-cloudcompare

# current problems
- compile error with avcodec -> ffmpeg

# how to fix
## install ffmpeg4.4
```
sudo pacman -Rd --nodeps ffmpeg
sudo pacman -S ffmpeg4.4
```

## try to compile the package
```
git clone https://github.com/muellerbernd/AUR-cloudcompare.git
cd AUR-cloudcompare
makepkg
```

## follow errors, missing symbolic links
- in my case this was the following
```
cd /usr/lib
sudo ln -sfn libavutil.so.56 libavutil.so
sudo ln -sfn libavcodec.so.58 libavcodec.so
sudo ln -sfn libavformat.so.58 libavformat.so
sudo ln -sfn libswscale.so.5 libswscale.so
```

# tbb problems
- follow the compiler error and comment mentioned lines out
- or disable tbb in cmake command
