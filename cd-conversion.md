# Converting CDs to local

## Extract to WAV

```
cd-paranoia -B -X 
```

## Encode them to AAC

```
ls *.wav | perl -nle 's/.wav$//; system("aac-enc", "-v", "5", "-a", "1", "$_.wav", "$_.m4a");'
```

## Fix up metadata

```
for i in t*.m4a; do ffmpeg -i $i -codec copy fixed-$i.m4a; done
```

## Cleanup

```
rm t*.wav t*.m4a
```
