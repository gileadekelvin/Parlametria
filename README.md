# Parlametria

Inteligência de dados para ação cidadã.

## Requisitos

* node 10.15.x
* [angular cli](https://github.com/angular/angular-cli) 8.3.15

## Como desenvolver (sem )

Primeiro, instale as dependências do projeto com `npm install`.

O comando `npm start` irá subir um servidor em modo de desenvolvimento. Navegue até `http://localhost:4200/` para ver. O aplicativo vai recarregar automaticamente quando houverem mudanças no código fonte.

## Como implementar

O comando `npm run build` irá preparar o aplicativo para implantação no servidor de produção. Os arquivos necessários serão gerados no diretório `dist/`.

## Rodando testes

O comando `npm run test` executa testes de unidade via [Karma](https://karma-runner.github.io).
O comando `npm run e2e` executa testes de integração via [Protractor](http://www.protractortest.org/).

## Usando docker

Para iniciar o desenvolvimento do projeto com docker basta levantar o serviço do frontend:

```
docker-compose up
```

**Observação importante**
Sempre que uma nova dependência for adicionada ao projeto é preciso refazer o build da imagem com o node. Para isto basta executar:

Lembre-se de parar o serviço em execução: `docker stop parlametria_frontend_1` ou `docker stop <id_container>`. <id_container> pode ser obtido pelo comando `docker ps`.

```
docker-compose build
```

## Comandos úteis

Caso você queira parar os containers e remover os volumes execute:

```
docker-compose down --volumes
```

Para visualizar os containers em execução:

```
docker ps
```

Para executar comandos num shell dentro do container:

```
docker exec -it <id_container> sh
```

Para remover um container

```
docker rm <id_container>
```
