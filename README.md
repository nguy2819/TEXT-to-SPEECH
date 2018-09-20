# TEXT TO SPEECH

> The 2 most important parts in this project are index.js, script in index.html, and lastly, the summary from voice.js
- In index.js
```
import allVoices from './voice';

const msg = new SpeechSynthesisUtterance();
msg.volume = 1; // 0 to 1
msg.rate = 1; // 0.1 to 10
msg.pitch = 1; //0 to 2
msg.text = "My wonderful husband, I always love you";

const voice = allVoices[4] // 47 total
console.log(`voice: ${voice.name}, language: ${voice.lang}`)
msg.voiceURI = voice.voiceURI;
msg.lang = voice.lang;

speechSynthesis.speak(msg);
```

- In index.html
```
<body>
    <script src="index.pack.js"></script>
</body>
```
