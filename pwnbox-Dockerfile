FROM amd64/ubuntu
RUN apt update && apt upgrade -y && apt install locales -y
RUN sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
    locale-gen
ENV LC_ALL en_US.UTF-8 
ENV LANG en_US.UTF-8  
ENV LANGUAGE en_US:en 
RUN apt install gdb gcc-multilib python3 python3-pip git fish curl wget ltrace strace neovim valgrind -y
RUN pip3 install pwn
RUN git clone https://github.com/pwndbg/pwndbg && cd pwndbg && ./setup.sh && echo 'source /pwndbg/gdbinit.py' > ~/.gdbinit.py && cd /
RUN version=$(curl -s https://api.github.com/repos/radareorg/radare2/releases/latest | grep -P '"tag_name": "(.*)"' -o| awk '{print $2}' | awk -F"\"" '{print $2}') && \
    wget https://github.com/radareorg/radare2/releases/download/${version}/radare2_${version}_amd64.deb && \
    dpkg -i radare2_${version}_amd64.deb && rm radare2_${version}_amd64.deb
RUN apt clean && rm -rf /var/lib/apt/lists/*
RUN pip3 cache purge
ENTRYPOINT ["/usr/bin/fish"]