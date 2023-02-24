Centos 8
========
마지막 Centos 버전 이 위로는 centos stream 버전임

패키지 업데이트
---------------
```CentOS 8 패키지 에러
# yum upgrade -y
CentOS Linux 8 - AppStream                       34  B/s |  38  B     00:01
Error: Failed to download metadata for repo 'appstream': Cannot prepare internal mirrorlist: No URLs in mirrorlist

하기 root 사용자 권한으로 저장소 경로를 변경
sudo sed -i -e "s|mirrorlist=|#mirrorlist=|g" /etc/yum.repos.d/CentOS-*
sudo sed -i -e "s|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g" /etc/yum.repos.d/CentOS-*
```
# yum update

재부팅 해야함


ssh 설치
--------
yum install install openssh-server

Ubuntu 22.04 LTS
=================
우분투 장기지원하는 최신버전

패키지 업데이트
---------------

# apt-get update

ssh 설치
-------
apt-get install openssh-server
