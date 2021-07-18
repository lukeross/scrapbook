# [Loseless JPEG rotation](https://leancrew.com/all-this/2009/04/derotating-jpegs-with-exiftool/)

[`exiftool`](https://exiftool.org/) can update the EXIF data to rotate images
without altering the image data (technically, the viewer rotates it according
to the EXIF). This avoids quality-loss associated with de- and re-compression.

## Do not rotate

```
exiftool -Orientation -n=1 filename.jpg
```

## Rotate 90 degrees clockwise

```
exiftool -Orientation -n=6 filename.jpg
```

## Rotate 90 degrees anticlockwise

```
exiftool -Orientation -n=8 filename.jpg
```

## Rotate 180 degrees

```
exiftool -Orientation -n=3 filename.jpg
```
