# comandos-linux
**Exemplos com base no Debian.**
Recomendação de Wiki - [Guia foca](https://www.guiafoca.org/)
## Básicos
- sudo apt update -- Verifica se existe atualizações no repo do linux utilizado.
- sudo apt upgrade -- Faz as atualizações encontradas.
- Pode ser executado mais de uma operação no mesmo comando utilizando o operador " && " -- exemplo: sudo apt update && sudo apt upgrade
- sudo adduser nmDoUsuario -- Adiciona um novo usuário.
- sudo login nmDoUsuario -- Loga no usuário desejado.
- useradd --help -- Caso não lembre como adicionar um novo usuário ( --help pode ser utilizados em outros comando para verificar como utiliza-los ).
- sudo usermod -a -G grupos nmDoUsuario -- Adiciona o usuario em determinado grupo.
- sudo apt install htop -- Instala a ferramenta htop para monitorar os recursos utilizados no servidor.
## Servidor e Banco de Dados (MySql)
- sudo apt install mariadb-server -- Instala o servidor do banco de dados MariaDB.
- sudo apt install php-mysql php-pdo -- Instala os conectores do banco no PHP.
- sudo service mariadb status -- Verifica o status do servidor.
- sudo service mariadb start -- Inicia o servidor.
- sudo service mariadb stop -- Para o servidor.
- sudo mysql -uroot -p -- Acessar o servidor.
### Criando um novo usuário
- CREATE USER 'senac@localhost' IDENTIFIED BY 'senac123';
- GRANT ALL PRIVILEGES ON * . * TO 'senac@localhost';
- FLUSH PRIVILEGES;
- exit
-----------
- mariadb -usenac -p -- Acessa o servidor do mariaDB com o usuário criado
- create database nomeDoBanco -- Cria um Banco de dados.
- use nomeDoBanco -- Marca para conseguir usar o banco criado.
- create table usuarios ( id int not null primary key auto_increment, login varchar(100) not null, nome varchar(100) not null, senha varchar(255) not null ); -- Cria uma tabela usuários.
- show tables -- Exibe as tabelas existentes no Banco.
