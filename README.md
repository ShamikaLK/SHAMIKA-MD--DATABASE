# <div align='center'> <b>**SHAMIKA-MD-DATABASE**</b> <img src = "https://github.com/7oSkaaa/7oSkaaa/blob/main/Images/Software_Tools.gif?raw=true" width = 50px> </div> 

<div align="center">

  <img src="https://i.ibb.co/TDX2Dch5/SHAMIKA-MD-DATABASE.png" />
      <p align="center">
      <a href="#">
  <img title="Creator" src="https://img.shields.io/badge/Creator-SHAMIKA_HARSHAMAL-red.svg?style=for-the-badge&logo=github">

  <b><a href="#"><img src="http://readme-typing-svg.herokuapp.com/?color=FF2024&center=true&vCenter=true&multiline=false&lines=Update+coming+soon+...+!" alt="" width = 900px></b>
</div>

## Installation <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="25">
Install in index.js in your bot

<b>Auto Voice</b>
```
https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/VOICE-CLIPS/SHAMIKA-MD-VOICE
```

<b>Auto Sticker</b>
```
https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/STICKERS-RAW/SHAMIKA-MD-STICKER
```

<b>Auto Msg</b>
```
Coming Soon.....
```

<b>Anti Links</b>
```
https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/refs/heads/main/ANTI-LINKS/SHAMIKA-MD-ANTI-LINKS
```

<b>Bad Word</b>
```
https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/BAD-WORDS/SHAMIKA-MD-ANTI-BAD
```

## Exsample Code <img src = "https://github.com/7oSkaaa/7oSkaaa/blob/main/Images/CP_PS.gif?raw=true" width = 50px>

🌟 Type cjs & Ems Code for index.js file
```js
if (config.AUTO_VOICE === 'true') {
      const url = 'https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/VOICE-CLIPS/SHAMIKA-MD-VOICE';
      try {
          let { data } = await axios.get(url);
          
          for (let vr in data) {
              if ((new RegExp(`\\b${vr}\\b`, 'gi')).test(body)) {
                  await sock.sendMessage(from, {
                      audio: {
                          url: data[vr]
                      },
                      mimetype: 'audio/mpeg',
                      ptt: true
                  }, { quoted: mek });
                  break; // Voice එකක් හමු වූ පසු ඉතුරු loop එක නවතන්න. // Stop the rest of the loop after finding a voice. 
              }
          }
      } catch (error) {
          console.error("Error fetching voice clips:", error);
      }
  }
````
🌟 Type cjs Code for auto.js file

```js
const config = require('../config');
const { cmd, commands } = require('../command');
const { fetchData } = require('../lib/functions');

cmd({
    on: "body"
}, async (sock, mek, m, { from, body, isOwner }) => {
    try {
        const voiceUrl = 'https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/VOICE-CLIPS/SHAMIKA-MD-VOICE';
        const data = await fetchData(voiceUrl);
        
        for (const text in data) {
            if (body.toLowerCase() === text.toLowerCase()) {
                if (config.AUTO_VOICE === 'true') {
                    //if (isOwner) return;        
                    await sock.sendPresenceUpdate('recording', from);
                    await sock.sendMessage(from, { 
                        audio: { url: data[text] }, 
                        mimetype: 'audio/mpeg', 
                        ptt: true 
                    }, { quoted: mek });
                }
            }
        }
    } catch (error) {
        console.error('Error in auto voice:', error);
    }
});

````
<br>

-----

<br>

## Notes ‼️
Thank for using this.
Please give this a star and a fork this repo. It would be a great help to me. Don't forget to follow me.

<b>📆 Last Update:-</b> 2025/06/27<br> 
<b>🕛 Last Update Time:-</b> 09:15pm
<br>

<div align="center">
  <p><b>Shamika Harshamal Project in <i>SHAMIKA-MD--DATABASE</i></b></p>
</div>
