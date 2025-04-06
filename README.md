![Screenshot](https://12388101.xyz/fls/image.jpg)

# YouTube Shorts Video Downloader and Converter
Download and convert YouTube Shorts instantly! Supports MP4, WEBM, and various resolutions. Fast, simple, and versatile! 

The ⚡ YouTube Shorts Downloader enables seamless downloading of YouTube Shorts in MP4 or WEBM formats with various resolutions ranging from 144p to 1080p. This API provides a fast and reliable solution for accessing Shorts in your preferred format and quality.

[Try the API now and get instant results](https://api999.short.gy/j0OhRm)

### Features:

- **Multiple Formats:** Download Shorts in MP4 or WEBM formats for compatibility with various devices and platforms.
- **Custom Resolutions:** Choose from a wide range of resolutions, including 144p, 360p, 720p, and up to 1080p, for optimal viewing quality.
- **Fast and Reliable:** Enjoy quick processing and stable downloads 24/7
- **Ease of Integration**: Simple endpoints and clear documentation for quick implementation.

### Use Cases:
- Build a personal content downloader.
- Integrate YouTube Shorts videos to your app.
- Convert Shorts into different formats for professional editing or presentation.

### Supported Formats:
- **Video**: MP4, WEBM
- **Resultion**: 144p, 240p, 360p, 480p, 720p, 1080p

How to use? Easy!
-----------
The request returns a ready MP4 or WEBM file immediately. You just need to save the response to the request as a file.

Example Shell
```
curl -X GET "'https://youtube-shorts-video-downloader-and-converter.p.rapidapi.com/download-short-webm/86wbvJofPqU?quality=480p'" \
-H "x-rapidapi-host: youtube-shorts-video-downloader-and-converter.p.rapidapi.com" \
-H "x-rapidapi-key: *your_rapid_key*" \
-o video.webm 
```

#### What is **videoId**?

The videoId is the unique identifier for a YouTube video.

For example, if the Shorts URL is:
https://www.youtube.com/shorts/86wbvJofPqU

Then the **videoId** is the part of the URL after the last slash:
**86wbvJofPqU**.

Routes
-----------
### `/download-short-webm/{videoId}?quality={quality}`
The API returns the best available video quality in WEBM format. Quality parameter can be 144p, 240p, 360p, 480p, 720p, 1080p. By default 720p.

PHP Example
```
$ch = curl_init("https://youtube-shorts-video-downloader-and-converter.p.rapidapi.com/download-short-webm/86wbvJofPqU?quality=480p");
curl_setopt_array($ch, [
    CURLOPT_RETURNTRANSFER =&gt; true,
    CURLOPT_HTTPHEADER =&gt; [
        "x-rapidapi-host: youtube-shorts-video-downloader-and-converter.p.rapidapi.com",
        "x-rapidapi-key: *your_rapid_key*"
    ]
]);

$response = curl_exec($ch);
curl_close($ch);
file_put_contents("video.webm", $response);
```

JS Example
```
const fetch = require('node-fetch');
const fs = require('fs');

const apiUrl = 'https://youtube-shorts-video-downloader-and-converter.p.rapidapi.com/download-short-webm/86wbvJofPqU?quality=480p';
const headers = {
  'x-rapidapi-host': 'youtube-shorts-video-downloader-and-converter.p.rapidapi.com',
  'x-rapidapi-key': 'your_rapid_key'
};

fetch(apiUrl, { headers })
  .then(res =&gt; res.buffer())
  .then(data =&gt; fs.writeFileSync('video.webm', data))
  .catch(console.error);
```

### `/download-short-mp4/{videoId}?quality={quality}`
The API returns the best available video quality in MP4 format. Quality parameter can be 144p, 240p, 360p, 480p, 720p, 1080p. By default 720p.

PHP Example
```
$ch = curl_init("https://youtube-shorts-video-downloader-and-converter.p.rapidapi.com/download-short-mp4/86wbvJofPqU?quality=480p");
curl_setopt_array($ch, [
    CURLOPT_RETURNTRANSFER =&gt; true,
    CURLOPT_HTTPHEADER =&gt; [
        "x-rapidapi-host: youtube-shorts-video-downloader-and-converter.p.rapidapi.com",
        "x-rapidapi-key: *your_rapid_key*"
    ]
]);

$response = curl_exec($ch);
curl_close($ch);
file_put_contents("video.mp4", $response);
```

JS Example
```
const fetch = require('node-fetch');
const fs = require('fs');

const apiUrl = 'https://youtube-shorts-video-downloader-and-converter.p.rapidapi.com/download-short-mp4/86wbvJofPqU?quality=480p';
const headers = {
  'x-rapidapi-host': 'youtube-shorts-video-downloader-and-converter.p.rapidapi.com',
  'x-rapidapi-key': 'your_rapid_key'
};

fetch(apiUrl, { headers })
  .then(res =&gt; res.buffer())
  .then(data =&gt; fs.writeFileSync('video.mp4', data))
  .catch(console.error);
```

### **Get Video Info - `/get-video-info/{videoId}`**

**title**

Description: The title of the video.

*Example value: "How to create an NFT collection | Thirdweb".*

**description**

Description: The video description, including text information and links.

*Example value: "In this video I show you how to create an NFT collection using Thirdweb. You'll learn how to use Thirdweb's no-code web app to create an ERC-721 smart contract for your NFT...".*

**author**

Description: The author of the video.
*Example value: "Sean Watase".*

**lengthSeconds**

Description: The duration of the video in seconds.



**viewCount**

Description: The number of views for the video.

**keywords**

Description: A list of keywords related to the video.

*Example value: ["thirdweb nft", "erc721 smart contract", "how to make money with nfts"].*

**isLiveContent**

Description: Indicates whether the video is a live stream.

**thumbnail**

Description: A list of video thumbnail images with their resolutions.
Example value:

```
[
  {
    "url": "https://i.ytimg.com/vi/DSffICxyj3A/maxresdefault.jpg",
    "width": 1280,
    "height": 720
  }
]
```

**embed.iframeUrl**

Description: URL for embedding the video in an iframe.

*Example value: "https://www.youtube.com/embed/DSffICxyj3A".*

**embed.width and embed.height**

Description: The width and height of the embedded video.

**ownerProfileUrl**

Description: The profile URL of the video owner.
Example value: "http://www.youtube.com/@SeanWatase".

**externalChannelId**

Description: The external ID of the channel.
Example value: "UChjGu9jkMSz_A2qQV1G-Y9w".

**isFamilySafe**

Description: Indicates whether the video is family-friendly.

**availableCountries**

Description: A list of countries where the video is available.
Example value: ["US", "GB", "CA", "AU"].

**category**

Description: The category of the video.
*Example value: "Science & Technology".*

**publishDate and uploadDate**

Description: The publication and upload dates of the video.
*Example values:
publishDate: "2022-10-14T11:51:29-07:00".
uploadDate: "2022-10-14T11:51:29-07:00".*

**isUnlisted**
Description: Indicates whether the video is unlisted.

---
[See the API in action – test it instantly here ](https://api999.short.gy/j0OhRm)

---

### **Feel free to write to me with any questions not listed in the documentation! :)**

If you have any inquiries or need further assistance, don’t hesitate to reach out. I’m here to help!

#### **Telegram Support:**

You can easily reach me on Telegram group for quick support or any additional questions.

https://t.me/+Zlto9kxqYjthYTQy
