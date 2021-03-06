# GLPI com Docker compose

Este repositório com o docker compose necessário para executar o GLPI através de **Docker** em sua ultima versão.

## Procedimento
```bash
sudo apt install git
```

### Instalando o docker:

```bash
curl -fsSL https://get.docker.com | sh
```

### Instalando do docker-compose

```bash
curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-Linux-x86_64" -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose
```

### Criando diretório para presistencia de dados e baixando o repositório

```bash
mkdir opt

cd /opt 

git clone https://github.com/adrianoazevedo/glpi_docker.git

cd glpi_docker 

mkdir -p ./var/www/html/glpi \
         ./var/lib/mysql

chown 472:472 ./var/lib/mysql \
              ./var/lib/mysql 
```

### Executando os containers

```bash
docker-compose up -d
```
Para acesar o **GLPI** acesse http://<seu_ip> **OU** `http://localhost`
 
### Configurando GLPI

```bash
host: mysql
usuario: glpi
senha: glpi
```

### GLPI

```bash
usuario: glpi
senha: glpi
```
### Os usuários e senhas padrões são:

```bash
-glpi/glpi para a conta do usuário administrador
-tech/tech para a conta do usuário técnico
-normal/normal para a conta do usuário normal
-post-only/postonly para a conta do usuário postonly
```
