# php8-apache-docker
Ambiente de desenvolvimento PHP 8 + JIT habilitado, Apache, SGBD MySQL 8 e Adminer

**Pré-requisitos:** Ter o Docker e Docker-compose instalados.


[Instalando Docker no Windows 10](https://mundodacomputacaointegral.blogspot.com/2019/10/instalando-o-docker-no-windows.html)

[Instalando Docker e Docker-compose no Linux (qualquer distro)](https://mundodacomputacaointegral.blogspot.com/2019/10/instalando-docker-e-docker-compose-no-Linux.html)

Após ter instalado o Docker e Docker-compose, segue os procedimentos: 

1. Fork do repositório

2. Clonar o repositório forkado

3. Acessar o diretório onde salvou o clone do repositório

4. Execute `docker-compose up -d`

O diretório src do HOST é o volume mapeado no diretório /var/www/html do CONTAINER. Então, é no diretório src que deve salvar os arquivos .php.

No browser http://localhost/info.php e veja o JIT e outras extensões habilitadas do PHP.

Acessar a ferramenta web para gerenciar o banco de dados no SGBD MySQL, acesse http://localhost:8080 as credencias de acesso, encontra-se no arquivo docker-compose.yml

Feito!
