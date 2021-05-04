<a href="https://codeclimate.com/github/PauloVitorRocha/Trabalho-Individual-2020-2/maintainability"><img src="https://api.codeclimate.com/v1/badges/22ee924a4896fc0ae056/maintainability" /></a>
# Trabalho Individual 2020.2

| Nome | Matrícula |
| ---- | --------- |
| Paulo Vítor Coelho da Rocha | 17/0062465 |

# 1. Containerização
Foi criado um Dockerfile para cada aplicação, um dentro da pasta /api e o outro na pasta /client

O container do banco de dados é criado diretamente no arquivo docker-compose.yml utilizando a imagem do postgres13.

# 2. Integração contínua
A integração continua foi feita por meio da utilização da ferramenta TravisCI onde foi criado um arquivo chamado .travis.yml, e esse arquivo é responsável por realizar duas tarefas:
  - Rodar os testes da api e verificar se o código está de acordo com as recomendações do flake8;
  - Rodar os testes do client e verificar se o código está de acordo com as recomendações do eslint;

A coleta de métricas foi feita com a ferramenta CodeClimate e podemos ver a sua badge no topo do README onde está escrito Maintainability A.

E podemos ve-los em funcionamento ao tentar fazer um Pull Request com código ¨ruim¨:
![image](https://user-images.githubusercontent.com/37215459/116953963-0033c800-ac65-11eb-92c6-ad446b3a1647.png)
onde houve falha na build na hora de verificar se o código respeita o flake8 através do TravisCI, e também há indicação de que o código inserido tem o fluxo de controle muito aninhado através do CodeClimate

# 3. Rodando
Para dar início à aplicação primeiro precisamos clonar o repositório com o comando:
``` 
git clone https://github.com/PauloVitorRocha/Trabalho-Individual-2020-2.git
```
Em seguida, para dar início à aplicação em execução em ambiente docker, basta entrar na pasta raiz do projeto com o comando:
``` 
cd Trabalho-Individual-2020-2
```
e executar o comando:
``` 
docker-compose up --build
```
se houver algum problema de permissão rode utilizando o comando:
``` 
sudo docker-compose up --build
```
O resultado deve ser esse só que com detalhes sobre as migrações da api
![image](https://user-images.githubusercontent.com/37215459/116953562-fc537600-ac63-11eb-90a3-fc5c3864014e.png)

