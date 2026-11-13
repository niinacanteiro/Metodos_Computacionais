# Métodos Computacionais

> Atividades da disciplina de **Métodos Computacionais** do curso de **Engenharia Elétrica (IFMT)**, desenvolvidas em **Python** no Jupyter/Google Colab. Material de estudo.

![Python](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

## O que tem aqui

| Notebook | Assunto | Resultado |
|---|---|---|
| `METÓDOS_COMPUTACIONAIS_01.ipynb` | Interpolação quadrática de ln(x) usando os pontos x = 1, 4 e 6, para estimar ln(2), e cálculo do erro percentual | f₂(2) ≈ 0,5658 contra ln(2) ≈ 0,6931 → erro de cerca de 18,4% |
| `METÓDOS_COMPUTACIONAIS_02.ipynb` | Interpolação quadrática a partir de uma tabela de dados (x = 10, 20, 30; y = 100, 150, 250) para estimar o valor em x = 25 | f₂(25) = 193,75 |

## O método: interpolação de Newton de 2º grau

Com três pontos conhecidos (x₀, y₀), (x₁, y₁) e (x₂, y₂), o polinômio é:

```
f₂(x) = b₀ + b₁·(x − x₀) + b₂·(x − x₀)·(x − x₁)
```

com os coeficientes calculados por diferenças divididas:

```
b₀ = y₀
b₁ = (y₁ − y₀) / (x₁ − x₀)
b₂ = [ (y₂ − y₁)/(x₂ − x₁) − (y₁ − y₀)/(x₁ − x₀) ] / (x₂ − x₀)
```

E o erro percentual em relação ao valor verdadeiro:

```
E% = (valor verdadeiro − valor aproximado) / valor verdadeiro × 100
```

## Como rodar

- **No navegador:** no [Google Colab](https://colab.research.google.com/), vá em *Arquivo → Abrir notebook → GitHub*, cole o link deste repositório e execute as células em ordem.
- **No computador:**

```bash
pip install notebook
git clone https://github.com/niinacanteiro/Metodos_Computacionais.git
cd Metodos_Computacionais
jupyter notebook
```

Os notebooks usam só Python padrão (`math`), sem outras bibliotecas.

## O que aprendi

- Montar um polinômio interpolador a partir de poucos pontos medidos.
- Calcular coeficientes por diferenças divididas e conferir que o polinômio passa pelos pontos dados.
- Medir a qualidade de uma aproximação com o erro percentual: com pontos distantes do valor procurado (exercício 1), o erro chega a ~18%, o que mostra a importância de escolher pontos próximos.

## Próximos passos

- Comparar a interpolação linear com a quadrática no mesmo problema.
- Gerar gráficos com `matplotlib` mostrando a função real e o polinômio.

---

Feito por **Nicoly Canteiro** · [GitHub](https://github.com/niinacanteiro) · [LinkedIn](https://www.linkedin.com/in/nicoly-canteiro)
