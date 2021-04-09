# centos5-vault

On March 31, 2017, support of CentOS 5 has ended.
And therefore, we cannot perform `yum` on CentOS 5 official images because yum repositories for CentOS 5 is deleted.
Since vault.centos.org forces https over tlsv3 which centos 511 doesn't support, use a pure http mirror that does not (yet) force https
This image rewrites yum repository urls in /etc/yum.repos.d to http://linuxsoft.cern.ch/centos-vault/5.11/
You can use this image as drop-in replacement of official `centos:5` (`centos:5.11`).
