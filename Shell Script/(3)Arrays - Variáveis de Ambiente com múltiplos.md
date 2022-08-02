# Arrays - Variáveis de Ambiente com múltiplos valores

Variáveis de ambiente podem ser usadas com arrays - variáveis que podem armazenar múltiplos valores de um mesmo tipo. Para configurar um array, liste os seus valores entre parênteses: 

testearray=(laranja morango acerola abacaxi)

Para acessar um elemento no array, use seu número de índice (entre colchetes) contando a partir de zero (todo o conjunto entre chaves):

echo ${testearray[1]}

morango

Para mostrar todo conteúdo do array, use o asterisco * no lugar do índice:

echo ${testearray[*]}

Alterar valores de uma posição específica:

testearray[2]=banana

Remover intens individuais:

unset testearray[2]

Remover o array todo:

unset testearray[*]