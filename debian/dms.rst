=========
 dms
=========

---------------------------------------------
UPnP DLNA Digital Media Server
---------------------------------------------

:Manual section: 1

Synopsis
--------

**dms** [*options*]


Description
-----------

dms is a UPnP DLNA Digital Media Server. It runs from the terminal, and serves
content directly from the filesystem from the working directory, or the path
given. The SSDP component will broadcast and respond to requests on all
available network interfaces.

dms advertises and serves the raw files, in addition to alternate transcoded
streams when it's able, such as mpeg2 PAL-DVD and WebM for the Chromecast. It
will also provide thumbnails where possible.

dms uses ``ffprobe``/``avprobe`` to get media data such as bitrate and
duration, ``ffmpeg``/``avconv`` for video transoding, and
``ffmpegthumbnailer`` for generating thumbnails when browsing. These
commands must be in the ``PATH`` given to ``dms`` or the features
requiring them will be disabled.

Known Compatible Players and Renderers
======================================

 * Probably all Panasonic Viera TVs.
 * Android's BubbleUPnP and AirWire
 * Chromecast
 * VLC
 * LG Smart TVs, with varying success.


Options
-------

-h, --help              show this help message and exit

-config string    	json configuration file

-fFprobeCachePath string    	path to FFprobe cache file (default "/home/drew/.dms-ffprobe-cache")

-friendlyName string    	server friendly name

-http string    	http server port (default ":1338")

-ifname string    	specific SSDP network interface

-ignoreHidden    	ignore hidden files and directories

-ignoreUnreadable    	ignore unreadable files and directories

-logHeaders    	log HTTP headers

-noProbe    	disable media probing with ffprobe

-noTranscode    	disable transcoding

-notifyInterval duration    	interval between SSPD announces (default 30s)

-path string    	browse root path

-stallEventSubscribe    	workaround for some bad event subscribers

