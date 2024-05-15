# Especificação de Caso de Uso: Fase de Ataque Entre Territórios

## Caso de Uso: Atacar Território

### Descrição:

## Interesses e Interessados:
- **Jogador**: deseja conquistar territórios para alcançar o objetivo(s) que lhe foi atribuído.
- **Sistema de validação de jogada**: Quer garantir que as as ações realizadas durante um ataque entre territórios são válidas. Deseja analisar a conclusão de objetivos por meio da ocupação de territórios e eliminação de jogadores. 
- **Inicializador do Jogo**: Quer garantir que todos os jogadores tenham sido atribuídos com objetivos e tenham recebido territórios para poder iniciar uma fase de ataque entre territórios. Deseja garantir que um jogo foi concluído com a vitória de um dos jogadores para assim poder realizar a inicialização de um novo jogo.
- **Administrador de Combates**: Deseja emitir resultados de empates, vitórias e derrotas durante um ataque entre territórios. Quer garantir que os resultados obtidos sejam devidamente aplicados nos territórios dos jogadores.

## Pré-condições:
- Todos os jogadores possuem territórios ocupados com pelo menos um exército
- Todos os jogadores foram atribuídos com objetivo(s)
- O jogador realizou a fortificação de um território

## Fluxo de Eventos:
### Fluxo Básico:
1. Jogador anuncia território atacante
1. Sistema de validação de jogada verifica que jogador possui o território
1. Sistema de validação de jogada verifica que território possui mais de um exército
1. Jogador anuncia qual território será alvo do ataque
1. Sistema de validação de jogada verifica que território é ligado pela fronteira do território atacante
1. Jogador informa quantidade de exércitos utilizados no ataque
1. Sistema de validação de jogada verifica que quantidade de exércitos é maior ou igual a 1 ou menor ou igual a 3
1. Sistema de validação de jogada verifica que território alvo utiliza a capacidade máxima de exércitos para defesa de território
1. Sistema de administração de combate emite valores aleatórios para a quantidade de exércitos atacantes
1. Sistema de administração de combate emite valores aleatórios para a quantidade de exércitos defensores
1. Sistema de administração de combate faz o máximo de comparações com os maiores valores emitidos entre os territórios de ataque e defesa
1. Sistema de administração de combate calcula quantidade de vitórias, derrotas e empates 
1. Sistema de validação de jogada realiza a remoção de exércitos entre os territórios de ataque e defesa acordo com o número de vitórias, derrotas e empates
1. Sistema de validação de jogada verifica que objetivo do jogador ainda não foi concluído
1. Jogador repete passos 1 ao 6 ou finaliza a jogada

## Pós Condições:

## Regras de Negócio específicas:

- RNE001: O jogador não pode atacar um território não contiguo ou não conectado por fronteiras;
- RNE002: O jogador não pode atacar um território se o território atacante possuir apenas um exército;
- RNE003: O jogador pode utilizar no máximo três exércitos por ataque;
- RNE004: O jogador não pode atacar o prórprio território;
- RNE005: O jogador pode atacar a quantidade de vezes desejada durante uma rodada;
- RNE006: Caso ocorra um empate durante uma Batalha, a vitória é do lado defensor;
- RNE007: O jogador só pode realizar um ataque a partir da segunda rodada.
