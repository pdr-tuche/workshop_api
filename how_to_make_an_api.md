# Roadmap criar api python drf

1-Cria uma pasta vazia.
2- Cria um ambiente virtual (python -m venv venv)
3- Ativa a venv (.\venv\Scripts\activate.ps1)
4- baixar as coisas, o django rest (pip install djangorestframework)
5- Cria o projeto (django-admin startproject nomedapasta .)
6- Cria o app (python .\manage.py startapp nomedoapp)
7- Da um ls pra ver onde a pasta ta alocada no diretorio
8- Vai na settings coloca dentro da installedapps nome rest_framework e o nome do app(não esquecer da virgula)
9- fazer o python manage.py makemigrations e fazer o python manage.py migrate
10- python manage.py runserver
11- verificar no navegador se tem o foguetinho, se tiver, funcionou.
12- Criar dois arquivos no app, o serializers.py e o urls.py
13- Importar na models from django.db import models
14- Modificar a models para adicionar as classes e a tabela pra recolher os dados.
15- Vamos pro serializers, from rest_framework import serializers e from .models import modelo
16- Criamos as classes serializer para converter de python para json e vice versa (serializers.ModelSerializer):
   -dentro de uma classe serializer criar a classe Meta:
   -Colocar o modelo
   -Selecionar os fields
17- Criar as views e jogar o serializers dentro:
   -from rest_framework import viewsets
   -from .models import modelo
   -from .serializers import classeSerializer
   -adicionar as classes para puxar os objetos do modelo e transportar o serializer para viewset
18- ir para urls do app
   -from rest_framework import routers
   -from .views import classeviewset
   -Setar o router como DefaultRouter()
   -registra os routers das viewsets
   -urlpatterns = router.urls
19- ir para urls do projeto
   -importar o include
   -criar o path da urls criada no app
20- python manage.py makemigrations
   -python manage.py migrate
   -python manage.py runserver
21- Vai no navegador pra ver se houve mudança
   - /nomedeterminadonaurl
22- Testar os metodos.
23- Se der erro, Stackoverflow ou chatgpt.

>feito por: turma workshop backend imersao fabrica de software 2023.2 sala 2 =)