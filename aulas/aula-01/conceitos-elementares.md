# Conceitos elementares
Os conceitos que iremos introduzir para que possamos passar por esse módulo sem muitos problemas:

1. Treinamento
1. Generalização
1. População e amostra
  1. Amostragem
1. Viés e variância
1. Validação Cruzada
1. Conjuntos de dados
1. Previsão

## Treinamento
> Refere-se ao processo de aquisição de conhecimento, habilidades e competências como resultado de formação profissional ou do ensino de habilidades práticas relacionadas à competências úteis específicas. ([Wikipedia](https://pt.wikipedia.org/wiki/Treinamento))

## Generalização
A habilidade de generalização é muito importante para um modelo. No nosso contexto, isso quer dizer que o modelo conseguirá desempenhar com precisão a sua função em novos dados, esses ainda não "vistos" por ele. Um modelo com um poder de generalização fraca tende a ser sobreajustado (_overfitting_), já um modelo com um poder de generalização forte será subajustado (_underfitting_). Esses dois problemas de generalização iremos ver mais a frente.

**Resumo**: generalização é a habilidade de classificar padrões de teste que não foram utilizados durante o treinamento.

## População e amostra
A população, na estatistica, consiste em um conjunto de elementos que corresponde aos nossos objetos de estudo, ela pode ser finita ou infinita. A amostra é um subconjunto da população.

### Amostragem
A amostragem é o processo de selecionar um grupo de indivíduos de uma população, a fim de estudar e caracterizar a população total.

- **Margem de erro**: diferença máxima entre os dados observados na minha amostra e os dados reais do universo;
- **Representatividade**: identifica se os elementos mostram a realidade da população;
  - **Balanceamento**: representatividade das classes existentes na população.
- **Nível de confiança**: nível de certeza sobre os dados reais que está dentro da margem de erro.

## Viés/Bias e Variância/Variance
Essencialmente, o viés aqui é uma fonte de erro no seu modelo que faz com que ele generalize e subestime seus dados. Por outro lado, a variação é a sensibilidade ao ruído nos dados que causam um sobreajustado no modelo. Normalmente ocorre de que se você melhorar um, por exemplo o viés, você tende a piorar o outro, no caso seria a variância.

**Exemplos de viés**:
- Viés de algoritmo: referente ao proprietário do código;
- Viés de amostra / Viés latente: os dados usados no treinamento não representam a população;
- Viés de preconceito: quando o conteúdo dos dados de treinamento é influenciado por estereótipos ou preconceitos provenientes da população;
- Viés de medida: resulta de uma medição incorreta;
- Viés de interação: quando o modelo é dependente de indivíduos que interagem com ele, podendo ser enviesado.

## Validação cruzada
É o particionamento do conjunto de dados em subconjuntos mutualmente exclusivos e seu uso no processo de treino e teste do modelo.

As 3 validações cruzadas mais utilizadas:
1. **Holdout**: divide os dados em dois subconjuntos disjuntos, um para treino (normalmente 2/3 do total de dados) e outro para teste (1/3 dos dados);
1. **K-fold**: divide os dados em `n` subconjuntos disjuntos de mesmo tamanho e, a partir disso, usa-se um subconjunto para treino e o restante para teste, alternando entre os subconjuntos;
  1. **Leave-one-out**: nessa abordagem do _k-fold_, se você tiver `k` dados, realiza o processo de treino com `k-1` dados e o teste com o dado que ficou de fora, fazendo isso para todos os dados.

## Conjuntos de dados
Separamos o nosso conjunto total de dados em 3 subconjuntos:

1. **Treino**: os dados que iremos usar para treinar o modelo;
1. **Validação**: os dados que responsáveis por validar o modelo;
1. **Teste**: os dados que irão de fato testar o modelo.

## Previsão
É a habilidade do nosso modelo de conseguir prever algo, após a etapa de treino.
