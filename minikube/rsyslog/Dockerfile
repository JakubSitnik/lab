FROM ubuntu:22.04

RUN  apt update && apt install -y rsyslog
COPY rsyslog.conf /etc

CMD ["rsyslogd", "-dn", "-i", "/tmp/test_$RANDOM.pid"]
