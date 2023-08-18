# Real time cheap as heck transcription service

## Components

### Github actions

open sourcing this content again for free computing power

### Libraries

-   ffmpeg
-   wit.ai or speech recognization or whisper
-   youtube-dl
-   yt-dlp
-   asyncio

Python cmd tool to parse any youtube video or livestream and save it in 10 seconds intervals to send to whisper/wit.ai for speech recognization (free to use).

-   To transcribe/download private videos/livestreams,you will need atleast one youtube account with atleast `view` access to the private video/livestream.
-   You will also need the youtube cookies from your browser in the Netscape HTTP Cookie File format.
-   To get that you need the [`Get Cookies.txt`](https://chrome.google.com/webstore/detail/get-cookiestxt-clean/ahmnmhfbokciafffnknlekllgcnafnie?hl=en-GB) extension.
-   Now go to any youtube video and click on the extension icon and click on `Export cookies.txt` and save the file.
-   Make sure that you are logged in to youtube in your browser from the account that has access to view the private video/livestream.
-   Make sure that the cookies file is in the root directory of this project and named `ytcookies.txt`.
