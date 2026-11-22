FROM almalinux:9

RUN dnf -y install systemd sudo
RUN dnf clean all
RUN id codespace >/dev/null 2>&1 || useradd -m -s /bin/bash codespace
RUN printf '%s\n' 'codespace ALL=(ALL) NOPASSWD:ALL' > /etc/sudoers.d/codespace
RUN chmod 0440 /etc/sudoers.d/codespace

STOPSIGNAL SIGRTMIN+3
CMD ["/sbin/init"]
