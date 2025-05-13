<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# install ubuntu faster-whisper-webui

To install faster-whisper-webui on Ubuntu, follow these steps:

1. Clone the repository:
```bash
git clone https://huggingface.co/spaces/aadnk/faster-whisper-webui
cd faster-whisper-webui/
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
pip install -r requirements-fasterWhisper.txt
```

3. Install additional system packages:
```bash
sudo apt install nginx ffmpeg
```

4. Configure Nginx:
Edit `/etc/nginx/sites-available/default` and add the following location block:
```nginx
location / {
    proxy_pass http://127.0.0.1:7860;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "Upgrade";
}
```

5. Modify Nginx configuration to increase max body size:
Edit `/etc/nginx/nginx.conf` and add:
```nginx
client_max_body_size 1000M;
```

6. Start Nginx:
```bash
sudo service nginx start
```

7. Run the faster-whisper-webui application:
```bash
python3 app.py --input_audio_max_duration -1 --server_name 127.0.0.1 --auto_parallel True
```

After completing these steps, you should be able to access the faster-whisper-webui interface through your web browser[^2].

## Additional Notes

- Ensure you have Python 3.8 or higher installed on your system[^3].
- If you encounter any issues with FFmpeg, make sure it's properly installed and added to your system PATH[^1].
- For optimal performance, consider using a system with GPU support and appropriate CUDA libraries[^4].

<div style="text-align: center">⁂</div>

[^1]: https://github.com/jhj0517/Whisper-WebUI

[^2]: https://gist.github.com/kiang/0d67d9c929c81de7e1f57e815dc23037

[^3]: https://hiro20180901.com/2024/01/11/whisper-and-faster-whisper-and-whisper-webui-install-method-on-wsl2-ubuntu-22-04-lts/

[^4]: https://www.youtube.com/watch?v=Kyc0AgMIBSU

[^5]: https://www.reddit.com/r/LocalLLaMA/comments/1d1j31r/faster_whisper_server_an_openai_compatible_server/

[^6]: https://huggingface.co/spaces/aadnk/faster-whisper-webui

[^7]: https://hub.docker.com/r/linuxserver/faster-whisper

[^8]: https://www.incredigeek.com/home/using-fasterwhisper-on-ubuntu/

