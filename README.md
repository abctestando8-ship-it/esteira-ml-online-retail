# Esteira de Machine Learning — Previsão de Churn (Online Retail)

## Descrição do projeto

Projeto de **classificação** que prevê se um cliente de uma loja online **vai voltar a comprar** ou **vai parar de comprar (churn)**. A ideia é que a loja possa direcionar ações de retenção (como cupons) só para quem está em risco de sair.

- **Base de dados:** [Online Retail — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail) (~540 mil transações de uma loja online do Reino Unido, entre 12/2010 e 12/2011).
- **Modelo:** Random Forest (scikit-learn).
- **Resultado:** acurácia de cerca de **67%** no conjunto de teste (um "chute" que sempre prevê a classe mais comum acertaria cerca de 59%).

A esteira, toda em um único notebook, contém:

1. Carga da base
2. Estatísticas descritivas
3. Transformações nas linhas (remoção de linhas sem cliente, repetidas e com quantidade/preço inválidos)
4. Transformações nas colunas (conversão de tipo, criação de colunas, remoção de coluna)
5. Criação da tabela de clientes e da coluna a ser prevista (`churn`)
6. Divisão em treino (60%), validação (20%) e teste (20%)
7. Treinamento e avaliação do modelo
8. Matriz de confusão e acurácia no conjunto de teste
9. Implantação do modelo (salvar e carregar) e predição


## Como reproduzir a execução

1. Baixe a base em https://archive.ics.uci.edu/dataset/352/online+retail (botão **Download**). Será baixado um arquivo `.zip`. **Não precisa descompactar.**
2. Abra notebook no Colab.
3. No menu do Colab, clique em **Ambiente de execução → Executar tudo**.
4. Quando aparecer o botão **Escolher arquivos** (na célula de carga dos dados), selecione o `.zip` baixado no passo 1.
5. Aguarde cerca de 1 a 2 minutos: a leitura do arquivo Excel é a parte mais demorada.
6. Ao final, o notebook mostra as estatísticas, a acurácia no teste, a matriz de confusão e as predições de exemplo.