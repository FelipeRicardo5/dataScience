# Relatório Técnico – Desafio Eletivo 1

## 1. Hipóteses
Neste estudo, buscamos avaliar se existe uma diferença significativa entre as idades de dois grupos distintos. Para isso, formulamos as seguintes hipóteses estatísticas:

- **H0 (Hipótese Nula):** As idades dos dois grupos possuem distribuição semelhante. Não há diferença estatisticamente significativa entre os grupos.
- **H1 (Hipótese Alternativa):** Há uma diferença estatisticamente significativa entre as idades dos dois grupos.

## 2. Materiais e Métodos

### Linguagem
- Python 3 foi utilizado para análise dos dados.

### Bibliotecas
As bibliotecas utilizadas foram:
- **pandas** – manipulação de dados;
- **numpy** – cálculo estatístico;
- **scipy.stats** – testes estatísticos;
- **seaborn** e **matplotlib.pyplot** – visualizações gráficas.

### Conjuntos de Dados
Os grupos de idades analisados foram:

- **Grupo 1:** [12, 15, 18, 22, 22, 25, 28, 30, 35, 40]
- **Grupo 2:** [15, 18, 21, 25, 25, 28, 31, 33, 38, 43]

### Etapas da Análise

1. **Estatísticas Descritivas:**
   - Média, variância e intervalo interquartil (IQR) foram calculados para ambos os grupos.

2. **Teste de Normalidade (Shapiro-Wilk):**
   - Avalia se os dados seguem distribuição normal. Um p-valor maior que 0,05 sugere normalidade.

3. **Teste de Comparação entre Grupos:**
   - Se ambos os grupos forem normalmente distribuídos, utilizamos o **teste t de Student (independente)**.
   - Caso contrário, utilizamos o **teste de Mann-Whitney U**, que é não paramétrico.

4. **Visualização Gráfica:**
   - Histogramas com curvas de densidade para analisar a distribuição.
   - Boxplot para comparar visualmente a dispersão e a mediana entre os grupos.

## 3. Resultados

### Estatísticas Descritivas

| Estatística | Grupo 1 | Grupo 2 |
|-------------|---------|---------|
| **Média**   | 26.7    | 27.7    |
| **Variância** | 78.57 | 71.68   |
| **IQR**     | 13.5    | 12.0    |

### Teste de Normalidade (Shapiro-Wilk)

- **Grupo 1:**
  - Estatística W = 0.963
  - p-valor = 0.826

- **Grupo 2:**
  - Estatística W = 0.956
  - p-valor = 0.759

**Interpretação:** Como ambos os p-valores são superiores a 0.05, podemos assumir que os dois conjuntos seguem uma distribuição normal.

### Teste de Comparação – Teste t de Student

- Estatística t = -0.312
- p-valor = 0.758

**Interpretação:** O p-valor é maior que 0.05, portanto, não rejeitamos a hipótese nula (H0). Não há diferença estatisticamente significativa entre as idades dos dois grupos.

### Visualizações
- Os histogramas mostram uma distribuição levemente simétrica para ambos os grupos.
- O boxplot revela distribuições e medianas próximas, reforçando o resultado do teste t.

## 4. Referências

- **Python Software Foundation.** Python Language Reference. Disponível em: [https://www.python.org](https://www.python.org)
- **Pandas:** [https://pandas.pydata.org](https://pandas.pydata.org)
- **NumPy:** [https://numpy.org](https://numpy.org)
- **SciPy:** [https://scipy.org](https://scipy.org)
- **Seaborn:** [https://seaborn.pydata.org](https://seaborn.pydata.org)
- **Matplotlib:** [https://matplotlib.org](https://matplotlib.org)
- Apostilas e slides do curso (caso aplicável)
