# flipstone/playground-base
FROM 46fc21600df9

# install packages we will need
RUN apt-get update && \
    apt-get install -y \
    build-essential zlib1g-dev libssl-dev libreadline6-dev libyaml-dev wget

ADD Python-2.7.7.tgz /home/vagrant
RUN chown -R vagrant.vagrant /home/vagrant/Python-2.7.7

USER vagrant
RUN cd /home/vagrant/Python-2.7.7 && \
    ls /home/vagrant/ && \
    ./configure --prefix=/home/vagrant/ && \
    echo 'export PATH=$PATH:/home/vagrant/bin/' >> /home/vagrant/.bashrc && \
    sh && \
    make && \
    make altinstall

USER root

