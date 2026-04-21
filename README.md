# pucpr_data_mining

Um projeto educacional de Data Mining implementando diferentes algoritmos de classificação no famoso dataset Iris da UCI.

## 📋 Descrição do Projeto

Este projeto implementa e compara três algoritmos de classificação fundamentais em Machine Learning usando o dataset Iris. O objetivo é explorar técnicas de mineração de dados, análise exploratória, validação de integridade de dados e avaliação de modelos preditivos.

### Datasets Utilizados

O projeto utiliza **dois conjuntos principais** de dados do Iris:

1. **UCI Machine Learning Repository**
   - Fonte: [UCI Machine Learning Repository - Iris](https://archive.ics.uci.edu/datasets/iris)
   - Contém duas versões:
     - **Iris Original**: Dataset clássico com 150 amostras
     - **Iris Bezdek**: Versão preparada por Bezdek et al. para validação
   - 4 atributos numéricos (comprimento e largura de sépalas e pétalas)
   - 3 classes de flores (Setosa, Versicolor, Virginica)
   - Localização: `uci-dataset-iris/`

2. **Iris do scikit-learn**
   - Integrado na biblioteca scikit-learn
   - Versão **corrigida** do Bezdek com correções de erros de entrada
   - Versão padronizada e utilizada nos notebooks:
     - `iris_decision_tree.ipynb`
     - `iris_knn.ipynb`
   - Carregável diretamente: `from sklearn.datasets import load_iris`
   - Utilizado para testes e benchmarks padrão

## 🚀 Início Rápido

### Requisitos
- Python 3.10+
- Conda ou Miniconda instalado

### Setup do Ambiente

#### Para Linux/macOS:
```bash
conda env create -f data-mining-env-linux.yml
conda activate data-mining
```

#### Para Windows:
```bash
conda env create -f data-mining-env-windows.yml
conda activate data-mining
```

### Verificando a Instalação
```bash
python -c "import sklearn, pandas, numpy; print('Ambiente configurado com sucesso!')"
```

## 📚 Notebooks Disponíveis

| Notebook | Descrição |
|----------|-----------|
| **iris_data_integrity.ipynb** | Análise de integridade comparando UCI original, Bezdek (corrigido) e sklearn. Evidencia os erros de entrada no dataset original e como foram corrigidos. Baseado no artigo de Bezdek et al. (1999) |
| **iris_decision_tree.ipynb** | Implementação de Árvore de Decisão com visualizações |
| **iris_knn.ipynb** | Implementação de K-Nearest Neighbors com análise de k-vizinhos |
| **iris_reptree.ipynb** | Implementação de Replica Tree (árvore de repetição) |

## 🤖 Modelos e Técnicas Utilizadas

### 1. **Análise de Integridade de Dados**
- **Comparação histórica dos datasets**:
  - UCI original vs. Bezdek (corrigido) vs. sklearn
  - Identificação de 3 amostras com erros de entrada na versão original
  - Confirmação de que sklearn implementou as correções de Bezdek et al. (1999)
- **Referência**: Bezdek et al. *"Will the real iris data please stand up?"* IEEE Transactions on Fuzzy Systems, 1999
- Análise exploratória e validação de integridade
- Verificação de valores faltantes
- Estatísticas descritivas
- Detecção de outliers

### 2. **Árvore de Decisão (Decision Tree)**
- Classificador baseado em árvores de decisão
- Visualização da estrutura da árvore
- Importância das features
- Matriz de confusão

### 3. **K-Nearest Neighbors (KNN)**
- Algoritmo de classificação por vizinhança
- Análise de diferentes valores de k
- Gráficos de dispersão com predições
- Avaliação de precisão por k

### 4. **Replica Tree**
- Técnica avançada de árvores de replicação
- Análise comparativa de performance
- Métricas de desempenho

## 📁 Estrutura do Projeto

```
pucpr_data_mining/
├── README.md                          # Este arquivo
├── LICENSE                            # Licença MIT
├── data-mining-env-linux.yml          # Ambiente conda para Linux/macOS
├── data-mining-env-windows.yml        # Ambiente conda para Windows
│
├── iris_data_integrity.ipynb          # Análise exploratória dos dados
├── iris_decision_tree.ipynb           # Modelo: Árvore de Decisão
├── iris_knn.ipynb                     # Modelo: K-Nearest Neighbors
├── iris_reptree.ipynb                 # Modelo: Replica Tree
│
├── uci-dataset-iris/                  # Dataset original UCI
│   ├── Index
│   └── iris.names
│
├── docs/                              # Documentação adicional
├── output/                            # Gráficos e resultados gerados
└── .git/                              # Controle de versão
```

## 💻 Como Usar

### Opção 1: Jupyter Notebook
```bash
jupyter notebook
```
Abra qualquer um dos arquivos `.ipynb` no navegador.

### Opção 2: Jupyter Lab
```bash
jupyter lab
```

### Opção 3: VS Code
- Abra a pasta do projeto no VS Code
- Instale a extensão "Jupyter"
- Abra qualquer notebook e execute as células

## 📊 Dependências Principais

- **scikit-learn**: Algoritmos de Machine Learning
- **pandas**: Manipulação de dados
- **numpy**: Computações numéricas
- **matplotlib**: Visualizações 2D
- **seaborn**: Visualizações estatísticas
- **jupyter**: Notebooks interativos

## 📈 Fluxo de Trabalho Recomendado

1. **Comece com**: `iris_data_integrity.ipynb`
   - Entender os dados
   - Verificar qualidade

2. **Depois explore**: `iris_decision_tree.ipynb`
   - Modelo interpretável
   - Visualize a árvore

3. **Em seguida**: `iris_knn.ipynb`
   - Algoritmo baseado em distância
   - Experimente diferentes k

4. **Finalmente**: `iris_reptree.ipynb`
   - Técnica mais avançada
   - Compare performances

## 📝 Exemplos de Uso

```python
# Carregar dados
from sklearn.datasets import load_iris
iris = load_iris()

# Criar e treinar modelo
from sklearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier()
model.fit(iris.data, iris.target)

# Fazer predições
prediction = model.predict(iris.data[:5])
```

## 🔍 Próximos Passos

- [ ] Implementar validação cruzada (Cross-Validation)
- [ ] Adicionar tuning de hiperparâmetros
- [ ] Comparação de performance entre modelos
- [ ] Visualizações interativas com Plotly
- [ ] Exportar modelos treinados

## 📄 Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

```
MIT License

Copyright (c) 2026 Renato Gouveia

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
```

## 👤 Autor

**Renato Gouveia**
- Projeto: Data Mining com Iris
- Instituição: PUCPR
- Ano: 2026

## 📧 Contato & Contribuições

Se você tiver sugestões, dúvidas ou queira contribuir com melhorias, sinta-se livre para:
- Abrir uma issue
- Enviar um pull request
- Entrar em contato

---

**Última atualização**: Abril de 2026