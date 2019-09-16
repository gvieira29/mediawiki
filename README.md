# INSTALAÇÃO DO MEDIAWIKI

O MediaWiki é um modelo de Wiki *Open Source*
Voce pode conferir o [Site Oficial clicando aqui](https://www.mediawiki.org/wiki/MediaWiki).


## COFIGURAR SERVIDOR WEB

Vamos configurar nosso servidor web em um Ubuntu 18.04.  
Você pode baixar a imagem que utilizamos clicando no [link para baixar](https://www.mediawiki.org/wiki/Download).  
Siga este passo a passo para fazer a instalação.  

Com o servidor ubuntu já instalado, é hora de configurarmos.  

1. Vamos instalar o OpenSSH.  
```
# apt-get install openssh-server
```
2. Baixar o pacote LAMP (Linux, Apache, MySQL,PHP).  

    Voce pode baixar um pacote completo utilizando o comando `# apt install -y lamp-server^`, mas aqui vamos instalar todos os pacotes separadamente.  
    1. Para instalar o Apache, utilize o comando
    ```
    # apt install -y apache2 
    ```
    Após instalar o Apache, você pode ir para o *localhost*, deverá exibir uma página como o da imagem abaixo, para comprovar que esta funcionando corretamente.

    [imagem]

    1. Instalar o PHP, vamos utilizar os pacotes: `libapache2-mod-php`, `php`, `php-cli`, `php-common`, `php-gd`, `php-intl`, `php-mbstring`, `php-pear`, `php-xml`, `php-zip`. Para instalar todos de uma vez, utilize o comando:
    ```
    apt install -y libapache2-mod-php php php-cli php-common php-gd php-intl php-mbstring php-pear php-xml php-zip
    ```
    1. Antes de fazer alguma modificação ou irmos para um teste, é necessário alterar as permissões do diretório `/var/www`, para isso, ainda em modo super usuário, insira o comando:
    ```
    # chmod 777 /var/www
    ```
    1. Instalar o Banco de dados, vamos utilizar MySQL
    ```
    # apt install -y mysql-client php-mysql mysql-server  
    ```

## GUIA MEDIAWIKI PASSO A PASSO

1. Devemos ter o `lamp-server`, um conjunto de ferramentas que ira criar nosso servidor web.  
L - Linux  
A - Apache  
M - MySQL (ou MariaDB)  
P - PHP (ou Python)



## ITALAÇAO DO MEDIAWIKI

1. Baixe o arquivo do site oficial https://www.mediawiki.org/wiki/MediaWiki, vamos utilizar o comando `wget` para baixar o pacote. 

wget https://releases.wikimedia.org/mediawiki/1.33/mediawiki-1.33.0.tar.gz

2. Para descompactar o arquivo utilize o `tar`.  

tar -xf mediawiki-1.33.0.tar.gz

3. 