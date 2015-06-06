# VERSION:		0.1
# DESCRIPTION:	Create keepass2 container with its dependencies
# AUTHOR:		Christian Koep <christian.koep@fom-net.de>
# USAGE:
#	# Build keepass2 image
#	docker build -t keepass2 .
#
#	# Run the container and mount your keepass2 database file
#	docker run -it \
#		-v /home/$USER/DB.kdbx:/root/DB.kdbx \
#		-v /tmp/.X11-unix:/tmp/.X11-unix \
#		-e DISPLAY=$DISPLAY \
#		keepass2
#
# ISSUES:
#	# 'Gtk: cannot open display: :0'
#	Try to set 'DISPLAY=your_host_ip:0' or run 'xhost +' on your host.
#	(see: http://stackoverflow.com/questions/28392949/running-chromium-inside-docker-gtk-cannot-open-display-0)
#

FROM debian:jessie
MAINTAINER Christian Koep <christian.koep@fom-net.de>

ENV DEBIAN_FRONTEND noninteractiv

RUN apt-get update && apt-get install -y \
	keepass2 \
	xdotool

CMD ["/usr/bin/keepass2"]