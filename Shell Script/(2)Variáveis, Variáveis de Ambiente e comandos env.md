# Variáveis, Variáveis de Ambiente e comandos env, unset e echo

## Variáveis

Vários programas precisam de informações sobre o usário e suas preferências para poderem rodar. Para evitar que você tenha de passar esses dados a cada comando que executa (ex.: caminhos de diretórios de bibliotecas), o shell cria um ambiente operacional composto de iinúmeras variáveis.

Essas variáveis contém valores que são usados pelos programas e por outros shells.

Há dois tipos de variáveis de ambiente:

- Variáveis de ambiente globais;
- Variáveis do shell (locais).

### Variáveis de ambiente globais

Elas podem ser passadas a todos os subprocessos do shell, incluindo outros shells.

Exemplos:

- PATH - Lista de diretórios de programas executáveis
- USERNAME - Nome do usuário logado
- TERM - Tipo de terminal ou janela de terminal em uso
- HOME - Diretório home do usuário atual
- UID - UID do usuário atual
- RANDOM - Gera um número aleatório
- LANG - Idioma, epecificado como locale

Os comandos **env** e **printenv** mostram as variáveis de ambiente no terminal.

Para criar uma variável global, crie uma local e depois utilize o comando **export** sobre ela.

### Variáveis do Shell

São como “variáveis locais”, pois são específicas do shell atual. 

Outros programas e shells não as herdam.

**Exemplos**

- SECONDS - número de segundos desde que o shell foi iniciado;
- SHELL - Indica qual o shell em uso atualmente.

Podemos criar uma varável nova digitando um par NOME-valor no terminal: 

teste=10

E verificamos seu valor com o comando echo:

echo $teste

Podemos disponiblizar a variável criada para outros shells ou programas com o comando export:

export teste

E podemos remover uma variável de ambiente com o comando unset:

unset teste