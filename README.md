# Comandos úteis para desenvolvedores

<br
/>

## Abrir um terminal

> <p
> >

    ctrl + alt + t

  </p>

> Em qualquer momento só clicar as 3 teclas juntas o comando vai abrir um prompt de comando(mais conhecido como terminal).

<br
/>

## mkdir nome-do-diretorio

  <h4
>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Obs.: Nome do diretorio <strong>não pode ter espaço</strong> senão é gerado 2 diretórios, mais pode usar <strong>camelCase</strong> ou <strong>snack-case</strong>
</h4>

> <p
> >

    mkdir nome-do-diretorio

  </p>

> O comando mkdir gera diretório.

<br
/>

## Comando para corrigir teclado americano

  <h4
>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Obs.: Comando para corrigir teclado americano o meu Dell G-15
</h4>

> <p
> >

    setxkbmap -layout us -variant intl

  </p>

> Esse comando define o layout do teclado para o inglês dos EUA (us) com a variante internacional (intl). Esta variante permite digitar acentos e outros caracteres usados em português. Para digitar um acento, você pressiona a tecla do acento (como ' ou ~) e depois a letra a ser acentuada.

> Essa mudança é temporária e será revertida quando você reiniciar o sistema.

<br
/>

## Manter o comando anterior permanente

1. Abra o terminal.
2. Digite o comando abaixo, e pressione Enter. Isso abrirá o arquivo .bashrc(aqui pode ser bash ou ~/.xinitrc o que for padr~ao do sistema) no editor de texto nano.

> <p
> >

    nano ~/.bashrc

  </p>

3. Role até o final do arquivo e adicione a seguinte linha

> <p
> >

   setxkbmap -layout us -variant intl

  </p>

4. Pressione Ctrl + O para salvar o arquivo, em seguida, Ctrl + X para sair do nano.

> Após essas etapas, o comando será executado toda vez que você abrir um novo terminal, o que efetivamente tornará a alteração permanente.

> Porém, é importante notar que isso não mudará o layout do teclado para aplicativos que você inicia por meio do menu ou de um ícone, apenas para aplicativos que você inicia a partir do terminal.

<br
/>

## lsof -i tcp:27017

<h4
>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Obs.: Utilizei quando, a porta do docker local, bloqueava subir o docker-compose. [tcp:27017] - este comando esta referenciando a porta que o deocker estava utilizando </h4>

> <p
> >

    lsof -i tcp:27017

  </p>

> O comando lsof (listar arquivos abertos) retorna os processos do usuário que estão usando ativamente um sistema de arquivos . Às vezes, é útil determinar por que um sistema de arquivos permanece em uso e não pode ser desmontado.

<br
/>

## sudo kill -9 `sudo lsof -t -i:3001`

<h4
>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Obs.: Utilizei quando, a porta 3001 local, estava em uso e eu precisava liberar ele. Este comando mata o que esta rodando nela </h4>

> <p
> >

    sudo kill -9 `sudo lsof -t -i:3001`

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

## docker stop $(docker ps -a -q)

> <p
> >

    docker stop $(docker ps -a -q)

 </p>

> O comando docker stop $(docker ps -a -q) vai parar todos os containers da maquina (Full Completo), inclusive os que tiverem ocultos.

<br
/>

## docker rm $(docker ps -a -q)

> <p
> >

    docker rm $(docker ps -a -q)

 </p>

> O comando docker rm $(docker ps -a -q) vai remover todos os containers da maquina (Full Completo), inclusive os que tiverem ocultos. Porem as imagens que o container baixou na máquina ele não remove.

<br
/>

## docker volume prune

> <p
> >

    docker volume prune

 </p>

> O comando docker volume prune vai remover todos os volumes da maquina (Full Completo).

<br
/>

## docker rm -v container_name

> <p
> >

    docker rm -v container_name

 </p>

> O comando docker rm -v container_name vai remover 1 ou mais container por vez só acrescentar o nome do container o -v vai remover todos os volumes não nomeados.

<br
/>

## docker images -a

> <p
> >

    docker images -a

 </p>

> O comando docker images -a vai listar todas as imagens Docker.

<br
/>

## docker rmi $(docker images -a -q)

> <p
> >

    docker rmi $(docker images -a -q)

 </p>

> O comando docker rmi $(docker images -a -q) vai remover todas as imagens da maquina (Full Completo), inclusive as que tiverem ocultas.

<br
/>

## docker container inspect [CONTAINER_ID ou NAME]

> <p
> >

    docker container inspect [CONTAINER_ID ou NAME] 

 </p>

> O comando docker container inspect serve para fazer a inspeção completa de como o container foi criado, ele funciona tanto com ID do container como o nome do container

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

  <hr>
<br
/>
    
## docker system prune --all --volumes

> <p
> >


    docker system prune --all --volumes

 </p>

> O comando docker system prune --all --volumes é para <strong>REMOVER TUDO DE UMA SÓ VEZ</strong>
> <p> <strong>Este comando não deleta o docker-compose up. Ou seja os containers startados.</strong> </p>

<br
/>
