## 𝕍𝕚𝕕𝕖𝕠 ℂ𝕆𝕄ℙℝ𝔼𝕊𝕊𝕆ℝ 𝔹𝕆𝕋  

## ᴍᴜʟᴛɪғᴜɴᴄᴛɪᴏɴ ǫᴜᴀʟɪᴛʏ ᴄᴏᴍᴘʀᴇssᴏʀ  

### A Telegram Video CompressorBot  

- it compress videos with negligible Quality change.
- u can generate sample Compressed videos nd screenshots too.
- u can set custom video name nd Thumbnail.
- u can get logs videos to a channel too.
- Coz of its Quality encode It takes little time to Compress.
- For now i set it for maximum 5 Processes at a time.
- Its Running Without Db so Block /ban /Broadcast Feature is currently Not available.



🅳🅾🅲🅺🅴🆁 🅵🅸🅻🅴

FROM python:3.9.2-slim-buster

RUN mkdir /bot && chmod 777 /bot

WORKDIR /bot

ENV DEBIAN_FRONTEND=noninteractive

RUN apt -qq update && apt -qq install -y git wget pv jq wget python3-dev ffmpeg mediainfo

COPY . .

RUN pip3 install -r requirements.txt

CMD ["bash","run.sh"]
