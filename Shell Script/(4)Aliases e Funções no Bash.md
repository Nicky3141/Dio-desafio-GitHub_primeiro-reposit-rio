# Aliases e Funções no Bash

## Aliases

É possível definir um alias para um comando ou sequência de comandos usados com frequência.

alias mo=’more’

alias lshome=’cd /home; ls’

Também permite modificar o comportamento padrão de um comando.

alias lsl=’ls -l’

Para listar os aliases criados, digite **alias** sem parâmetros.

Por padrão, os aliases são locais ao shell e não são repassados a outros programas.

Para excluir um alias criado, use unalias nome_alias

## Funções

O bash também permite trabalhar com funções, que são parecidas com os aliases, mas em vez de comandos, temos pequenos programas.

Sintaxe:

nome_função() {comandos}

**Exemplo:**

palavra(){

>cd /home/nick42

>echo ‘Linha acrescentada’ >> teste_func

>}

### Obs:

Aliases e Funções criadas dessa forma ficam ativas enquanto o sistema estiver iniciado, assim que ele for desligado esses aliases e funções criadas serão excluidas, para criar funções e aliases permanentes é preciso usar outras ferramentas.