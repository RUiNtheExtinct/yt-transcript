# Real time cheap as heck transcription service

## Components

### Github actions

open sourcing this content again for free computing power

### Libraries

-   ffmpeg
-   wit.ai or whisper
-   youtube-dl
-   yt-dlp
-   asyncio

Python cmd tool to parse any youtube video or livestream and save it in 10 seconds intervals to send to whisper/wit.ai for speech recognization (free to use).

Install [ffmpeg](https://ffmpeg.org/download.html) for best results. **(NOT optional)**

Install [MySQL](https://dev.mysql.com/downloads/installer/) and add the required keys to the .env file to save the generated transcriptions to database. **(optional)**

Create a discord webhook and add the webhook url to the .env file to send the generated transcriptions for a livestream to your discord server. **(optional)**

-   To transcribe/download private videos/livestreams,you will need atleast one youtube account with atleast `view` access to the private video/livestream.
-   You will also need the youtube cookies from your browser in the Netscape HTTP Cookie File format.
-   To get that you need the [`Get Cookies.txt`](https://chrome.google.com/webstore/detail/get-cookiestxt-clean/ahmnmhfbokciafffnknlekllgcnafnie?hl=en-GB) extension.
-   Now go to any youtube video and click on the extension icon and click on `Export cookies.txt` and save the file.
-   Make sure that you are logged in to youtube in your browser from the account that has access to view the private video/livestream.
-   Make sure that the cookies file is in the root directory of this project and named `ytcookies.txt`.

### Usage

-   Install the required libraries using `pip install -r requirements.txt`
-   Create a `.env` file in the root directory of this project and add the keys to it by following the [`.env.example`](./.env.example) file.
-   To get transcription for a youtube video, run:
    ```python
    	python transcribe_video_private.py --url="<youtube_video_url>"
    ```
-   To get live transcriptions for an ongoing youtube livestream, run:
    ```python
    	python transcript_manager.py --url="<youtube_livestream_url>"
    ```
