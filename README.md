# Deezer ogg preview conversion

A small script to play audio preview from deezer with html5 audio tag (for Firefox, opera or chrome).

[Read more about Deezer API](http://developers.deezer.com/api)

## Requirements

* ffmpeg
* php

### ffmpeg install (Debian)

    sudo apt-get install update
    sudo apt-get install ffmpeg
    
### Conversion 

     ffmpeg -i http://cdn-preview-a.deezer.com/stream/a4e149e52e2ffdc4f057661b40ba7ee3-1.mp3 -f ogg -strict experimental -acodec vorbis -ab 192k test.ogg

## How to 

* Get a deezer track id from [Deezer API](http://developers.deezer.com/api)

* Call the function getSample($track_id) (The function calls Deezer API to get the audio preview url and directly convert it into ogg format. 
The ogg file will be stored in a stream folder)

* getSample return the path of the ogg file. 