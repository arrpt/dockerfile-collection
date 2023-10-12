FROM --platform=amd64 rust:latest
RUN sudo apt update&& sudo apt upgrade
RUN apt install -y git
RUN curl https://sh.rustup.rs -sSf | sh
#RUN apt install -y openssh-server
#RUN mkdir /var/run/sshd
#RUN echo "root:root" | chpasswd
#RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
#EXPOSE 22
RUN apt clean && rm -rf /var/lib/apt/lists/*
#CMD ["/usr/sbin/sshd", "-D"]