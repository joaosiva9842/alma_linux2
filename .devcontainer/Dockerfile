FROM almalinux:9

RUN dnf -y install systemd sudo curl && \
    dnf clean all && \
    useradd -m -s /bin/bash codespace && \
    echo "codespace ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/codespace && \
    chmod 0440 /etc/sudoers.d/codespace

STOPSIGNAL SIGRTMIN+3
CMD ["/sbin/init"]
