# svenBot
svenBot is a **simple/lightweight** non-guild music bot for Discord, made with **Python 3.6**. 
This bot is built for private hosting, custom use. Now using the rewrite version of Discord.py.
During the rewrite migration I removed some bloaty features, the bot is again a little lighter.

## Installation
Clone this repo:
```
$ git clone https://github.com/johanhelmuth/svenBot.git
```

Install required Python libraries (using requirements.txt that comes with this repo):
```
$ pip install -r requirements.txt
```
**Important:** Installing the discord.py[voice] package (included in requirements.txt) 
should be enough to get opus up and running, but if you're having issues with it connecting to voice, 
then install libopus0 on your system. This bot also requires the host to have ffmpeg installed on the system.
You should use this bot with ffmpeg 3.4+. Should be simple enough to figure out.

Ubuntu 18.04 LTS example (if you have something earlier than ffmpeg 3.4):
```
$ sudo add-apt-repository ppa:jonathonf/ffmpeg-3
$ sudo apt update
$ sudo apt install ffmpeg
$ sudo apt install libopus0
```

## Configure
Now it's time to configure `config.py`. Go to https://discordapp.com/developers/applications/ 
and create an application, name the application/bot whatever you want. When you have 
created the application, you should be able to see the token under the "Bot" tab, by clicking 
"Click to reveal token". Copy that token into the `config.py` file. 

## Run
Run bot.py using Python 3.6, Python alias may vary:
```
$ python bot.py
```

## Commands
| Commands          | Description                                                                       |
| ----------------- | --------------------------------------------------------------------------------- |
| !play             | Plays/queues video, use URL or search string.                                     |
| !stop             | Clears queue and leaves voice channel.                                            |
| !skip             | Skips current song.                                                               |
| !q                | Outputs out the current queue of songs.                                           |
| !vol              | Adjust volume using value between 1-100 (no value will output current volume).    |