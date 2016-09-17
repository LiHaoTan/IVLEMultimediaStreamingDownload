1. Install FFMpeg.
2. Run the Javascript code below and copy the code into command line. (without the outermost double quotes)

```javascript
"ffmpeg -i \"https://"
 + escape(document.getElementsByName("ctl00$ctl00$ContentPlaceHolder1$ContentPlaceHolder1$hidFilePath")[0].value.substr(8))
 + "\" -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 file.mp4";
```
