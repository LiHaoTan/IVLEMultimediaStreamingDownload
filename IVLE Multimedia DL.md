1. Install FFmpeg. (See Below)
2. Run the Javascript code below (can be saved to snippets) and the FFmpeg command will be copied to your clipboard.

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

 copy("ffmpeg -i \"https://"
 + escape(url.substr(8))
 + "\" -bsf:a aac_adtstoasc -vcodec copy -c copy -crf 50 \"" + fileName + ".mp4\"");

 "Success! The FFmpeg command is now copied to your clipboard."
```

#Example Output:
Sucess! The FFmpeg command is now copied to your clipboard.
