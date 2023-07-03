# Como instalar o Docker

- Baixe o Docker neste link: https://www.docker.com/products/docker-desktop
- Instale o Docker. A instalação é simples. O Docker Compose já será instalado juntamente.
- Apos instalar o Docker, é necessário instalar o WSL (Windows Subsystem for Linux). Para tanto, abra um terminal de linha de comando em modo administrativo e digite o comando abaixo:

```shell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

- Após o comando finalizar, reinicie o seu computador.
- Após o computador reiniciar, abra novamente um terminal de linha de comando em modo administrativo e digite o comando abaixo:

```shell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

- Reinicie o seu computador novamente.
- Após o computador reiniciar, provavelmente a mensagem abaixo irá aparecer para você:
  
```shell
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

- Para sanar este problema, faça o download do Kernel atualizado neste link: 

```shell
https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
```
- Instale o Kernel e então reinicie o seu computador.
- Após o computador reiniciar, abra novamente um terminal de linha de comando em modo administrativo e digite o comando abaixo:

- Após o computador reiniciar, abra novamente um terminal de linha de comando em modo administrativo e digite o comando abaixo:

```shell
wsl --set-default-version 2
```
- E pronto! Agora, teste o Docker e o Docker Compose para verificar se tudo está ok.

# Como instalar a image do MySQL

Obs: Para facilitar o aprendizado tenha as seguintes extensões instaladas no seu VSCode

1 - Database Cliente

2 - Docker

- Acesse o site do Docker Hub e pesquise por mysql, copie os seguintes códigos e jogue no terminal:
  
  ```shell
  docker pull mysql
  ```
  
  ```shell
   docker run --name nome -e MYSQL_ROOT_PASSWORD=suaSenha -p 3306:3306 -d mysql:versao
  ```

  - Agora o docker conseguirá fazer a conexão da porta da sua máquina para a porta do container do MySQL e você
  - Crie a conexão com o banco no database client e agora você poderá usar o MySQL dentro do container, sem ele estar instalado na sua máquina
 
<div align="center">
  <img src="https://cdn.discordapp.com/attachments/695042455724228638/1125549048837972100/image.png" width="700px" />
  <img src="https://cdn.discordapp.com/attachments/695042455724228638/1125549323212570705/image.png" width="700px" />
</div>
