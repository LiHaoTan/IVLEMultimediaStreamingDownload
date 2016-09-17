1. Install FFMpeg. (See Below)
2. Run the Javascript code below and copy the code into command line. (without the outermost double quotes)

#macOS
```bash
brew install ffmpeg
```

#Ubuntu
```bash
apt-get install ffmpeg
```

```javascript
"ffmpeg -i \"https://"
 + escape(document.getElementsByName("ctl00$ctl00$ContentPlaceHolder1$ContentPlaceHolder1$hidFilePath")[0].value.substr(8))
 + "\" -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 file.mp4";
```
