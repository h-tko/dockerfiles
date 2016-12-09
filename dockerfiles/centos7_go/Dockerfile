FROM centos:centos7
MAINTAINER H-TKO

EXPOSE 8080
EXPOSE 3000

ENTRYPOINT ["/bin/bash"]

Run yum -y update
Run yum -y install vim nginx git wget curl tar sudo
Run yum -y install epel-release
Run yum -y install nodejs npm

Run wget https://download.postgresql.org/pub/repos/yum/9.6/redhat/rhel-6-x86_64/pgdg-centos96-9.6-3.noarch.rpm -P /usr/local/src/
Run rpm -ivh /usr/local/src/pgdg-centos96-9.6-3.noarch.rpm
Run yum -y install postgresql96-server postgresql96-devel postgresql96-contrib

Run wget https://storage.googleapis.com/golang/go1.7.4.linux-amd64.tar.gz -P /usr/local/src/
Run tar xvfz /usr/local/src/go1.7.4.linux-amd64.tar.gz -C /usr/local/

Run echo "export GOPATH=\$HOME/go" >> /etc/bashrc
Run echo "export GOROOT=/usr/local/go" >> /etc/bashrc
Run echo "export PATH=$PATH:\$GOROOT/bin:\$GOPATH/bin" >> /etc/bashrc

Run npm install -g webpack
