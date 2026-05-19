What you need

ESP32-S3 with display and LVGL in ESPHome
Home Assistant with Music Assistant
SSH access to HA
Python with Pillow library (pip3 install Pillow --break-system-packages)<img width="4032" height="3024" alt="IMG_1886" src="https://github.com/user-attachments/assets/e5597a54-63be-4c3f-a495-735e1c1b5f05" />
<img width="4032" height="3024" alt="IMG_1888" src="https://github.com/user-attachments/assets/df6f4357-16d5-44ca-8faf-95077dc354da" />


How it works
Music Assistant creates its own media player entity (in my case media_player.voice_mass_3) that has an entity_picture attribute with the direct Spotify CDN image URL — it is publicly accessible without authentication.

Step 1 — Python script for color extraction
Save as /config/album_color.py:
https://www.homeassistant-cz.cz/viewtopic.php?p=26053#p26053
Step 2 — HA Configuration
Into configuration.yaml:

Automation that runs a script when a song changes:

Step 3 — ESPHome YAML
Album Cover:

Dynamic colors — sensors + lambda:

Result
The UI automatically changes color with each new song. The text brightness is adjusted to always be readable.

the last idle page, I have a file to test, so it's not much use
with the red button I turn off the amplifier that I connected to the vpe (sendspin), think about whether to leave it, it suits me, it's good to see if it's on.
then it still wants to fix the "next" icon button and then probably the background around the image
so I spent almost the whole night on it and the last few hours with a lot of help from AI, so Claude has a big part in making it work + he prepared a summary for me
And finally, thanks to Pete30, who will definitely know his job there
and of course Claude
