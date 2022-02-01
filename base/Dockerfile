FROM registry.access.redhat.com/ubi8/ubi:8.5-214

RUN dnf install python3 python3-pip sudo -y && \
    python3 -m pip install --upgrade pip && \
    python3 -m pip install pytest

CMD ["/bin/sh"]