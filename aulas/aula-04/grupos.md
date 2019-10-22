# Grupos/Conjuntos de dados
Separamos o nosso conjunto total de dados em 3 subconjuntos:

1. **Treino**: os dados que iremos usar para treinar o modelo;
1. **Validação**: os dados que responsáveis por validar o modelo;
1. **Teste**: os dados que irão de fato testar o modelo.

No geral, os subconjuntos de treino e validação andam lado a lado, pois ajudam na etapa de treino do modelo. Já o subconjunto de teste serve para avaliarmos o nosso modelo.

## Proporções
As proporções de cada subconjunto variam de acordo com o tamanho do seu _dataset_. Proporções como 70/30 (70 para o treino e 30 para a avaliação) e 80/20 são bastante adotadas. Sendo que, em conjuntos de dados bastante grandes, as etapas do treinamento se tornarão bastante demoradas. Com isso em mente, é interessante adotar a regra: quanto maior o seu _dataset_, maior será o subconjunto de treino e menor os subconjuntos de validação e teste, proporcionalmente.
