# Vagrant 虚拟环境管理

# 1. 如何安装

## 1.1 安装 Virtualbox

http://www.virtualbox.org

## 1.2 安装 Vagrant

https://developer.hashicorp.com/vagrant/downloads?product_intent=vagrant

# 2. 快速开始

* 启动 dotnet 构建环境

```
cd dotnet-build
vagrant up
vagrant ssh
```

* 启动 docker 构建环境

```
cd docker-build
vagrant up
upgrant ssh
```

# 3. 如何使用

## 3.1 初始化配置

* 初始化新的配置

```
mkdir xxx
cd xxx
vagrant init
```

## 3.2 初始化虚拟机

```
vagrant up
```

## 3.3 进入虚拟机

```
vagrant ssh
```

## 3.4 释放虚拟机

```
vagrant destory
```

## 3.5 更多帮助

```
vagrant help
```
