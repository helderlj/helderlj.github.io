---
layout: post
title: "Anotações GIT"
date: 2022-06-02 12:00:00 -0300
categories: [git,cli,command-line]
tags: [git,cli,notes]
---

# Alguns comandos uteis de GIT que utilizo no dia a dia.
Comados uteis GIT para ser utilizados em qualquer projeto GIT.

## Iniciar repositorio local e subir para repositorio online (repositorio online ja deve estar criado)
```git
git init
git add .
git commit -m "Primeiro Commit"
git remote add origin https://github.com/usuario/new-repository.git
git branch -M main
git push -u origin main
```

# GIT FLOW

## Iniciando git flow localmente num projeto git (pode ser necessário instalar o flow)
```bash
git flow init
```

## Iniciando uma feature
```git
git flow feature start nome-da-feature
```
Codar e commitar normalmente
## Finalizando uma feature
```git
git flow feature finish nome-da-feature
```

## Releases
```git
git flow release start numero-da-versao
git flow release finish numero-da-versao
git checkout main
git pull
git push
```

## Hotfix/bugfix
```git
git flow hotfix start numero-do-hotfix (ex. 1.0.1)
code code + adds & commits
git flow hotfix finish numero-do-hotfix (ex. 1.0.1)
```
