Batch-convert PNG to lossy JPG:

```
ls *.png | while read FILE; do convert $FILE -quality 40 ${FILE%.png}.jpg; done
```

Batch-convert JPG to Base64:

```
ls *.jpg | while read FILE; do base64 -w 0 "$FILE" > "${FILE}.b64.txt"; done
```

Batch-convert WAV to MP3:

```
ls *.wav | while read FILE; do echo "ffmpeg -i $FILE -ac 1 -b:a 96k ${FILE%.wav}.mp3"; done
```

Batch-convert MP3 to Base64:

```
ls *.mp3 | while read FILE; do base64 -w 0 "$FILE" > "${FILE}.b64.txt"; done
```
