FROM jenkins/jnlp-slave

USER root

ENV DOCKERVERSION=18.06.3-ce
RUN curl -fsSLO https://download.docker.com/linux/static/stable/x86_64/docker-${DOCKERVERSION}.tgz \
  && tar xzvf docker-${DOCKERVERSION}.tgz --strip 1 \
                 -C /usr/local/bin docker/docker \
  && rm docker-${DOCKERVERSION}.tgz \
  && curl -fsSLO https://github.com/openshift/source-to-image/releases/download/v1.1.14/source-to-image-v1.1.14-874754de-linux-amd64.tar.gz \
  && tar xzvf source-to-image-v1.1.14-874754de-linux-amd64.tar.gz -C /usr/local/bin \
  && rm source-to-image-v1.1.14-874754de-linux-amd64.tar.gz


