echo -> Repete o que for escrito

clear -> limpa a tela

echo $variavel -> indica onde está essa variavel

pwd -> indica qual pasta estamos atualmente

cd -> change directory, mudar de pasta

ls -> lista conteudos de arquivos e diretorios na pasta atual

cd .. -> volta 1 diretorio pra cima

./arquivo -> abre o arquivo dentro da pasta que estamos

NOME_VARIAVEL = nome -> declara uma var local NOME_VARIAVEL com valor = nome

export NOME_VARIAVEL -> transforma a var local em var global

export VARIAVEL=valor -> ja cria ela exportada

cat -> mostra o conteudo de um arquivo de texto

set -> Lista todas as variaveis sejam locais ou globais

env -> Lista apenas as variaveis globais (pois é um programa externo)

unset NOME_VARIAVEL -> remove a variavel

HISTFILE -> Variavel que armazena o historico de comandos do bash

HISTFILESIZE -> tamanho maximo do arquivo

HISTSIZE -> quantidade de linhas maxima do arquivo

HOME -> mostra a home do usuario local

HOSTNAME -> mostra o nome do computador

LOGNAME ou USER -> nome do usuario que fiz login nessa sessão

PATH -> mostra os arquivos que contem os atalhos que podem ser usados no terminal

SHELL -> Indica qual shell está sendo utilizado

TERM -> Indica qual terminal esta sendo usado (xterm=GUI; tty=CLI direto)

echo $$ -> Mostra o PID do shell atual

echo $! -> Mostra o PID do último processo aberto em background

echo $? -> Mostra o código de retorno do último processo executado (0 = OK, !0 = erro)

echo ~ -> Mostra o HOME do usuário atual

echo ~usuario -> Mostra o HOME do usuário usuario

cd ~ -> Vai para o HOME do usuario atual

comando1 ; comando 2 ; comando3 -> executa os 3 comandos em sequência

comando1 && comando 2 -> executa o comando1 e se for sucesso, executa o comando2

comando1 || comando 2 -> executa o comando1 e se for falha, executa o comando2

!! -> repete o último comando digitado

!n -> repete o comando n do history

!string -> repete o ultimo comando que tenha essa string

history -c -> limpa o history
