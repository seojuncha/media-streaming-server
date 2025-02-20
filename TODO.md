## Ver 1.
Simple RTSP Server written in C.
Bypass original stream, no transcode, no trasmux.

- input: media container file(mp4, etc)
- output: rtsp/rtp stream
- play: vlc

### Feature & Library
- Media (ffmpeg)
  - Read a media file
  - Demux the file
  - Get encoded video/audio stream

- RTSP (native C)
  - server
    - listen
    - accept client connections
    - read client's request
      - then, feed it to parser
    - send response
  - parser

- RTP (native C)
  - packetize

### Hacking Method
- Protocol Analysis
  - [rtsp-simple-server](https://github.com/bhaney/rtsp-simple-server)