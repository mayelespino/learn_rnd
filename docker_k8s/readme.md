# Notes on Kubernetes and Docker


# Links

- an UBUNTU desktop that can be accessed via web browser | https://github.com/fcwu/docker-ubuntu-vnc-desktop |
- Running VNC server | https://www.howtogeek.com/devops/how-to-run-gui-applications-in-a-docker-container/

```
FROM ubuntu:latest
RUN apt-get update && apt-get install -y firefox x11vnc xvfb
RUN echo "exec firefox" > ~/.xinitrc && chmod +x ~/.xinitrc
CMD ["v11vnc", "-create", "-forever"]
```

