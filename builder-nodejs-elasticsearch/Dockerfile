FROM gcr.io/jenkinsxio/builder-jx:2.0.1140-472

RUN yum install -y java-1.8.0-openjdk-devel && yum clean all

COPY ./elasticsearch-init.sh /

RUN curl -f --silent --location https://rpm.nodesource.com/setup_12.x | bash - && \
  yum install -y sudo nodejs gcc-c++ make bzip2 GConf2 gtk2 chromedriver chromium xorg-x11-server-Xvfb

# Yarn
ENV YARN_VERSION 1.3.2
RUN curl -f -L -o /tmp/yarn.tgz https://github.com/yarnpkg/yarn/releases/download/v${YARN_VERSION}/yarn-v${YARN_VERSION}.tar.gz && \	
	tar xf /tmp/yarn.tgz && \
	mv yarn-v${YARN_VERSION} /opt/yarn && \
	ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn

# Install elasticsearch
RUN wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-6.5.4.tar.gz && \
		tar -xzf elasticsearch-6.5.4.tar.gz && \
		mv ./elasticsearch-6.5.4 /
		

