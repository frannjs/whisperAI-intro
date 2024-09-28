# whisperAI-intro COMMANDS 

### COMMANDS FOR MAC:

LIST DEVICES:
```
ffmpeg -f avfoundation -list_devices true -i "" 
```

CREATE FOLDER:
```
folder name: voice recognition
```

RECORD AUDIO AND SAVE THE FILES:
```
ffmpeg -f avfoundation -i ":MacBook Pro Microphone" -t 5 "/Users/francostratta/Desktop/voice recognition/$(date +'%Y%m%d').mp3"
```
CONVERT AUDIO FILE INTO .TXT FILE:
```
whisper 20240928.mp3 --language Spanish --fp16 False
```


### COMMANDS FOR WINDOWS:

LIST DEVICES:
```
ffmpeg -list_devices true -f dshow -i dummy
```

CREATE FOLDER:
```
mkdir "voice recognition"
```

RECORD AUDIO AND SAVE THE FILES:
```
ffmpeg -f dshow -i audio="Microphone (Your Microphone Name)" -t 5 "%USERPROFILE%\Desktop\voice recognition\%date:~-4,4%%date:~-10,2%%date:~-7,2%.mp3"
```

CONVERT AUDIO FILE INTO .TXT FILE:
```
whisper 20240928.mp3 --language Spanish --fp16 False
```
