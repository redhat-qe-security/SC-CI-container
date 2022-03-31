FROM quay.io/centos/centos:stream8

RUN dnf update -y --allowerasing --skip-broken --nobest && \
    dnf groupinstall "Smart Card Support" -y && \
    dnf install openssl python3 python3-pip sudo procps-ng sssd authselect policycoreutils -y && \
    python3 -m pip install --upgrade pip && \
    python3 -m pip install pytest coverage click pexpect pyyaml python-decouple python-freeipa cryptography coloredlogs fabric tox ; \
    echo "redhat" | passwd root --stdin

CMD ["/bin/sh"]
