# THE DOCKER WORKSHOP

#### by Vincent Sesto, Onur Yılmaz, Sathsara Sarathchandra, Aric Renzo e Engy Fouda


## Configurando o ambiente

Requerimentos

* CPU dual-core com suporte a virtualização;
* 4GB de memória RAM;
* 20GB de espaço em disco disponível;
* Ubuntu 20.04 LTS.

Os comandos aqui apresentados foram testados e executados no Ubuntu 20.04 LTS.

## Instalação e configuração

Atualizando o gerenciador de pacotes:

```bash
sudo apt update
sudo apt upgrade
```

Instalando o Git

```bash
 sudo apt install git-all
```

Instalando e configurando o Docker

```bash
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
docker -version
sudo usermod -aG docker ${USER}
reboot
```
