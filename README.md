# Campeões da Copa do Mundo
## Análise de Agrupamentos (Clusters)



<div class="conteudo" style="border-box: none">
<p align="justify">
    Utilizando o trabalho de "Libertadores 2022 - Fase de Grupos" como inspiração, foi analisado o desempenho das seleções campeãs da Copa do Mundo.
Foi utilizado o método hierárquico de agrupamento, onde não é necessário saber o número de grupos. As variáveis utilizadas neste trabalho foram: Pontos Conquistados, Aproveitamento, Gols Feitos, Gols Sofridos, Apoio (Média de Público) e Fator Casa (se o campeão foi mandante).
</p> 

### Análise de Correlação

<div class="conteudo" style="border-box: none">
<p align="justify">
    Inicialmente, foi analisado a correlação entre as variáveis selecionadas. De cara, observa-se que há uma correlação positiva forte entre Gols Feitos e Gols Sofridos, isto é, Seleções que fazem muitos gols, sofrem muitos gols (Seleções com um jogo mais ofensivo). Seleções com maior Apoio do Público conquistam mais pontos (vencem mais).<br><br>
    Seleções da Casa possuem desempenho ofensivo menor e sofrem poucos gols. Por consequência (e obviedade), Seleções da Casa possuem maior Apoio do Público. Apoio do Público tem uma correlação positiva fraca com Gols Feitos, ou seja, quanto mais Gols Feitos, melhor o Aproveitamento.
</p> 

<div align="center">
<img src="https://user-images.githubusercontent.com/54998262/173140787-991852e6-3013-4e43-b0d5-3fdb36375057.png" width="400px" />
</div>

### Análise de Agrupamento   

<p align="justify">
    Posteriormente, foi aplicado a Distância Euclidiana para verificar a menor distância entre dois pontos, provada pelo Teorema de Pitagoras. A partir da Correlação Cofenética (mede o grau de preservação das distâncias emparelhadas pelo dendrograma resultante do agrupamento em relação às distâncias originais). Para este caso, a Ligação Média foi utilizada.
</p>     
    
### Observa-se 5 grupos com algumas particularidades:
<p align="justify">
Grupo 1: Alemanha de 1954, sendo a seleção campeã com maior média de Gols Feitos em uma única edição (25 Gols em 6 Jogos) e também a maior média de Gols Sofridos em uma única edição (14 Gols em 6 Jogos) - Inclusive uma das maiores goleadas sofridas pela Alemanha em Copas - 8x3 para a Hungria de Puskás.<br><br>
Grupo 2: Seleções que venceram a Copa como Mandante - Uruguai de 1930, Itália de 1934, Inglaterra de 1966, Alemanha de 1974, Argentina de 1978, e França de 1998.<br><br>
Grupo 3: É o grupo dos Bicampeões. Seleções experientes que tiveram um bom desempenho no bicampeonato.<br><br>
Grupo 4: É o grupo das Seleções que tiveram desempenho espetacular, sofrendo poucos gols, fazendo muitos gols (incluindo com Aproveitamento de 100% - Brasil de 1970 e 2002).<br><br>
Grupo 5: É o grupo das Seleções que tiveram desempenho conservador (times bem mais defensivos), que se notabilizaram por fazer poucos gols porém que também sofreram poucos gols (Espanha de 2010 é a seleção campeã com o pior ataque e a melhor defesa das Copas).
</p>
<div>
    
<div align="center">
<img src="https://user-images.githubusercontent.com/54998262/173144033-58de7d5d-0f89-48a5-b776-3881f0e1d942.png" width="600px" />
</div>

## Método K-means



<div class="conteudo" style="border-box: none">
<p align="justify">
    O agrupamento k-means é um método de segregar em torno de centros (centroides) diversos dados, criando o que analogamente na química chamamos de clustering que gera o efeito de particionar n observações dentre k grupos onde cada observação pertence ao grupo mais próximo da média. Isso resulta em uma divisão do espaço de dados em um Diagrama de Voronoi.
</p> 

### Definindo a quantidade de "k" grupos
    
<p align="justify">
    Foi determinado uma quantidade ótima de grupos a partir da largura média da silhueta. Na Figura, é possível observar que o número optimizado de Clusters determinado é de 6, entretanto, se utilizar 5 grupos, a distância não é grande, o que nos leva a selecionar esse número de "k".
</p>   
<div>
    
<div align="center">
<img src="https://user-images.githubusercontent.com/54998262/173145661-5afd447f-5878-4bc9-9cad-c88e68a2d892.png" width="500px" />
</div>

### Cluster Plot

### Observa-se 5 grupos com algumas particularidades:
<p align="justify">
Grupo 1: Grupo formado pelas Seleções Bicampeãs. Na Silhueta também é possível observar Argentina de 1986 e França de 2018 (pertencentes ao Grupo 4 e que foram bicampeãs nestas edições).<br><br>
Grupo 2: Seleções que venceram a Copa como Mandante - Uruguai de 1930, Itália de 1934, Inglaterra de 1966, Alemanha de 1974, Argentina de 1978, e França de 1998.<br><br>
Grupo 3: Alemanha de 1954, sendo a seleção campeã com maior média de Gols Feitos em uma única edição (25 Gols em 6 Jogos) e também a maior média de Gols Sofridos em uma única edição (14 Gols em 6 Jogos) - Inclusive uma das maiores goleadas sofridas pela Alemanha em Copas - 8x3 para a Hungria de Puskás.<br><br>
Grupo 4: É o grupo das Seleções que tiveram desempenho espetacular, sofrendo poucos gols, fazendo muitos gols (incluindo com Aproveitamento de 100% - Brasil de 1970 e 2002).<br><br>
Grupo 5: É o grupo das Seleções que tiveram desempenho conservador (times bem mais defensivos), que se notabilizaram por fazer poucos gols porém que também sofreram poucos gols (Espanha de 2010 é a seleção campeã com o pior ataque e a melhor defesa das Copas). Na Silhueta também é possível observar várias outras Seleções que tiveram desempenho mais conservador mas que pertencem aos outros grupos.
</p>
<div>
    
<div align="center">
<img src="https://user-images.githubusercontent.com/54998262/173146887-8b65e18e-9b92-45e1-80cd-c4827b528ba4.png" width="600px" />
</div>
