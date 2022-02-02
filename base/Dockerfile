FROM quay.io/centos/centos:stream8

RUN dnf update -y && \
    dnf groupinstall "Smart Card Support" -y && \
    dnf install openssl python3 python3-pip sudo procps-ng sssd authselect -y && \
    python3 -m pip install --upgrade pip && \
    python3 -m pip install pytest && \
    echo "redhat" | passwd root --stdin \

CMD ["/bin/sh"]
