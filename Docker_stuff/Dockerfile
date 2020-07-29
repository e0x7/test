FROM kalilinux/kali-bleeding-edge

ARG KALI_DESKTOP
RUN export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    apt-get install -y \
        curl sudo apt-transport-https gnupg \
        x11vnc xvfb novnc dbus-x11 \
        kali-defaults kali-desktop-${KALI_DESKTOP} && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
EXPOSE 5900/tcp 6080/tcp
ENV DISPLAY :1
ENV KALI_DESKTOP ${KALI_DESKTOP}


