---
layout: wiki
title: Raspberry
categories: linux
description: ʹ����ݮ�ɴ�����������ָ��
keywords: keyword1, keyword2
---
## ����root�˻�

raspbianĬ���û���Ϊpi������Ϊraspberry����ʹ��raspi-config�޸Ĺ����룬��Ϊ�޸ĺ�����룩

Ĭ������£�root�û���δ���ã���û������

```
# �����µ�����

sudo passwd root

# ����root �˻�

su root

```
## ��Դ

### �鿴���汾
Ruby version 2.4.0 or higher, including all development headers (check your Ruby version using ruby -v)
RubyGems (check your Gems version using gem -v)
GCC and Make (check versions using gcc -v,g++ -v, and make -v)

### gem��Դ
gem sources -r https://rubygems.org/

gem sources -a https://gems.ruby-china.com/

�鿴gem Դ gem sources -l

### apt��Դ

����Դ
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak

sudo cp /etc/apt/sources.list.d/raspi.list /etc/apt/sources.list.d/raspi.list.bak

��Դ���ο��廪Դ https://mirror.tuna.tsinghua.edu.cn/help/raspbian/

�޸��������Դ��ִ���������

```
sudo nano /etc/apt/sources.list

# �༭ `/etc/apt/sources.list` �ļ���ɾ��ԭ�ļ��������ݣ�����������ȡ����

deb http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ buster main non-free contrib rpi

deb-src http://mirrors.tuna.tsinghua.edu.cn/raspbian/raspbian/ buster main non-free contrib rpi

```

�޸�ϵͳ����Դ��ִ���������

```
sudo nano /etc/apt/sources.list.d/raspi.list

# �༭ `/etc/apt/sources.list.d/raspi.list` �ļ���ɾ��ԭ�ļ��������ݣ�����������ȡ����
deb http://mirrors.tuna.tsinghua.edu.cn/raspberrypi/ buster main ui

```
ͬ������Դ��ִ���������

```
sudo apt-get update
```

## ��װjekyll

gem install jekyll