FROM public.ecr.aws/docker/library/docker:dind AS dind

ARG PASSWORD=""

RUN apk add openssh-server python3
RUN ssh-keygen -A
RUN  yes "${PASSWORD}" | head -n 2 | passwd

COPY ./sshd_config /etc/ssh/sshd_config

RUN apk add py3-pip

ENTRYPOINT ["/bin/sh", "-c", "/usr/sbin/sshd && /usr/local/bin/dockerd-entrypoint.sh"]
