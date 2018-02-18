[![Go Report Card](https://goreportcard.com/badge/github.com/henson/Hosts)](https://goreportcard.com/report/github.com/henson/Hosts)  [![Travis Status for henson/Hosts](https://travis-ci.org/henson/Hosts.svg?branch=master)](https://travis-ci.org/henson/Hosts)  [![GitHub release](https://img.shields.io/github/release/henson/Hosts.svg)](https://github.com/henson/Hosts/releases/tag/v1.0)

# Hosts
自动生成 Hosts 文件，科学上网

![](1947422058.jpg)

图题《取经》（作者：@青红造了个白 ，侵删！）

## 特别声明

本项目仅作技术学习之用，不鼓励、不支持也不赞成任何互联网违法违规行为，任何不当使用的行为概与本项目无关！！！

### 特点

- 自动生成 Hosts 文件
- 超快的响应速度
- 支持 Windows 和 Linux 系统

### 更新日志

- 2018.02.18
  - 添加配置文件
  - 支持 Windows 和 Linux
- 2018.02.10
  - 提升访问速度

### 目前可访问网站

|目标网站|响应时间|
|:------|------:|
|www.instagram.com|25.947 ms|
|www.tumblr.com|30.690 ms|
|www.flickr.com|4.871 ms|
|www.medium.com|5.111 ms|
|www.pinterest.com|28.895 ms|
|www.vimeo.com|4.893 ms|
|~~www.twitter.com~~|ip 被封|
|~~www.youtube.com~~|同上|
|~~www.facebook.com~~|同上|
|~~www.golang.org~~|同上|

本项目只能解决 DNS 被污染情况，并不能解除 IP 封印，所以并不是对所有网站都适用。欢迎大家提交 issue ，告知其它网站访问情况，以便更新。

## 使用方法

### 直接下载可执行文件

根据平台直接下载各版本运行文件： [releases](https://github.com/henson/Hosts/releases)

### 从源码编译本项目

```
go get -u github.com/henson/Hosts
```

### 程序运行

修改同目录下配置文件 config.yaml，添加相应的目标网站，以“ | ”符号分隔

```yml
# 目标网站
hosts: "www.instagram.com|www.tumblr.com|www.flickr.com|www.medium.com|www.pinterest.com"
```

使用前，先备份系统中的 hosts 文件

> Windows 系统下文件路径：
> 
> C:\Windows\System32\drivers\etc\hosts

> Linux 系统下文件路径：
> 
> /etc/hosts


然后运行主程序

```
go run hosts.go
```

或

```
go build

./Hosts
```

### 日常使用

在浏览器中使用 **Https** 来访问目标网站，为免 IP 修改或 DNS 被污染，建议每个月运行一下程序。
