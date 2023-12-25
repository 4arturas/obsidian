https://github.com/ggerganov/whisper.cpp/pkgs/container/whisper.cpp

```sh
# download model and persist it in a local folder
docker run -it --rm -v path/to/models:/models whisper.cpp:main "./models/download-ggml-model.sh base /models"
```

```sh
# transcribe an audio file
docker run -it --rm -v path/to/models:/models -v path/to/audios:/audios whisper.cpp:main "./main -m /models/ggml-base.bin -f /audios/jfk.wav"
````

```sh
# transcribe an audio file in samples folder
docker run -it --rm -v path/to/models:/models whisper.cpp:main "./main -m /models/ggml-base.bin -f ./samples/jfk.wav"
```

