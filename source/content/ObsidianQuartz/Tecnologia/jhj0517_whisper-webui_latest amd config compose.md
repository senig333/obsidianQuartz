<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# jhj0517/whisper-webui:latest amd config compose

To configure and run the jhj0517/whisper-webui:latest Docker image on an AMD system, you can use the following docker-compose configuration:

```yaml
version: '3'
services:
  whisper-webui:
    image: jhj0517/whisper-webui:latest
    volumes:
      - /path/to/models:/Whisper-WebUI/models
      - /path/to/outputs:/Whisper-WebUI/outputs
    ports:
      - "7860:7860"
    command: --server_name 0.0.0.0 --server_port 7860
```

Make sure to replace `/path/to/models` and `/path/to/outputs` with the actual paths on your system where you want to store the models and outputs[^1][^4].

For AMD systems, you should remove the NVIDIA-specific deployment configuration. If you're using a different GPU, you may need to adjust the `requirements.txt` file to match your environment[^2][^3].

To run the container:

1. Save the above configuration as `docker-compose.yaml` in your project directory.
2. Open a terminal in that directory.
3. Run the following command:
```bash
docker-compose up
```

After the container starts, you can access the Whisper WebUI by opening `http://localhost:7860` in your web browser[^2][^3].

<div style="text-align: center">⁂</div>

[^1]: https://huggingface.co/spaces/jhj0517/Whisper-WebUI/blob/e2af0e00cd0ad5ba417d0e0b330de7c2fa103169/docker-compose.yaml

[^2]: https://huggingface.co/spaces/jhj0517/Whisper-WebUI/blame/d4bc29b9a0aa067c59c0ff4833787e0193a3bbe5/README.md

[^3]: https://github.com/jhj0517/Whisper-WebUI

[^4]: https://docker-compose.net/lvjxqpjn

[^5]: https://github.com/jhj0517/Whisper-WebUI/blob/master/docker-compose.yaml

[^6]: https://hub.docker.com/r/jhj0517/whisper-webui

[^7]: https://colab.research.google.com/github/jhj0517/Whisper-WebUI/blob/master/notebook/whisper-webui.ipynb

[^8]: https://www.reddit.com/r/artificial/comments/11kreit/introducing_whisper_webui_easy_subtitle_generator/

