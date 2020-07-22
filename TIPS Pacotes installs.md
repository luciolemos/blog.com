INSTALANDO BITNAMI LAMPSTACK
luciolemos@dell:~$ cd Downloads
luciolemos@dell:~/Downloads$ sudo chmod 755 bitnami-lampstack-7.4.8-0-linux-x64-installer.run
luciolemos@dell:~/Downloads$ sudo ./bitnami-lampstack-7.4.8-0-linux-x64-installer.run
==============================================================================================================================================
NOVA INSTALAÇÃO DO XAMPP
luciolemos@dell:~/Downloads$ sudo chmod 755 xampp-linux-x64-7.4.8-0-installer.run
luciolemos@dell:~/Downloads$ sudo ./xampp-linux-x64-7.4.8-0-installer.run
STARTANDO O XAMPP VIA CLI
luciolemos@dell:~$ cd /opt/lampp
luciolemos@dell:/opt/lampp$ sudo ./manager-linux-x64.run
==============================================================================================================================================
BAIXANDO E INSTALANDO O GOOGLE CHROME
luciolemos@dell:~$ wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
luciolemos@dell:~$ sudo apt install ./google-chrome-stable_current_amd64.deb
==============================================================================================================================================
INSTALAÇÃO DO XAMPP
luciolemos@dell:~$ cd Downloads                                                  /* Entrando no diretório Downloads
luciolemos@dell:~/Downloads$ ls                                                  /* listando o conteúdo do diretório Downloads
- xampp-linux-x64-7.4.8-0-installer.run
luciolemos@dell:~/Downloads$ sudo ./xampp-linux-x64-7.4.8-0-installer.run        /* Instalando
[sudo] senha para luciolemos: 
==============================================================================================================================================
INSTALAÇÃO DO COMPOSER (https://getcomposer.org/download/)
luciolemos@dell:~$ sudo php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"     
luciolemos@dell:~$ sudo php -r "if (hash_file('sha384', 'composer-setup.php') === 'e5325b19b381bfd88ce90a5ddb7823406b2a38cff6bb704b0acc289a09c8128d4a8ce2bbafcd1fcbdc38666422fe2806') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
luciolemos@dell:~$ sudo php composer-setup.php --install-dir=/bin --filename=composer
All settings correct for using Composer
Downloading...
Composer (version 1.10.9) successfully installed to: /bin/composer
Use it: php /bin/composer
==============================================================================================================================================
INSTALANDO O LARAVEL VIA COMPOSER, CONFIGURANDO A VARIÁVEL $PATH, EDITANDO O ARQUIVO "bashrc" E CRIANDO O PROJETO "blog" (https://www.youtube.com/watch?v=OQCzVonb34w).
luciolemos@dell:~$ composer global require laravel/installer /*INSTALAÇÃO GLOBAL DO LARAVEL
luciolemos@dell:~$ cd .config/composer/vendor/bin            /*MUDANDO (cd) PARA A PASTA DE INSTALAÇÃO DO LARAVEL
luciolemos@dell:~/.config/composer/vendor/bin$               /*DENTRO DA PASATA         
luciolemos@dell:~/.config/composer/vendor/bin$ ./laravel     /*DE DENTRO DA PASTA VERIFICANDO A VERSÃO DO INSTALADOR E OUTRAS INFORMAÇÕES  
Laravel Installer 3.2.0

Usage:
  command [options] [arguments]

Options:
  -h, --help            Display this help message
  -q, --quiet           Do not output any message
  -V, --version         Display this application version
      --ansi            Force ANSI output
      --no-ansi         Disable ANSI output
  -n, --no-interaction  Do not ask any interactive question
  -v|vv|vvv, --verbose  Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug

Available commands:
  help  Displays help for a command
  list  Lists commands
  new   Create a new Laravel application
luciolemos@dell:~/.config/composer/vendor/bin$ 
luciolemos@dell:~$ export PATH="$HOME/.config/composer/vendor/bin:$PATH" /*CONFIGURAÇÃO DA VARIÁVEL $PATH
luciolemos@dell:~$ sudo nano .bashrc                                     /*EDITANDO O "bashrc" COM O EDITOR NANO 
luciolemos@dell:~$ laravel new blog                                      /*CRIANDO O PROJETO LARAVEL "blog"
luciolemos@dell:~$ ls                                                    /*LISTANDO (ls) OS ARQUIVOS/DIRETÓRIOS NA HOME
'Área de Trabalho'   blog   composer-setup.php   Documentos   Downloads   Imagens   Modelos   Música   Público   Vídeos
luciolemos@dell:~$ cd blog
luciolemos@dell:~/blog$ php artisan serve
Laravel development server started: http://127.0.0.1:8000
[Mon Jul 20 20:05:01 2020] PHP 7.4.3 Development Server (http://127.0.0.1:8000) started
==============================================================================================================================================
INSTALANDO EXTENSÕES NO PHP
luciolemos@dell:~$ sudo apt-get install php-mbstring
luciolemos@dell:~$ sudo apt-get install php-xml
luciolemos@dell:~$ sudo apt-get install curl
==============================================================================================================================================
VERIFICANDO O CONTEÚDO DA VARIÁVEL $PATH
luciolemos@dell:~$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games
luciolemos@dell:~$ 
==============================================================================================================================================
INSTALAÇÃO E CONFIGURAÇÃO DO XDEBUG 2.9.6
luciolemos@dell:~/Downloads$ tar -xvzf xdebug-2.9.6.tgz                                   /* Descompactando o xdebug
luciolemos@dell:~/Downloads$ ls                                                           /* Listando os arquivos em Downloads
- google-chrome-stable_current_amd64.deb
- package.xml  
- xampp-linux-x64-7.4.8-0-installer.run  
- xdebug-2.9.6  
- xdebug-2.9.6.tgz
luciolemos@dell:~/Downloads$ cd xdebug-2.9.6                                              /* Entrando na pasta do xdebug-2.9.6
luciolemos@dell:~/Downloads/xdebug-2.9.6$ sudo apt-get install php-dev autoconf automake  /* Instalando o xdebug
luciolemos@dell:~/Downloads/xdebug-2.9.6$ phpize                                          /* verificando a instalação do xdebug
- Configuring for:
- PHP Api Version:         20190902
- Zend Module Api No:      20190902
- Zend Extension Api No:   320190902
luciolemos@dell:~/Downloads/xdebug-2.9.6$ ./configure                                     /* Configurando o xdebug
luciolemos@dell:~/Downloads/xdebug-2.9.6$ make                                            /* Criando os módulos
luciolemos@dell:~/Downloads/xdebug-2.9.6$ sudo cp modules/xdebug.so /opt/lampp/lib/php/extensions/no-debug-non-zts-20190902
==============================================================================================================================================
MARIADB VIA TERMINAL
luciolemos@dell:~$ sudo /opt/lampp/bin/mysql -u root -p
Enter password: # Não tem senha.
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 15
Server version: 10.4.13-MariaDB Source distribution
Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.
Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.
MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| test               |
+--------------------+
5 rows in set (0.001 sec)
MariaDB [(none)]> 
==============================================================================================================================================
INSTALAÇÃO DO "lxqt-sudo", PARA ADICIONAR PROGRAMAS AOS MENUS
luciolemos@dell:~$ sudo apt-get install lxqt-sudo
[sudo] senha para luciolemos:  
==============================================================================================================================================
INSTALANDO O GIT (https://git-scm.com/download/linux)
CONFIGURANDO O GIT (https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Configura%C3%A7%C3%A3o-Inicial-do-Git)
luciolemos@dell:~$ git config --global user.email luciolemos.j5@gmail.com
luciolemos@dell:~$ git config --global user.name "luciolemos"
luciolemos@dell:~$ git config --global core.editor xed
luciolemos@dell:~$ git config --list
user.email=luciolemos.j5@gmail.com
user.name=luciolemos
core.editor=xed
luciolemos@dell:~$ 

PACOTES INSTALADOS
1. Instalação do Google Chrome; Sublime Text 3.2.2; XAMPP e ativando extensões em /opt/lampp/etc/php.ini; xdebug-2.9.6 e atualizando o php.ini do XAMPP; Composer; PHPStorm; Laravel; Spotify; Git, lxqt-sudo.
==============================================================================================================================================
