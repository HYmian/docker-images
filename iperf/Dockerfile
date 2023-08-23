FROM fedora:38

RUN dnf install -y iperf3 sysstat \
  	&& dnf clean all \
  	&& rm -rf /var/cache/yum

ENTRYPOINT ["iperf3"]
