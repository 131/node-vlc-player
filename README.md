# VLC player
Simply start vlc.exe (included in the module) process 

## API

```js
const child = require('vlc-player')( ['path/to/video.mp4'] );

// vlc is started
// child is a dummy nodejs process

setTimeout(function(){
  child.kill();
}, 1000);
```

## NB

The indent of this module is mostly to provide binaries for windows, linux equivalent (that we explicitly require at the application level)  is a "dummy" : 
```js
'use strict';

const spawn   = require('child_process').spawn;
module.exports = function(/* args, options */) {
  return spawn.bind(null, 'vlc').apply(null, arguments);
}
```



# TODO
* Nothing special (very dummy module)

# Credits
* [131](mailto:131.js@cloudyks.org)
* [VLC](http://videolan.org)


# Keywords / shout box
vlc, vlc-win32, vlc-binaries, mp4, ffmpeg, "Let's have a beer and talk in Paris"




