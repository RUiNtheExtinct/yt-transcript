# Real Time Youtube Transcription

A cli based transcription tool that can transcribe any youtube video provided an url or any locally downloaded video.

## Components

Python cmd tool to parse any youtube video or livestream and save it in 10 seconds intervals to send to whisper/wit.ai for speech recognization (free to use).

Install [ffmpeg](https://ffmpeg.org/download.html) for best results. **(NOT optional)**

Install [MySQL](https://dev.mysql.com/downloads/installer/) and add the required keys to the .env file to save the generated transcriptions to database. **(optional)**

Create a discord webhook and add the webhook url to the .env file to send the generated transcriptions for a livestream to your discord server. **(optional)**

For transcribing private videos:

-   To transcribe/download private videos/livestreams,you will need atleast one youtube account with atleast `view` access to the private video/livestream.
-   You will also need the youtube cookies from your browser in the Netscape HTTP Cookie File format.
-   To get that you need the [`Get Cookies.txt`](https://chrome.google.com/webstore/detail/get-cookiestxt-clean/ahmnmhfbokciafffnknlekllgcnafnie?hl=en-GB) extension.
-   Now go to any youtube video in your browser and click on the `Get Cookies.txt` extension icon.
-   Click on `Export cookies.txt` and save the file.
-   Make sure that you are logged in to youtube in your browser from the account that has access to view the private video/livestream.
-   Save the cookies file in the root directory of this project and name it `ytcookies.txt`.

### Usage

-   Install the required libraries using `pip install -r requirements.txt`
-   Create a `.env` file in the root directory of this project and add the keys to it by following the [`.env.example`](./.env.example) file.
-   To get transcription for any youtube video, run:

```bash
    python transcribe_video.py --url="<youtube_video_url>"
```

-   To get live transcriptions for an ongoing youtube livestream, run:

```bash
    python transcript_livestream.py --url="<youtube_livestream_url>"
```

-   To transcribe a downloaded video, run:

```bash
    python transcribe_video.py --url="<video_path>"
```

### Livestream Transcription options

--url <string> : the url or path to the video that you want to transcribe

--interval_size <integer> : time interval between getting transcripts on livestream in seconds, default = 60

--save_to_db <integer> : Saves transcription to sql database, False if input is 0, True for any other number, default = 0
