# Amazon Music Downloader - AMZ-DL / AMP-V2

Thank you for using AMZ-DL / AMP-V2 by SpinnySpiwal!

Usage: production.py [-h] [--use-cache] [--no-license-cache] [--enable-download] [--album ALBUM] [--asinlist ASINLIST] [--track TRACK] [--search SEARCH] [--tracksearch] [--audio-workaround] [--atmos-enable] [--uhd-enable] [--hd-enable] [--shuffle]
                     [--skip-all] [--play-all] [--inappdownload] [--iadlist] [--no-album-cache] [--no-discord-rpc] [--no-interactive] [--enable-export] [--export-path EXPORT_PATH]

AMZ-DL is a tool by SpinnySpiwal to stream and download content from Amazon Music. This tool is intended for educational purposes only. Please refer to the following format for cfg.json: { "email": "example@example.com", "pwd": "password-example" }

Command Line Arguments:
  * -h, --help            Show this help message and exit.
  * --use-cache           Use cached credentials if available.
  * --no-license-cache    Do not use the license cache.
  * --enable-download     Download songs.
  * --album ALBUM         Specify the album to play/download.
  * --asinlist ASINLIST   Provide a list of ASINs to play/download.
  * --track TRACK         Specify the track to play/download.
  * --search SEARCH       Enter the search query.
  * --tracksearch         Enable track search functionality.
  * --audio-workaround    Use this to work around downmixing to 2 channels when forcing Atmos. (DISABLED)
  * --atmos-enable        Enable Atmos. (BROKEN)
  * --uhd-enable          Enable UHD.
  * --hd-enable           Enable HD.
  * --shuffle             Shuffle the tracks.
  * --skip-all            Index decryption keys by skipping all tracks.
  * --play-all            Play all tracks.
  * --inappdownload       Download a track from in-app.
  * --iadlist             Download a list of tracks from in-app.
  * --no-album-cache      Do not use the album cache.
  * --no-discord-rpc      Disable Discord RPC.
  * --no-interactive      Disable interactive mode.
  * --enable-export       Export songs from compressed zlib format to the song format.
  * --export-path EXPORT_PATH Specify the path to export the songs to.

## Help & Troubleshooting

* Q: Why are my credentials not working?
  * A: Please ensure that your credentials are correct and that you have not made any typos.

* Q: Why is the tool not working?
  * A: Please ensure using a https proxy that there is no programming errors. If there is, please report it to me.

* What is a device.wvd file?
  * A: A device.wvd file is a file that contains the Widevine® DRM license for the tool.

* What is a cfg.json file?
  * A: A cfg.json file is a file that contains the user's credentials. It is used to login to the user's Amazon Music account.

* What is a rpc_quotes.txt file?
  * A: A rpc_quotes.txt file is a file that contains quotes for the Discord Rich Presence. A default one is provided if a file is not found.

* Why is my search cache so large?
  * To clear your search cache, please wait 1 hour for the previous queries to be invalidated or manually delete the file yourself.

* Why do we need a decryption key cache?
  * A: A decryption key cache is used to speed up the decryption process.
  * Q: Why is my decryption key cache so large?
  * A: Your decryption key cache is large because you have been using the tool for a long time. Clearing it is not recommended. As the more keys you have, if the widevine protocol is ever updated, the keys will still be there.

* Why do I need user_agents.json?
  * A: user_agents.json is a file that contains a list of user agents. It is used to bypass Amazon's device verification. As the dynamically changing user agents confuse amazon, user agent randomization is used to prevent profiling and tracing of our tool.

* Why am I stuck with OPUS 320kbps?
  * A: Amazon Music only supports Opus 320kbps. To stream or download in other formats, use `--hd-enable` or `--uhd-enable`. The status of your Amazon Music subscription does not matter. For some reason, anyway.

* What is mpv?
  * A: mpv is a media player that can play audio and video files. It is used to play the downloaded songs. Please install it from [here](https://mpv.io/installation/).

Example:
```
python3.12 dist/production.py --use-cache --tracksearch --search "Shout Out to My Ex"
```


