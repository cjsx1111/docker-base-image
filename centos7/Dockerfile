FROM centos:7
RUN sed -e 's|^mirrorlist=|#mirrorlist=|g' \
        -e 's|^#baseurl=http://mirror.centos.org|baseurl=https://mirrors.bfsu.edu.cn|g' \
        -i.bak \
        /etc/yum.repos.d/CentOS-*.repo \
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
ENV LANG en_US.utf8
