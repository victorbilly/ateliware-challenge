# ateliware-challenge

Aplicação Dockerizada com Django e Postgres, Gunicorn, and Nginx (dois branchs um com servidor Nginx (Main) e outro sem)

Para dockerizar ótimo artigo em 
http://github.com - automatic!

A aplicação possui dois arquivos dockers, sendo um para ambiente de desenvolvimento e outro para ambiente de produção

# Para rodar a aplicação

*Crie e configure inicialmente os arquivos de variáveis de ambiente conforme os exemplos gerando: .env .en.prod e .env.bd*

*Para rodar em ambiente de desenvolvimento*

`$ docker-compose up -d --build`
`$ docker-compose exec web python3 manage.py migrate` #para criar as migrações

E finalmente
`$ docker-compose up -d --build`

Estando a aplicação rodando em:

[http://127.0.0.1:8000](http://127.0.0.1:8000)

Após rodar comando para criar as migrações da base de dados
* 


sudo docker-compose -f docker-compose.prod.yml up -d --build
sudo docker-compose -f docker-compose.prod.yml exec web python3 manage.py migrate

Para criar um usuário Admin para a Área Administrativa
sudo docker-compose -f docker-compose.prod.yml exec web python3 manage.py createsuperuser
