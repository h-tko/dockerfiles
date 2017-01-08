FROM ubuntu:16.10
MAINTAINER H-TKO

EXPOSE 80
EXPOSE 11122

ENTRYPOINT ["/bin/bash"]

Run apt-get update
Run apt-get install -y apt-utils ibus-mozc language-pack-ja
Run apt-get install -y vim nginx git wget curl tar sudo make gcc openssh-server
Run apt-get install -y software-properties-common
Run add-apt-repository -y ppa:tsuru/golang17
Run apt-get update
Run apt-get install -y golang
Run apt-get install -y nodejs npm

Run echo "export GOPATH=\$HOME/go" >> /etc/bashrc
Run echo "export GOROOT=/usr/local/go" >> /etc/bashrc
Run echo "export PATH=$PATH:\$GOROOT/bin:\$GOPATH/bin" >> /etc/bashrc

Run echo "export LANG='ja_JP.UTF-8'" >> /etc/bashrc
Run echo "export LANGUAGE='ja_JP.UTF-8'" >> /etc/bashrc

Run npm install -g webpack
