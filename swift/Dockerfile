FROM ubuntu:wily
MAINTAINER John Neyer <github@jneyer.com>

RUN apt-get update \
&& apt-get -y install curl clang libicu-dev libpython2.7-dev libxml2-dev \
&& cd /tmp \
&& curl https://swift.org/builds/swift-2.2.1-release/ubuntu1510/swift-2.2.1-RELEASE/swift-2.2.1-RELEASE-ubuntu15.10.tar.gz -o swift.tgz \
&& curl -q  https://swift.org/keys/all-keys.asc | gpg --import - \ 
&& curl https://swift.org/builds/swift-2.2.1-release/ubuntu1510/swift-2.2.1-RELEASE/swift-2.2.1-RELEASE-ubuntu15.10.tar.gz.sig -o swift.tgz.sig \
&& gpg --verify swift.tgz.sig \
&& tar zxvf swift.tgz \
&& mv swift*RELEASE*/usr /usr/local/swift \
&& ln -s /usr/local/swift/bin/* /usr/local/bin

