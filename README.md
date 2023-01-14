# Comandos úteis para desenvolvedores

## lsof -i tcp:27017

<h4>Obs.: Utilizei quando a porta do docker local bloqueava subir o docker-compose.</h4>

> <p>
    lsof -i tcp:27017
  </p>

> O comando lsof (listar arquivos abertos) retorna os processos do usuário que estão usando ativamente um sistema de arquivos . Às vezes, é  útil determinar por que um sistema de arquivos permanece em uso e não pode ser desmontado.

## docker-compose up -d
>
> <p>
    docker-compose up -d
 </p>

> O comando docker-compose up -d é para subir o docker-compose e o -d manter ativo na máquina.

## docker-compose down
>
> <p>
    docker-compose down
 </p>

> O comando docker-compose down é para baixar o docker-compose
