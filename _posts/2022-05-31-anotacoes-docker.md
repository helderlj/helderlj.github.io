---
layout: post
title: "Anotações Docker"
date: 2022-05-31 19:10:00 -0300
categories: [docker,cli,wsl2]
tags: [docker,cli,wsl2,notes]
---

# Alguns comandos uteis de docker que utilizo no dia a dia.
Comandos geralmente utilizados no WLS do Windows, mas podem ser utilizados em qualquer Linux baseado em debian.

## Inicia serviço do docker no Linux
```bash
service docker start
```

## Mata todos os containers rodando dinamicamente
```bash
docker kill $(docker ps -q)
```

## Mata todos os containers rodando no linux com sudo (utilizado em servidor de produção)
```bash
sudo docker kill $(sudo docker ps -q)
```

## Remove o link entre as imagens e os containers
```bash
docker rm $(docker ps -a -q)
```

## Remove todas as imagens baixadas
```bash
docker rmi $(docker images -q)
```
---
# Config do arquvio .wslconfig localizado em "C:\Users\username"
```ini
[wsl2]
memory=8GB
processors=4
swap=2GB
```
