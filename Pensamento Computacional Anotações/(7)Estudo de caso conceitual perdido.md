# Estudo de caso conceitual: perdido

Supondo que tem uma pessoa perdida na floresta, como utilizar o pensamento computacional para maximizar as chances de sobrevivência dele?

Primeiro precisamos identificar:

- Os mecanismos;
- Recursos comuns;
- Os detalhes mais importantes.

Decompondo o problema de Sobrevivência:

- Água
    - Chuva
        - Recipiente
        - Fogo (para purificar) *
    - Nascente
        - Recipiente
        - Fogo (para purificar) *
- Comida
    - Coletar
        - Fogo *
    - Caçar
        - Fogo *
        - Lança
- Abrigo
    - Proteção
        - Fogo *
        - Lança
    - Quente e seco
        - Fogo *
    - Localização
        - Mapa (pode ser criado por abstração focando nos aspectos principais)

Com isso ja utilizamos:

- Decomposição: dividindo o problema em vários subproblemas;
- Reconhecimento de padrões: onde o fogo (*) é o “objeto” mais presente entre os subproblemas;
- Abstração: para a construção do mapa.

Próximo passo seria o preparo de comida, exemplo:

- Pegar o peixe
- Colocar água em algum recipiente
- Fazer uma fogueira
- Ferver a água
- Limpar o peixe
- Fazer o cozido na panela
- Assar o peixe

E com isso cobrimos a parte de algoritmo, e utilizaremos algo semelhante na resolução dos outros problemas.