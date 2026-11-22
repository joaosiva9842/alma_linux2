FROM almalinux:9

RUN dnf -y install systemd sudo curl && \
    dnf clean all && \
    systemctl set-default multi-user.target

STOPSIGNAL SIGRTMIN+3
CMD ["/sbin/init"]
