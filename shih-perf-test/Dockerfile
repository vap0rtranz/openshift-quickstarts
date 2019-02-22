FROM registry.access.redhat.com/rhel7
MAINTAINER Justin Pittman (justin.pittman@redhat.com)
# pull official RHEL container image, must have access to RH container catalog
#WORKDIR /usr/src/myapp
CMD [ echo, "hello world from container"]
USER root
CMD [ yum, install, "-y", "gcc", "gcc-c++", "make", "libXext-devel", "perl", "perl-Time-HiRes", "libX11-devel", "mesa-libGL-devel", "git"]
USER justin
CMD [ git, clone, "https://github.com/kdlucas/byte-unixbench"]
CMD [ cd, byte-unixbench ]
RUN [ "./Run" ]
EXPOSE 8080
