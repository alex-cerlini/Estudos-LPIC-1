## 103-1:

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

atalho ctrl+r string -> pesquisa o history de comandos em live time

apertar o tab 2x -> mostra o autocomplete do comando

man comando -> mostra o manual do comando

quando o comando é interno não tem manual foi faz parte do bash então man bash para ver

info comando -> perto de um man reduzido

man -k "string" -> busca comandos que tenham a string

apropos "string" -> busca comandos que tenham a string

whatis comando -> o que é esse comando

comando --help -> ótimo para explorar possibilidades do comando

uname -> fala do linux (versão, arquitetura..)

alias -> atalhos:

alias atalho='uname -a" -> executa uname -a quando digitar atalho (temporariamente)

which comando -> localiza onde está o comando

echo \* -> imprime na tela tudo o que está na pasta atual

echo '\*' -> imprime \* na tela (funciona com aspas duplas também)

echo '\\\*' -> imprime \\\*

echo "\\\*" -> imprime \*

---

## 103-2:

cat arquivo -> mostra o conteudo de um arquivo de texto

tac arquivo -> inverso de cat, mostra o conteudo da ultima linha ate a primeira

head arquivo -> mostra as primeiras 10 linhas do arquivo (cabeçalho)

tail arquivo -> mostra as ultimas 10 linhas do arquivo (footer)

less arquivo -> abre arquivo longo podendo scrollar o prompt com seta do teclado ( /palavra ele busca depois de ter dado o comando less)

wc arquivo -> conta a quantidade: linhas, palavras e bytes

nl arquivo -> enumera as linhas do arquivo sem considerar as linhas em branco

sort arquivo -> ordena o arquivo em ordem alfabetico

sort -r arquivo -> ordena o arquivo em ordem alfabetica reversa

sort -k2 arquivo -> ordena o arquivo em ordem alfabetica pelo segunda palavra da linha

uniq arquivo -> junta duas linhas seguidas

sort arquivo | uniq -> ordena em ordem alfabetica e depois retira todos os registros duplicados

od arquivo -> imprime o arquivo em octais

join arquivo1 arquivo2 -> junta os dois arquivos (linha de 1 junta na mesma linha do outro pelo indice)

paste arquivo1 arquivo2 -> soma os dois arquivos em um só (linha de 1 adiciona na linha do outro)

split -l15 arquivo -> divide o arquivo em arquivos de 15 linhas

split -l15 arquivo novo_arquivo\_ -> divide o arquivo em arquivos nomeados novo arquivo_xx de 15 linhas

split -b100 arquivo -> divide o arquivo em arquivos de 100 bytes

cat arquivo.txt | tr a-z A-Z -> pega o arquivo.txt e transformar todas as letras minusculas em maiusculas

cat arquivo.txt | tr ei EI -> pega o arquivo.txt e transformar todos os e em E e todos os i em I

cat arquivo.txt | tr [:upper:] [:lower:] -> pega o arquivo.txt e transformar tudo que ta maiusculo em minusculo

cat arquivo.txt | tr -d A -> pega o arquivo.txt e deleta todos os A

cat arquivo.txt | tr -d [:blank:] -> pega o arquivo.txt e deleta tudo que é espaço em branco

cut -c-5 arquivo.txt -> mostra os 5 primeiros caracteres de cada linha

cut -c5- arquivo.txt -> mostra a partir do quinto caractere em diante de cada linha

sed 's/Palavra1/Palavra2/' arquivo.txt -> Troca a primeira Palavra1 por Palavra2 por linha do arquivo

sed 's/Palavra1/Palavra2/g' arquivo.txt -> Troca todas as Palavra1 por Palavra2 por linha do arquivo (global)

sed '3,5 d' arquivo.txt -> apaga a linha 3 a 5

sed '/Claudia/d' arquivo.txt -> Apaga

echo "Curso de liiiiiiinux" | tr -s i -> remove todos os i repetidos e mantem só 1 (saída seria: Curso de linux)

tr -d "\r" < ArquivoGeradoWindows.txt > NovoArquivo -> tira o modo windows de pular linha (CRLF)

xzcat arquivo.txt.xz -> Mostra o conteudo sem descompactar

bzcat arquivo.txt.bz2 -> Mostra o conteúdo sem descompactar

zcat arquivo.txt.gz -> Mostra o conteúdo sem descompactar
