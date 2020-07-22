VERSÃO DO INSTALADOR DO LARAVEL
luciolemos@dell:~$ laravel --version
Laravel Installer 3.2.0
===========================================================================================================

VERSÃO DO COMPOSER
luciolemos@dell:~$ composer --version
Composer version 1.10.9 2020-07-16 12:57:00
====================================================================================================================

VERSÃO DO PHP
luciolemos@dell:~$ php --version
PHP 7.4.3 (cli) (built: May 26 2020 12:24:22) ( NTS )
Copyright (c) The PHP Group
Zend Engine v3.4.0, Copyright (c) Zend Technologies
    with Zend OPcache v7.4.3, Copyright (c), by Zend Technologies
====================================================================================================================

CAMINHO DO WORKSPACE DO PHPSTORM
luciolemos@dell:~/Documentos/PhpStormProjects$ 
luciolemos@dell:~/Documentos/PhpStormProjects$ ls /*Listando os diretórios (projetos) dentro de "PhpStormprojects". 
blog.com  
Php_exercises  
site.com
luciolemos@dell:~/Documentos/PhpStormProjects$ cd blog.com /*Entrando (cd) no diretório do Projeto blog.com
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ 
===================================================================================================================

CRIANDO O PROJETO "exemplo_inst" A PARTIR DO INSTALADOR DO LARAVEL (o arquivo .env é gerado normalmente).
luciolemos@dell:~/Documentos/PhpStormProjects$ laravel new exemplo_inst
===================================================================================================================

CRIANDO O PROJETO "exemplo_composer" VIA COMPOSER (o arquivo .env é gerado normalmente).
luciolemos@dell:~/Documentos/PhpStormProjects$ composer create-project --prefer-dist laravel/laravel exemplo_composer
===================================================================================================================

LISTANDO COMANDOS E VERIFICANDO A VERSÃO DO LARAVEL INSTALADA
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan list
Laravel Framework 7.20.0
===================================================================================================================

LIMPANDO O CACHE
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan config:cache
Configuration cache cleared!
Configuration cached successfully!
===================================================================================================================

INDICANDO QUAL O BANCO DE DADOS DEVE SER POVOADO.
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan db:seed --database=blog
Database seeding completed successfully.
===================================================================================================================

CRIANDO UMA MIGRATION
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan make:migration create_pessoal_table --create=pessoal
Created Migration: 2020_07_21_113455_create_pessoal_table
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ 
===================================================================================================================

EXECUTANDO A CRIAÇÃO DAS MIGRATIONS PRESENTES EM "batabase/migrations".
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan migrate
Migration table created successfully.
Migrating: 2014_10_12_000000_create_users_table
Migrated:  2014_10_12_000000_create_users_table (0.59 seconds)
Migrating: 2019_08_19_000000_create_failed_jobs_table
Migrated:  2019_08_19_000000_create_failed_jobs_table (0.26 seconds)
Migrating: 2020_07_21_113455_create_pessoal_table
Migrated:  2020_07_21_113455_create_pessoal_table (0.51 seconds)
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ 
===================================================================================================================

EXECUTANDO O RESET NO BANCO DE DADOS DAS MIGRATIONS CRIADAS.
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan migrate:reset
Rolling back: 2020_07_21_113455_create_pessoal_table
Rolled back:  2020_07_21_113455_create_pessoal_table (0.36 seconds)
Rolling back: 2019_08_19_000000_create_failed_jobs_table
Rolled back:  2019_08_19_000000_create_failed_jobs_table (0.23 seconds)
Rolling back: 2014_10_12_000000_create_users_table
Rolled back:  2014_10_12_000000_create_users_table (0.24 seconds)
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ 
===================================================================================================================
EXECUTANDO O REFRESH NO BANCO DE DADOS (o comando desfaz -rollback- AS MIGRATIONS E TORNA A CRIÁ-LAS.
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan migrate:refresh
Rolling back: 2020_07_21_113455_create_pessoal_table
Rolled back:  2020_07_21_113455_create_pessoal_table (0.61 seconds)
Rolling back: 2019_08_19_000000_create_failed_jobs_table
Rolled back:  2019_08_19_000000_create_failed_jobs_table (0.21 seconds)
Rolling back: 2014_10_12_000000_create_users_table
Rolled back:  2014_10_12_000000_create_users_table (0.36 seconds)
Migrating: 2014_10_12_000000_create_users_table
Migrated:  2014_10_12_000000_create_users_table (0.94 seconds)
Migrating: 2019_08_19_000000_create_failed_jobs_table
Migrated:  2019_08_19_000000_create_failed_jobs_table (0.29 seconds)
Migrating: 2020_07_21_113455_create_pessoal_table
Migrated:  2020_07_21_113455_create_pessoal_table (0.27 seconds)
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ 
===================================================================================================================

USADO PARA CRIAR O ARQUIVO DE MIGRIÇÃO DA TABELA USERS
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan make:migration create_users_table
Created Migration: 2020_06_26_032955_create_users_table
===================================================================================================================

USADO PARA IMPLEMENTAR NOVA COLUNA À ESTRUTURA DA TABELA PESSOAL
luciolemos@dell:~/Documentos/PhpStormProjects/blog.com$ php artisan make:migration add_votes_to_pessoal_table --table=pessoal
===================================================================================================================

Voltando para o diretório "www", onde será criado o projeto "spima".
C:\wamp\www\site.com>cd ..

Linha de comando para a criação do projeto "spima", dentro de "www".
C:\wamp\www>laravel new spima

Executando p projeto "spima", no vscode.
C:\wamp\www\spima>code .
C:\wamp\www\spima>

C:\wamp\www\site.com>php artisan serve
Laravel development server started: http://127.0.0.1:8000
[Thu Jun 25 12:24:13 2020] PHP 7.4.0 Development Server (http://127.0.0.1:8000) started






