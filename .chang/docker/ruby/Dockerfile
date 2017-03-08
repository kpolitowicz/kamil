FROM ruby:2.3.3-slim

ENV APP_UID=1000

RUN groupadd --gid $APP_UID app \
  && useradd --uid $APP_UID --gid app --shell /bin/bash --create-home app

RUN apt-get update \
  && apt-get upgrade -y --fix-missing \
  && apt-get install -y \
    build-essential \
    git \
    libmysqlclient-dev \
    nodejs \
    libmagic1 \
    libmagic-dev \
    imagemagick \
    libmagickwand-dev \
    libicu-dev \
    libqtwebkit-dev \
    gstreamer1.0-plugins-base \
    gstreamer1.0-tools \
    gstreamer1.0-x \
    mysql-client \
    default-jre \
    curl \
  && apt-get autoremove \
  && apt-get clean

RUN curl --retry 3 http://download.gna.org/wkhtmltopdf/0.12/0.12.0/wkhtmltox-linux-i386_0.12.0-03c001d.tar.xz | tar -C /tmp --extract -J \
  && cp /tmp/wkhtmltox/bin/wkhtmltopdf /usr/bin \
  && rm -rf /tmp/wkhtmltox

RUN gem install bundler benchmark-ips

CMD bash