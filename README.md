# pre_modelagem_score_credito_curso_EBAC
Projeto desenvolvido durante o curso Profissão: Cientista de Dados. O objetivo do projeto foi a preparação dos dados para implementação de modelos preditivos numa base de Score de Crédito.

## Etapas do Projeto:

- Etapa 1.1: Verificação dos tipos de dados, conversão e correção de dígitos incorretos (',' por '.');
- Etapa 1.2: Verificação de dados faltantes. A coluna 'Age' apareceu com alguns valores nulos, mas, em virtude do tamanho do conjunto de dados, optou-se por substituir o valor pela média, que se provou idêntica à mediana. Além disso, a coluna foi convertida de float64 para int.
- Etapa 1.3: Verificação de consistência nas variáveis de texto com .unique(). Todas as células se mostraram corretamente digitadas, então não houve necessidade de substituição.
- Etapa 2.1: Verificação das estatísticas básicas com .describe() e análise da distribuição das variáveis numéricas com plotly através da análise de boxplots e histogramas para cada variável. Nenhuma delas apresentou outliers significativos.
- Etapa 2.2: Verificação das distribuições das variáveis categóricas por meio de histogramas feitos com plotly.
- Etapa 2.3: Verificação das relações entre as variáveis por análise bivariada. Aqui, buscou-se responder às seguintes perguntas, com os insights das respostas abaixo de cada uma:
  
  * Existe relação entre a idade e o status civil?
    - A média das idades das pessoas casadas é maior que a das solteiras.
  * Qual a relação entre o score de crédito e o nível de escolaridade?
    - Graus mais altos de esoclaridade demonstram scores mais altos.
  * O salário parece influenciar na idade?
    - Salários aumentam com a idade.
  * O salário parece influenciar no Score de Crédito?
    - Scores mais altos têm relação com maiores rendas.
  * Clientes com casa própria tendem a ter um score mais alto?
    - Sim, scores mais altos estão mais presentes em indivíduos com imóvel próprio.
  * Qual a relação entre gênero e grau de escolaridade?
    - Mais pessoas do gênero feminino tendem ao bacharelado e ao doutorado, enquanto pessoas do gênero masculino tendem ao mestrado e ao grau de associado. 
  * Qual a relação entre grau de escolaridade e renda?
    - Quanto maior o grau de escolaridade, maior a renda associada.
  * Qual a relação entre gênero e score?
    - Homens tendem a scores mais altos

- Etapa 3.1: Análise de correlação e plotagem da matriz com plotly. As variáveis mais correlacionadas foram idade e renda, o que é reforçado pela análise bivariada.
- Etapa 3.2: Tratamento de variáveis categóricas com LabelEncoder, que foi escolhido por seu melhor desempenho em problemas de classificação.
- Etapa 3.3: Plotagem da correlação com as variáveis categóricas convertidas. Aqui, os resultados foram:
  
  * Altas correlações negativas para:
    - Posse de imóveis e idade
    - Estado civil e idade
    - Número de filhos e gênero
    - Estado civil e renda
    - Posse de imóveis e renda
    - Número de filhos e estado civil

  * Altas correlações positivas em:
    - Gênero e renda;
    - Idade e renda;
    - Educação e renda;
    - Estado civil e posse de imóveis.
      
- Etapa 3.5: Separação em bases de treino e teste com train_test_split. Aqui, foi escolhido 25% como tamanho do conjunto teste e random_state = 42 para garantir repetibilidade dos resultados. Em seguida, verificou-se se os tamanhos dos conjuntos estavam corretos. 
- Etapa 3.6: Verificação do balanceamento do conjunto de treino com countplot, provando que a coluna não era balanceada.
- Etapa 3.7: Balanceamento do conjunto de treino com SMOTE e verificação dos resultados.
- Etapa 3.8: Salvamento dos conjuntos de treino e teste para aplicação em projetos posteriores.

## Resultados
Neste projeto, foi possível aplicar todas as etapas de pré-processamento de dados, de forma que o conjunto foi bem preparado para aplicação em modelos de machine learning. 
