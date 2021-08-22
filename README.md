# opt-ant-colonies
Ant Colonies populational metaheuristic

Algoritmo Colônia de Formigas - Aplicado Ao Problema do Caixeiro Viajante

Video overview: https://www.youtube.com/watch?v=sDBe6R0axAY

Método de busca populacional
- Proposto por Dorigo et al. (1991)
- Simula o comportamento de um conjunto de agentes(formigas) que se cooperam para resolver um problema de otimização por meio de comunicações muito simples
- Ao deslocaram-se as formigas deixam um rastro (substância chamada feromônio), que é usado para comunicaram-se quimicamente

Rota das formigas ao encontrarem um alimento
![image](https://user-images.githubusercontent.com/22028539/130354928-dab1d9d0-5193-4b38-b3f2-df8a7d83e66a.png)



Pressuposto:
- Considerando o efeito da presença simultânea de muitas formigas, então cada uma contribuirá com um parte da distribuição de feromônio.
- Bons conjuntos de arcos serão utilizados por muitas formigas e, portanto, receberão uma quantidade maior de feromônio
- Aproximação para o modelo computacional:
- Formigas deixam o feromônio em cada arco visitado após chegar ao destino
- Na vida real, as formigas deixam o feromônio durante o movimento e não após chegar ao seu destino

- Funcionamento do método: superposição concorrente de m procedimentos usando uma única formiga

Cada formiga atua como segue:
1. Em cada passo a formiga escolhe uma cidade para mover-se dentre aquelas ainda não visitadas
2. A probabilidade de a formiga escolher o arco (i,j) é diretamente proporcional à quantidade ij de feromônio no arco (i,j) e inversamente ao comprimento dij do arco 
3. A probabilidade de a formiga k sair da cidade i em direção à cidade j é calculada como:
4. A formiga lembra-se de cada cidade já visitada
5. Após uma rota ser completada, a formiga deposita uma certa quantidade de feromônio (ij) em cada arco (i, j) da rota, formando uma trilha com rastros de feromônio
  - Para os arcos que não pertencem à rota ij = 0
6. Considera-se a evaporação de feromônio em cada arco (i, j), tomando-se um fator  de evaporação, com  < 1, dado por:

Tij <- (1 - p) x Tij + DELTATij

Procedure:
![image](https://user-images.githubusercontent.com/22028539/130355785-6fb42c5f-a6c7-45c8-8be5-dc23aa7c9174.png)

Considera-se um conjunto de m formigas, cada qual localizada em uma certa cidade

Formulation:

![image](https://user-images.githubusercontent.com/22028539/130355331-89877118-ad41-4e10-a9e7-7b216ff235ea.png)

Params:

![image](https://user-images.githubusercontent.com/22028539/130355344-301ab5a3-a766-4eaa-be6a-d8032a679fdd.png)

References:

- Canal Ponto Ótimo: https://www.youtube.com/channel/UCOOwrwblBTnfl7-Fl5_eTug
- UFOP Computational inteligence course: http://www3.decom.ufop.br/pos/pesquisa/otimizacao-e-inteligencia-computacional/
- Professor Marcone: http://decom.ufop.br/prof/marcone
- Professor Puca: http://decom.ufop.br/puca
