# INSTALAÇÃO DO MEDIAWIKI

O MediaWiki é um modelo de Wiki OpenSource

## MONTANDO SERVIDOR WEB

Para fazer a instalação da Wiki, vamos configurar um servidor web (caso não tenha ainda). Siga estas etapas  

- Voce pode instalar o pacote LAMP, que  pode ser feito através do comando `# apt install -y lamp-server^`, mas este guia ira mostrar como baixar os pacotes separadamente
  ```bash
  # apt install -y lamp-server^
  ```
- Instalar o apache.  
  ```
  # apt install -y apache2
  ```
  Pronto, o apache esta instalado.  

- Instalar o PHP.    
  ```bash
  # apt install -y libapache2-mod-php php php-cli php-common php-gd php-intl php-mbstring php-pear php-xml php-zip
  ```
  Para verificar se está funcionando corretamente, crie uma pagina de teste:  
  ```bash
  echo "<?php phpinfo(); ?>" >> teste.php
  cp teste.php /var/www/html
  service apache2 restart
  ```

- Instalar o Banco de Dados, vamos utilizar o MySql, também pode ser usado MariaDB para este projeto.  