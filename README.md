# MC847 — Trabalho Final de Aprendizado Não Supervisionado

Modelos de recomendação e análise de espaços latentes sobre o dataset **MovieLens 100K**.

## Estrutura do repositório

```
.
├── data/                                # MovieLens 100K, baixado pelo notebook
├── unsupervised_assignment_2s2026.ipynb # notebook do projeto (preenchido e executado)
├── pyproject.toml                       # dependências
├── uv.lock                              # versões exatas, gerado pelo uv
├── .python-version                      # versão do Python usada (3.12)
└── README.md                            # como reproduzir
```

## Como reproduzir

Pré-requisitos: [uv](https://docs.astral.sh/uv/getting-started/installation/).

```bash
# 1. Criar o ambiente
uv sync

# 2. Abrir o Jupyter Lab
uv run --with jupyter jupyter lab
```

Depois, abra `unsupervised_assignment_2s2026.ipynb` e execute todas as células
(*Run All*). Na primeira execução, o notebook baixa e extrai o MovieLens 100K
em `data/ml-100k/`.

As sementes aleatórias estão fixadas com `set_seed(42)`, de modo que tabelas e
figuras devem ser reproduzíveis.

## Dados

O projeto usa o [MovieLens 100K](https://grouplens.org/datasets/movielens/100k/):

- 100.000 notas inteiras (1 a 5) de 943 usuários para 1.682 filmes;
- ~6,3% de densidade (mais de 93% dos pares usuário–filme não têm nota);
- metadados de usuários (idade, gênero, ocupação) e de filmes (título, ano e 19 gêneros).

## Etapas

1. **Baselines e fatoração de matrizes** — baseline aditiva, PCA com imputação e
   fatoração de matrizes com SGD.
2. **Modelos probabilísticos e espaço latente** — PPCA via EM, VAE (decodificador
   linear e não linear) e análise dos espaços latentes.
3. **Projeto do grupo** — pergunta, hipótese, experimento e previsão formulados
   antes da execução.
