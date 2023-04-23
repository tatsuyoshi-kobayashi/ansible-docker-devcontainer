FROM public.ecr.aws/ubuntu/ubuntu:22.10_stable

RUN apt update
RUN apt install -y ansible ansible-lint

COPY ./local_hosts /etc/ansible/hosts

ENV ANSIBLE_HOST_KEY_CHECKING false
ENV LANG C.UTF-8
