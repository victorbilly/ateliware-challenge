# ateliware-challenge

Aplicação Dockerizada com Django e Postgres, Gunicorn, and Nginx (dois branchs um com servidor Nginx (Main) e outro sem)


*Para rodar esta aplicação*
A aplicação possui dois arquivos dockers, um para ambiente de desenvolvimento e outro para ambiente de produção

*Antes de rodar você deve configurar os arquivos de variáveis de ambiente: .env .en.prod e .env.bd*
*Para rodar em ambiente de desenvolvimento*

* sudo docker-compose up -d --build
Após rodar comando para criar as migrações da base de dados
* 

Para criar um usuário Admin para a Área Administrativa
sudo docker-compose -f docker-compose.prod.yml exec web python3 manage.py createsuperuser
