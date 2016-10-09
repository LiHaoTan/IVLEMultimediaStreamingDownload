1. Install FFmpeg. (See Below)
2. Run the Javascript code below and copy the printed FFmpeg command into command line.

#macOS
```bash
brew install ffmpeg
```

#Ubuntu
```bash
apt-get install ffmpeg
```

#Windows
Go to https://www.ffmpeg.org/ to download and install.

#Javascript
```javascript
var url = document.getElementById("ctl00_ctl00_ContentPlaceHolder1_ContentPlaceHolder1_hidFilePath").value;

var lastSlashIndex = url.lastIndexOf("/");
var extensionIndex = url.lastIndexOf(".mp4.m3u8");
var fileName = url.substr(lastSlashIndex + 1, extensionIndex - lastSlashIndex - 1);

//alternative regular expression just for fun /[^\/]+(?:\.mp4\.m3u8$)/

console.log("ffmpeg -i \"https://"
 + escape(url.substr(8))
 + "\" -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 " + fileName + ".mp4");

 "Sucess! Copy the above FFmpeg command"
```

#Example Output:
ffmpeg -i "https://vod.nus.edu.sg/hls-vod/ivle/users/13342cd6-97ce-4859-8185-5fe7b296ca56/NUS%20CFG_4_Happiness%20Seminar_20160908.mp4.m3u8" -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 file.mp4
