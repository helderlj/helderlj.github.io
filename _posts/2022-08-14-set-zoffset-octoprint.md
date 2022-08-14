---
layout: post
title: "Configuração do Z-Offset Impressora 3D com BL-TOUCH e Octoprint"
date: 2022-08-14 11:00:00 -0300
categories: [3D,tecnico,command-line]
tags: [3dprinting,octopi,rpi]
---
![octoprint](https://octoprint.org/assets/img/octoprint-600x400.png)
# Configurar o Z-Offset da impressora com BL-Touch via Octoprint.

## Procedimento para configura a altura do bico em impressoras rodando bl-touch+octoprint

```
Resetar todos os eixos (home)
```

## Com os eixos resetados e Octoprint conectado, os comandos a seguir são executados no console:

___
Reseta o Z-Offset configurado atualmente
```
M851 Z0
```

Grava a alteração na EEPROM
```
M500
```

Seta os parametros como ativos
```
M501
```

Mostra os parametros ativos
```
M503
```

Reseta o eixo Z
```
G28 Z
```

Reseta o eixo Z
```
G28 Z
```

Move o bico para o Z-0 que estiver configurado no momento
```
G1 F60 Z0
```

Desliga o limite da mesa mover em sentido negativo (caso necessario)
```
M211 S0 -
```
___
> Através da interface do Octoprint, desça o bico lentamente e verifique a altura com uma folha de papel. O papel deve se mover com uma pequena resistencia.
**Anote** o valor do eixo Z exibido no display da impressora. Adicione -0.01 ao valor valor obtido (Ex. valor obtido: -1.30, o valor do offset deverá ser -1.31)
___


Substitua o valor aqui pelo resultado obtido
```
M851 Z-1.31
```

Religa o limite da mesa mover em sentido negativo (caso tenha sido desligado)
```
M211 S1
```

Grava a alteração na EEPROM
```
M500
```

Seta os parametros como ativos
```
M501
```

Mostra os parametros ativos
```
M503 - display current settings
```
___
## Feito
