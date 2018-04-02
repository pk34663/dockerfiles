# docker build -t getiplayer .
# docker run --rm -it -v /home/<user> getiplayer --get ".*"
# docker run --rm -it -v /home/philk:/home/philk getiplayer --pid=p05td9zp --output=/home/philk/Video
FROM centos:latest

RUN yum -y install epel-release && yum -y update
RUN yum -y install perl perl-LWP-Protocol-https.noarch perl-XML-LibXML.x86_64 perl-Env.noarch git\
 perl-JSON-PP.noarch perl-Mojolicious.noarch 

RUN rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-1.el7.nux.noarch.rpm
RUN git clone https://github.com/get-iplayer/get_iplayer
RUN yum -y install ffmpeg.x86_64 AtomicParsley.x86_64
ENTRYPOINT ["/get_iplayer/get_iplayer"]
