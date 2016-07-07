FROM ubuntu:wily
MAINTAINER John Neyer <github@jneyer.com>

RUN apt-get update \
&& apt-get -y install curl clang libicu-dev libpython2.7-dev libxml2-dev \
&& cd /tmp \
&& curl https://swift.org/builds/development/ubuntu1510/swift-DEVELOPMENT-SNAPSHOT-2016-06-20-a/swift-DEVELOPMENT-SNAPSHOT-2016-06-20-a-ubuntu15.10.tar.gz -o swift.tgz \
&& curl -q https://swift.org/keys/all-keys.asc | gpg --import - \ 
&& curl https://swift.org/builds/development/ubuntu1510/swift-DEVELOPMENT-SNAPSHOT-2016-06-20-a/swift-DEVELOPMENT-SNAPSHOT-2016-06-20-a-ubuntu15.10.tar.gz.sig -o swift.tgz.sig \
&& gpg --verify swift.tgz.sig \
&& tar zxvf swift.tgz \
&& mv swift*DEVELOPMENT*/usr /usr/local/swift \
&& ln -s /usr/local/swift/bin/* /usr/local/bin

