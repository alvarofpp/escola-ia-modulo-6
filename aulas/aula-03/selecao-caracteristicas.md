# Seleção de variáveis

Nessa etapa do treinamento, devemos descobrir e/ou decidir quais dados são mais importantes para o treinamento do nosso modelo.

Algo que devemos nos atentar para não confundir é a diferença entre seleção de características e redução de dimensionalidade:

- **Seleção de características**: selecionar e excluir dados (características) sem modificá-las.
- **Redução de dimensionalidade**: transformar os dados (características) em uma dimensão menor.

Antes de entrarmos nesses tópicos, vamos entender melhor o que é variável.

## Variável
Variável pode ser entendida como qualquer quantidade, qualidade, magnitude... de uma característica que pode possuir vários valores numéricos.

### Tipos de variáveis
Os diferentes tipos de variáveis:

- **Qualitativa**: seus valores não são numéricos, mas sim determinadas características.
  - **Dicotômicas**: variáveis que podem assumir apenas dois valores.
- **Quantitativa**: seus valores são dados em números.
  - **Contínuas**: variável que pode assumir qualquer valor dentro de um intervalo.
  - **Discretas**: variável que assume valores geralmente inteiros.

Caso de variáveis **binárias**: 0 (ausência da característica) ou 1 (presença da característica).

### Níveis de mensuração das variáveis
Existem níveis crescentes de mensuração, sendo eles, em ordem crescente:

- **Nominal**: valores não numéricos e não ordenados.
  - Exemplo: cor e modelo do carro.
- **Ordinal**: valores não numéricos e ordenados. Uma instância pode apresentar valor comparativamente maior do que uma outra.
  - Exemplo: faixa etária.
- **Intervalar**: valores numéricos. Existe uma ordem entre os valores e também uma diferença entre esses valores.
  - Exemplo: temperatura.
- **Proporcional** ou **Razão**: valores numéricos. Além da diferença, tem sentido calcular a proporção entre valores (zero é absoluto).
  - Exemplo: peso, altura, etc.

## Seleção de características
Consiste em selecionar as características mais relevantes para o nosso modelo.

- Remoção de características com valores faltantes.
  - Remover colunas que excedam uma quantidade máxima de dados faltantes que definimos.
- Remoção de características com baixa variância.
  - Baixa variãncia pode tornar o modelo enviesado a partir daquela característica.
- Remoção de característica com alta correlação.
  - Características com alta correlação se tornam redundantes em nosso modelo, sendo apenas mais dados para o treino e fazendo com que o processo demore mais. Além de que podem ocasionar _overfitting_. Opte por escolher a coluna com maior correlação com o alvo.
- Seleção de característica univariada.
  - Seleciona as melhores características com base em testes estatísticos univariados.
- Eliminação recursiva de característica.
  - Elimina as características menos importantes e continua o processo até chegar em um número especificado de características.

## Redução de dimensionalidade

- PCA (Principal Components Analysis).
  - É uma técnica de redução de dimensionalidade que projeta os dados em um espaço dimensional menor.
