# Comandos úteis para desenvolvedores

<meta
name="viewport" content="width=device-width, initial-scale=1">

<link
  rel="stylesheet" href="./style.css"
>

<br
/>

<details>
  <summary> <strong
  class='center'
>mkdir nome-do-diretorio</strong></summary>


  <h4
> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Obs.: Nome do diretorio **não pode ter espaço** senão é gerado 2 diretórios, mais pode usar <strong>camelCase</strong> ou <strong>snack-case</strong>
</h4>

> <p
> >

    mkdir nome-do-diretorio

  </p>

> O comando mkdir gera diretório.

<br
/>
</details>
## lsof -i tcp:27017

<h4
>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Obs.: Utilizei quando, a porta do docker local, bloqueava subir o docker-compose.</h4>

> <p
> >

    lsof -i tcp:27017

  </p>

> O comando lsof (listar arquivos abertos) retorna os processos do usuário que estão usando ativamente um sistema de arquivos . Às vezes, é útil determinar por que um sistema de arquivos permanece em uso e não pode ser desmontado.

<br
/>

## docker ps -a

> <p
> >

    docker ps -a

 </p>

> O comando docker ps -a é para verificar os containers existentes na máquina -a é para verificar inclusive os inativos

<br
/>

## docker-compose up -d

> <p
> >

    docker-compose up -d

 </p>

> O comando docker-compose up -d é para subir o docker-compose e o -d manter ativo na máquina.

<br
/>

## docker exec -it [nome-do-container ou o código] bash

> <p
> >

    docker exec -it [nome-do-container ou o código] bash

 </p>

 <h4
 >
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Obs.: Para sair so digitar exit e clicar no enter.</h4>

> O comando docker exec -it [nome-do-container ou o código] bash  este comando vai executar o docker-compose e te deixar dentro do container no terminal bash

<br
/>

## docker-compose down

> <p
> >

    docker-compose down

 </p>

> O comando docker-compose down é para baixar o docker-compose

<br
/>
