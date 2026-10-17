# Detecção de desinformação nas eleições presidenciais brasileiras

Código do TCC "Análise comparativa de algoritmos de aprendizado de máquina para detecção de desinformação nas eleições presidenciais brasileiras".

- Aluno: Davi Willian Silva de Paula
- Orientador: Paulo Henrique Rodrigues
- Curso: Sistemas de Informação, PUC Minas (campus Contagem)

## O que este repositório faz

Compara três algoritmos (Naive Bayes, SVM e XGBoost) na detecção de notícias falsas em português.
Os modelos são treinados com as bases Fake.Br e FakeRecogna e testados também no FactPolCheckBr,
com conteúdo das eleições presidenciais de 2022.

## Organização

| Notebook | Etapa |
|---|---|
| `notebooks/00_ambiente.ipynb` | Prepara o ambiente, fixa a semente e registra as versões |
| `notebooks/01_bases.ipynb` | Baixa, unifica e diagnostica as três bases |
| `notebooks/02_preprocessamento.ipynb` | Limpa e padroniza os textos (a fazer) |
| `notebooks/03_treino_avaliacao.ipynb` | Vetoriza, treina e avalia os modelos (a fazer) |

As bases de dados não ficam no repositório. Elas são guardadas no Google Drive, na pasta `TCC/dados`.

## Como reproduzir

1. Abra o notebook no Google Colab (Arquivo > Abrir notebook > GitHub).
2. Execute os notebooks na ordem numérica.
3. Todos os sorteios usam a semente 42.
