# Calibre

Calibre using docker.

Run:

```shell
docker run --rm \
  -e DISPLAY=unix:0 \
  -e GDK_DPI_SCALE \
  -e GDK_SCALE \
  -v /etc/localtime:/etc/localtime:ro \
  -v /tmp/.X11-unix:/tmp/.X11-unix \
  -u $(id -u) \
  -e HOME \
  -v $HOME/Books:$HOME/Books \
  -v $HOME/Dropbox/Calibre-config:$HOME/.config/calibre \
  dmitryrck/calibre calibre
```
