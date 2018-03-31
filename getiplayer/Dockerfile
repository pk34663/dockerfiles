FROM centos:latest

RUN yum -y install perl perl-LWP-Protocol-https.noarch perl-XML-LibXML.x86_64 perl-Env.noarch git 
RUN yum -y install epel-release

RUN git clone https://github.com/get-iplayer/get_iplayer
ENTRYPOINT ["/get_iplayer/get_iplayer"]
