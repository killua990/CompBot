## ๐๐๐๐๐  โ๐๐โโ๐ผ๐๐๐โ ๐น๐๐  

## แดแดสแดษชาแดษดแดแดษชแดษด วซแดแดสษชแดส แดแดแดแดสแดssแดส  

### A Telegram Video CompressorBot  

- it compress videos with negligible Quality change.
- u can generate sample Compressed videos nd screenshots too.
- u can set custom video name nd Thumbnail.
- u can get logs videos to a channel too.
- Coz of its Quality encode It takes little time to Compress.
- For now i set it for maximum 5 Processes at a time.
- Its Running Without Db so Block /ban /Broadcast Feature is currently Not available.



### ๐ณ๐พ๐ฒ๐บ๐ด๐ ๐ต๐ธ๐ป๐ด

- FROM python:3.9.2-slim-buster

- RUN mkdir /bot && chmod 777 /bot

- WORKDIR /bot

- ENV DEBIAN_FRONTEND=noninteractive

- RUN apt -qq update && apt -qq install -y git wget pv jq wget python3-dev ffmpeg mediainfo

- COPY . .

- RUN pip3 install -r requirements.txt

- CMD ["bash","run.sh"]
