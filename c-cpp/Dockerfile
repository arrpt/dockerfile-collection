FROM --platform=amd64 gcc
RUN apt update && apt upgrade -y
#RUN apt install -y openssh-server
#RUN mkdir /var/run/sshd
#RUN echo "root:root" | chpasswd
#RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
#EXPOSE 22
#CMD ["/usr/sbin/sshd", "-D"]
RUN apt clean && rm -rf /var/lib/apt/lists/*