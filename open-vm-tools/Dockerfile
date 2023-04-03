FROM debian:bullseye

RUN apt-get update -y && apt-get install -y open-vm-tools && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Required for a graceful shutdown and ifup etc are missing
RUN rm /etc/vmware-tools/scripts/vmware/network

# TODO
# To properly shutdown we need systemctl to talk to the host

CMD ["/usr/bin/vmtoolsd"]
