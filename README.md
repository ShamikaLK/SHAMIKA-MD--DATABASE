# <div align='center'>SHAMIKA-MD-DATABASE</div>

<div align="center">

  <img src="https://i.ibb.co/93c0VgP7/shamika-wa-baileys.jpg" />

</div>

## Install
Install in index.js in your bot

<bAuto Voice</b>
```
https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/VOICE-CLIPS/SHAMIKA-MD-VOICE
```

<bAuto Sticker</b>
```
https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/STICKERS-RAW/SHAMIKA-MD-STICKER
```

<bAuto Msg</b>
```
import makeWASocket from '@whiskeysockets/baileys'
```

<b>Anti Links</b>
```
https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/refs/heads/main/ANTI-LINKS/SHAMIKA-MD-ANTI-LINKS
```

<b>Bad Word</b>
```
https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/BAD-WORDS/SHAMIKA-MD-ANTI-BAD
```

## Exsample Code


```
if (config.AUTO_VOICE === 'true') {
      const url = 'https://raw.githubusercontent.com/ShamikaLK/SHAMIKA-MD--DATABASE/main/VOICE-CLIPS/SHAMIKA-MD-VOICE';
      try {
          let { data } = await axios.get(url);
          
          for (let vr in data) {
              if ((new RegExp(`\\b${vr}\\b`, 'gi')).test(body)) {
                  await conn.sendMessage(from, {
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
```
