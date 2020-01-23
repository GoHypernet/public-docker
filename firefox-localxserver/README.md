# firefox-localxserver
This runs Firefox on the latest Ubuntu inside of Docker, connected to your local X server. This is based on https://dev.to/darksmile92/run-gui-app-in-linux-docker-container-on-windows-host-4kde.

# How To Use
This container requires you to have a local X server setup. On windows, you can use VcXsrv, on OSX XQuartz works great, on Linux you probably already have one. The key thing is to set the DISPLAY environment variable in the container to something that will connect to your X server. 

To start the container, use this command:
    docker run -it --rm -e DISPLAY=YOUR.IP.ADDR.HERE:0.0 IMAGEID google.com

Where:
DISPLAY is the display string for your local X server. On windows using VcXsrv, the example string will suffice.
IMAGEID is the ID of the built image, can be grabbed from
    docker images
google.com can be any url you want the browser to open with.

