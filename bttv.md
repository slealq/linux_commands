# Streaming one of the signals to RTSP locally
This following command to open a streaming channel on the server side.

     cvlc -vvv v4l2:///dev/video0 --sout '#transcode{vcodec=mp4v, acodec=none, vb=2000, ab=0}:rtp{sdp=rtsp://:8554/}'

Where the `/dev/video0` is the input you want to transmit and `:8554/` is the port to transmit to.

Now to listen to this channel, then run the following command:

    vlc rtsp://192.168.1.60:8554/

# Changing settings of standards and capture

When using the Geovision 850 cards, the standard was set to PAL instead of NTSC

    v4l2-ctl -d 0
    v4l2-ctl -d 0 --get-standard
    v4l2-ctl -d 0 --set-standard=ntsc