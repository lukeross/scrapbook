# [Simple DVD authoring on Linux](https://ogris.de/howtos/dvd-authoring.html)

1. Install

  - [dvdauthor](<http://dvdauthor.sourceforge.net/>)
  - [FFmpeg](<http://ffmpeg.org/>)
  - [MPlayer](<http://www.mplayerhq.hu/>)

2. Convert all video files to a DVD compatible format, eg.:

  ```console
  $ ffmpeg -i xmas2011.mpg -thread 8 -target pal-dvd xmas2011.vob
  ```

3. Create a config file for dvdauthor, eg. *dvd.xml*: 

  ```xml
<dvdauthor dest="/data/fjo/dvd/out">
    <vmgm>
      <menus>
        <video format="pal" />
        <pgc entry="title" />
      </menus>
    </vmgm>
    <titleset>
      <titles>
        <video format="pal" />
        <pgc>
          <vob file="xmas2011.vob" />
        </pgc>
      </titles>
    </titleset>
  </dvdauthor>
  ```

4. Launch dvdauthor:

  ```console
  $ dvdauthor -x dvd.xml
  ```

5. Check if everything went ok:

  ```console
  $ mplayer dvd://1//data/fjo/dvd/out
  ```

6. Insert a blank DVD

7. Burn that beast:

  ```console
  $ growisofs -Z /dev/dvd -dvd-compat -dvd-video -V Xmas2011 /data/fjo/dvd/out
  ```

8. Annoy your relatives with this masterpiece every time you see each other :-)
