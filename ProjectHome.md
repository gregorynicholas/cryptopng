Reading or writing secret text from/to uncompressed raster image (PNG, GIF, ...). Every 3 bits are encoded to 3x3 pixelgrid. Central pixel keeps the information, each channel of RGB represents one bit. If at least one of a neighbouring pixels color channel is same as color channel of central pixel, it's a logical one(true), else logical zero(false).

The most beautiful thing is that you almost can't recognize, if image keeps some secret message. It looks like very similar to original.

With this [python](http://www.python.org) script you can send image from your vacation with some encoded text to your friend and nobody supposes anything strange.

### Script usage ###
Write these commands in Linux bash terminal:

**Write secret text to image**
```
cryptopng image <<< "secret message"
```

**Read text from image**
```
cryptopng image
```

**Print count of chars image can keep**
```
cryptopng --capacity image
```

**Show script usage**
```
cryptopng --help
```

### Feedback ###
Suggestions and bugs send to smejkalv\_AT\_gmail\_DOT\_com.

Thank you.