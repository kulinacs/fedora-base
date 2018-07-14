FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    libssl-dev \
    openssh-client \
    sshpass \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install ansible==2.5

WORKDIR /tests

COPY . /tests

ENTRYPOINT ["ansible-playbook"]
CMD ["all.yml"]
