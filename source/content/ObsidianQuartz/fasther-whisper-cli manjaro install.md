# fasther-whisper-cli manjaro install

To install faster-whisper-cli on Manjaro, follow these steps:

1. Open a terminal on your Manjaro system.
2. Ensure you have Python and pip installed. Manjaro uses Python 3 by default, so you can install pip using:

```bash
sudo pacman -S python-pip
```

3. It's recommended to create a virtual environment for the installation:

```bash
python -m venv whisper-env
source whisper-env/bin/activate
```

4. Install faster-whisper-cli using pip:

```bash
pip install faster-whisper-cli
```

5. To utilize GPU acceleration, make sure you have NVIDIA drivers and CUDA installed[^1]. You can install them using:

```bash
sudo pacman -S nvidia cuda
```

6. Verify the installation by running:

```bash
faster-whisper --help
```


This should install faster-whisper-cli on your Manjaro system. Remember to activate the virtual environment whenever you want to use the tool. For optimal performance, ensure your NVIDIA drivers and CUDA are properly configured[^1][^3].

<div style="text-align: center">⁂</div>

[^1]: https://www.toolify.ai/ai-news/stepbystep-guide-setting-up-manjaro-and-installing-audio-whisper-project-1634850

[^2]: https://www.toolify.ai/ai-news/local-realtime-transcription-with-audio-whisper-1733

[^3]: https://www.youtube.com/watch?v=RS5RSCRpasA

[^4]: https://www.youtube.com/watch?v=e1pmV8l7uLs

[^5]: https://snapcraft.io/install/whisper-cpp/manjaro

[^6]: https://snapcraft.io/install/whisper-gael/manjaro

[^7]: https://github.com/absadiki/subsai

[^8]: https://pypi.org/project/faster-whisper-cli/

