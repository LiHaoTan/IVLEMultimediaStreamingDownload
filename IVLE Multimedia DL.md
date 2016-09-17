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

#Javascript
```javascript
"ffmpeg -i \"https://"
 + escape(document.getElementsByName("ctl00$ctl00$ContentPlaceHolder1$ContentPlaceHolder1$hidFilePath")[0].value.substr(8))
 + "\" -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 file.mp4";
```

#Example Output:
ffmpeg -i "https://vod.nus.edu.sg/hls-vod/ivle/users/13342cd6-97ce-4859-8185-5fe7b296ca56/NUS%20CFG_4_Happiness%20Seminar_20160908.mp4.m3u8" -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 file.mp4
