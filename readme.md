# Aplicativo Local Library em Django com MySQL.


## Projeto criado a partir do tutorial [The Local Library website](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Tutorial_local_library_website).

A aplicação cria um site para uso de uma biblioteca.
* É possível cadastrar usuários com diferentes permissões de acesso, inclusão de livros com diversas características, alteração de status de empréstimos, dentre outras várias funcionalidades.
* Alguns testes automatizados foram implementados para garantir o correto funcionamento da aplicação.

### Decidi implementar esse projeto com o banco de dados **MySQL**.
* Deve-se criar um banco de dados e um usuário com as devidas permissões:

 `CREATE DATABASE nome_do_banco_de_dados;`

 `CREATE USER 'djangouser'@'%' IDENTIFIED WITH mysql_native_password BY 'password';`
 
 `GRANT ALL ON blog_data.* TO 'djangouser'@'%';`
 
 `FLUSH PRIVILEGES;`
 
   * É necessário editar o arquivo de configuração:
 
 `sudo nano /etc/mysql/my.cnf`
 
 `[client]`

`database = nome_do_banco_de_dados`

`user = djangouser`

`password = password`

`default-character-set = utf8`


  * Após criar um virtual enviroment, basta rodar os seguintes comandos:

`pip3 install -r requirements.txt`

`python3 manage.py makemigrations`

`python3 manage.py migrate`

`python3 manage.py collectstatic`

`python3 manage.py test # Caso queria rodar os testes.`

`python3 manage.py createsuperuser`

`python3 manage.py runserver`


É possível consultar o repositório desde tutorial [aqui](https://github.com/mdn/django-locallibrary-tutorial).

***