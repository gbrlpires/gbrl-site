---
title: "Comandos Linux que sempre preciso mas sempre esqueço"
date: 2022-08-31T17:19:19-03:00
draft: false
tags:
 - tecnologia
 - linux
---

### Atualiza Repositórios/Instala atualizações
```
sudo apt-get update
apt-get upgrade
```

### Deleta kernels não usados
Uso esse especialmente para o PopOS

```
apt autoremove
dpkg --list | grep linux-image
sudo apt remove --purge linux-image-[versão]-generic
```

Obs. Das últimas vezes usar o Synaptic teve um resultado melhor pra visualizar o que não estava sendo usado

### Deleta kernels não usados (via Synaptic)
1. Abrir Synaptic
2. Recarregar informações dos pacotes (botão Reload/Recarregar)
3. Pesquisar por 'linux-image'
4. Com o botão direito, escolher a opção 'Marcar para remoção completa' os kernels não utilizados
5. Aplicar as alterações

### Erro no apt-upgrade ("dpkg: error processing package libglib2.0-0:i386")
```
sudo dpkg --configure -a
sudo apt --fix-broken install
```
