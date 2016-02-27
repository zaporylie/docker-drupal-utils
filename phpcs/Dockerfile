FROM drupaldocker/php:cli
MAINTAINER drupal-docker <info@drupaldocker.org>

ADD run.sh .phpcs.yml /root/

RUN DEBIAN_FRONTEND=noninteractive apt-get update \
  && apt-get -yq install shunit2 curl git \
  && composer global require drupal/coder \
  && chmod +x /tmp/phpcs.sh \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

ENV PHPCS_CONFIG_FILE=".phpcs.yml" \
 DEBUG=FALSE

CMD ["/root/phpcs.sh"]
