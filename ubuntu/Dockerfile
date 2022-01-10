FROM ubuntu:latest
RUN apt update && apt install ca-certificates -y \
    && echo -n '' > /etc/apt/sources.list \
    && echo \
      'deb https://mirrors.bfsu.edu.cn/ubuntu/ focal main restricted universe multiverse\n'\
      '# deb-src https://mirrors.bfsu.edu.cn/ubuntu/ focal main restricted universe multiverse\n'\
      'deb https://mirrors.bfsu.edu.cn/ubuntu/ focal-updates main restricted universe multiverse\n'\
      '# deb-src https://mirrors.bfsu.edu.cn/ubuntu/ focal-updates main restricted universe multiverse\n'\
      'deb https://mirrors.bfsu.edu.cn/ubuntu/ focal-backports main restricted universe multiverse\n'\
      '# deb-src https://mirrors.bfsu.edu.cn/ubuntu/ focal-backports main restricted universe multiverse\n'\
      'deb https://mirrors.bfsu.edu.cn/ubuntu/ focal-security main restricted universe multiverse\n'\
      '# deb-src https://mirrors.bfsu.edu.cn/ubuntu/ focal-security main restricted universe multiverse\n'\
       >> /etc/apt/sources.list \
    && apt update \
    && apt install -y locales && rm -rf /var/lib/apt/lists/* \
    && localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 \
    && apt update && DEBIAN_FRONTEND=noninteractive apt -y install tzdata \
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && dpkg-reconfigure --frontend noninteractive tzdata 
ENV LANG en_US.utf8
