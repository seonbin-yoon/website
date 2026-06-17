FROM golang:1.26

ARG USERNAME=docker
ARG PASSWORD=docker

RUN apt-get update \
    && useradd -m -d /home/${USERNAME} -s /bin/bash ${USERNAME} \
    && echo "${USERNAME}:${PASSWORD}" | chpasswd \
    && sed -i 's/^#force_color_prompt=yes/force_color_prompt=yes/' /home/${USERNAME}/.bashrc \
    && chown -R ${USERNAME}:${USERNAME} /home/${USERNAME}

WORKDIR /home/${USERNAME}/app

COPY --chown=${USERNAME}:${USERNAME} . .

USER ${USERNAME}

EXPOSE 8080