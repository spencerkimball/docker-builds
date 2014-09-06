FROM ubuntu:14.04

MAINTAINER Spencer Kimball <spencer.kimball@gmail.com>

RUN apt-get update -y -qq
RUN apt-get dist-upgrade -y -qq
RUN apt-get install -y -qq dnsmasq-base dnsutils
ADD dnsmasq.conf /etc/dnsmasq.conf
ADD resolv.dnsmasq.conf /etc/resolv.dnsmasq.conf

VOLUME [ "/dnsmasq.hosts" ]

CMD ["/usr/sbin/dnsmasq", "-d"]
