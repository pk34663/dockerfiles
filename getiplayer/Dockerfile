# docker build -t getiplayer .
# docker run --rm -v /home/philk:/home/philk latest --profile-dir=/home/philk "Doctor"
# docker run --rm -v /home/philk:/home/philk latest --profile-dir=/home/philk --get 2208 --output=/home/philk/Video
FROM centos:latest

RUN yum -y install epel-release && yum -y update
RUN yum -y install perl perl-LWP-Protocol-https.noarch perl-XML-LibXML.x86_64 perl-Env.noarch git\
 perl-JSON-PP.noarch perl-Mojolicious.noarch perl-Time-Piece.x86_64

RUN rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-1.el7.nux.noarch.rpm
RUN git clone https://github.com/get-iplayer/get_iplayer
RUN yum -y install ffmpeg.x86_64 AtomicParsley.x86_64
ENTRYPOINT ["/get_iplayer/get_iplayer"]
