# Arquivos de Configuração profile

Variáveis de ambiente, funções e aliases podem ser configurados automaticamente pelo bash com o uso de alguns arquivos de configurações, de modo a definir o ambiente operacional ao iniciar o sistema.

Cada arquivo de configuração tem um escopo e momento de uso definidos, e o arquivo usado depende do método usado para iniciar o bash. Há três formas de se iniciar o bash

- Como um shell de login padrão na inicialização;
- Como um sehll interativo que não é o shell de login;
- Como um shell não-interativo para rodar um script

Obs: (~) significa a pasta do usuário, exemplo: /home/nick42

| Arquivo | Uso |
| --- | --- |
| /etc/profile * | Arquivo de inicialização, executado durante o login e válido para todo sistema; contém variáveis de ambiente e programas de inicialização. |
| /etc;bashrc ou /etc/bash.bashrc | Arquivo de inicialização, válido para todo o sistema, executado pelo .bashrc do usuário para cada shell bash iniciado. Contém funções e aliases. |
| ~/.bash_profile | Se existir, será exectado após /etc/profile durante o login. |
| ~/.bash_login | Se o .bash_profile não existir, será executado automaticamente durante o login. |
| ~/.profile | Se nenhum dos dois anteriores existirem, será executado automaticamente no login. |
| ~/.bashrc * | Executado automaticamente quando o bash é iniciado interativamente. |
| ~/.inputrc | Contém variáveis de configurações do modo de operação do bash em relação ás teclas (vinculação). |
| ~/.bash_logout | Executado automaticamente no lougout. |

## Shell de Login

Quando nos logamos no sistema Linux, o shell bash é iniciado com um shell de login.

Esse shell procura por quatro arquivos de inicialização para processar seus comandos, na seguinte ordem?

/etc/profile

~/.bash_profile

~/.bash_login

~/.profile

## Shell Interativo

Quando o bash é iniciado como um shell interativo, ele não processa o arquivo /etc/profile; em vez disso, ele tenta executar o arquivo .bashrc no diretório do usuário atual. O arquivo .bashrc pode ser usado para o usuário insira aliases personalizados e funções de scripts pessoais.

Também executa o arquivo global /etc/bashrc ou /etc/bash.bashrc, o qual configura algumas variáveis de ambiente locais.

## Shell Não-Interativo

è o shell inciado para executar um script (sehll script).

Quando um shell é iniciado em modo não interativo, ele verifica a variável de ambiente BASH_ENV para descobrir se há comandos de inicialização a executar.

Por padrão, o valor desta variável não é configurado.

## RESUMÃO

Quando você se loga no sistema Linux, o shell bash acessa o arquivo de inicialização /etc/profile, e também os arquivos de inicialização locais do seu usário, presentes no diretório home: ~/.bash_login, ~/.bash_profile e ~/.profile

Esses arquivos locais são todos opcionais e podem ser personalizados pelo usuário para incluir variáveis de ambiente e scripts de inicialização.