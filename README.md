# INSTALAÇÃO DO MEDIAWIKI

O MediaWiki é um modelo de Wiki OpenSource

## MONTANDO SERVIDOR WEB

Para fazer a instalação da Wiki, vamos configurar um servidor web (caso não tenha ainda). Siga estas etapas  

- Voce pode instalar o pacote LAMP, que  pode ser feito através do comando `# apt install -y lamp-server^`, mas este guia ira mostrar como baixar os pacotes separadamente
  ```
  # apt install -y lamp-server^
  ```

- Instalar o apache.  
  ```
  # apt install -y apache2
  ```
  Pronto, o apache esta instalado.  
  Agora dê acesso ao diretório utilizando:  
  ```
  # chmod 777 /var/www
  ```

- Instalar o PHP.    
  ```
  # apt install -y libapache2-mod-php php php-cli php-common php-gd php-intl php-mbstring php-pear php-xml php-zip
  ```
  Para verificar se está funcionando corretamente, crie uma pagina de teste:  
  ```
  echo "<?php phpinfo(); ?>" >> teste.php
  cp teste.php /var/www/html
  service apache2 restart
  ```
  Agora acesse localhost/teste.php ou 127.0.0.1/teste.php para verificar a página que criamos.  

- Instalar o Banco de Dados, vamos utilizar o MySQL, também pode ser usado MariaDB para este projeto.  
  ```
  # apt install -y mysql-client mysql-server php-mysql
  ```
  Com o MySQL Instalado, crie o primeiro banco, abra o MySQL:
  ```
  # mysql
  ```
  Para verificar 