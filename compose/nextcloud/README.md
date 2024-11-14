Link do compose

https://github.com/docker/awesome-compose


https://github.com/docker/awesome-compose/tree/master/nextcloud-redis-mariadb

Se der erro de permissão no Banco de Dados:
Acesse o banco de dados:

Entre no banco de dados com um usuário que tenha permissões de administrador (como root para MySQL/MariaDB):


`mysql -u root -p`

Conceda permissões ao usuário:

`GRANT ALL PRIVILEGES ON nextcloud.* TO 'nextcloudfabio'@'%';`
`FLUSH PRIVILEGES;`

Esse comando concede todas as permissões ao usuário nextcloudfabio para o banco de dados nextcloud, permitindo que ele crie, altere e consulte dados conforme necessário.