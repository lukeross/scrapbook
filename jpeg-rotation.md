# [Loseless JPEG rotation](https://leancrew.com/all-this/2009/04/derotating-jpegs-with-exiftool/)

[`exiftool`](https://exiftool.org/) can update the EXIF data to rotate images
without altering the image data (technically, the viewer rotates it according
to the EXIF). This avoids quality-loss associated with de- and re-compression.

## Do not rotate

```sh
exiftool -Orientation=1 -n filename.jpg
```

## Rotate 90 degrees clockwise

```sh
exiftool -Orientation=6 -n filename.jpg
```

## Rotate 90 degrees anticlockwise

```sh
exiftool -Orientation=8 -n filename.jpg
```

## Rotate 180 degrees

```sh
exiftool -Orientation=3 -n filename.jpg
```
