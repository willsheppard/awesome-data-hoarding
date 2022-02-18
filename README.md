# data-hoarding

A collection of code and tools for scraping, hoarding, organising and browsing data

Inspired by Reddit's /r/DataHoarder

## Scraping tools

### General purpose

- [wget](https://www.gnu.org/software/wget/manual/wget.html)
    - Example: `wget --mirror --convert-links --adjust-extension --page-requisites --span-hosts -U Mozilla -e robots=off --no-cookies -D www.example.com,files.example.com,images.example.com http://www.example.com/`

- [StreamRipper](http://streamripper.sourceforge.net)
    - Example: `streamripper ###URL### -u "FreeAmp/2.x" -q -l 86400`

### Specialised

- [youtube-dl](https://yt-dl.org)
    - Example: `youtube-dl "$1" --ignore-errors --extract-audio --audio-quality 0 --audio-format mp3 --prefer-ffmpeg --output "%(title)s.%(ext)s" `
    - Album: `youtube-dl "$1" --ignore-errors --extract-audio --audio-quality 0 --audio-format mp3 --prefer-ffmpeg --output "%(album)s - %(artist)s - %(track)s.%(ext)s"`
    - Playlist: `youtube-dl "$1" --ignore-errors --extract-audio --audio-quality 0 --audio-format mp3 --prefer-ffmpeg --output "%(playlist_title)s/%(playlist_title)s - %(playlist_index)02d - %(artist)s - %(title)s.%(ext)s"`

- [DiscordChatExporter](https://github.com/Tyrrrz/DiscordChatExporter) + excellent [wiki](https://github.com/Tyrrrz/DiscordChatExporter/wiki)
    - Example: `docker run --rm -v /var/www/zaphod/adhd:/app/out tyrrrz/discordchatexporter:stable export --channel ###ID### --token ###SECRET### --format Json`
    - List guilds: `docker run tyrrrz/discordchatexporter:stable guilds`
    - List channels: `docker run tyrrrz/discordchatexporter:stable channels --guild ###ID###`

## Communities

- https://www.reddit.com/r/DataHoarder

## Similar projects

- https://github.com/igorbarinov/awesome-data-engineering
- https://github.com/lorien/awesome-web-scraping
