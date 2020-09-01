# chromakey
Use gstreamer to create a dummy V4L2 device combining a still image and live video by turning a _greenscreen_ background into an alpha channel.

You'll need to install the v4l2loopback kernel modules.
`sudo apt install v4l2loopback-dkms`

Then create the loopback device. In my case it ends up as `/dev/video2` because I have two
other devices.
`sudo modprobe v4l2loopback`