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
| `notebooks/02_limpeza_e_extracao.ipynb` | Limpa as bases e extrai os boatos do FactPolCheckBr |
| `notebooks/02b_revisao.ipynb` | Mede a concordância da revisão e monta o conjunto eleitoral final |
| `notebooks/03_preprocessamento.ipynb` | Normaliza, tokeniza, remove stopwords (mantém negações), gera versões com e sem stemming e divide o Fake.Br por par |
| `notebooks/04_treino_avaliacao.ipynb` | Vetoriza, treina e avalia os modelos (a fazer) |

As bases de dados não ficam no repositório. Elas são guardadas no Google Drive, na pasta `TCC/dados`.

## Como reproduzir

1. Abra o notebook no Google Colab (Arquivo > Abrir notebook > GitHub).
2. Execute os notebooks na ordem numérica.
3. Todos os sorteios usam a semente 42.

## Revisão dos boatos (FactPolCheckBr)

Os boatos foram extraídos automaticamente das matérias das agências e revisados com apoio de um modelo de linguagem (Claude), seguindo o protocolo descrito no notebook `02`. Não houve validação humana independente (sem kappa de Cohen); a planilha de conferência do lote 1 (`conferencia_lote_01_para_Davi.xlsx`) fica como opção para uma checagem futura. Resultado: 652 candidatos, 536 `ok`, 3 `corrigir`, 113 `descartar` (539 usados). As decisões (ids e motivos, sem os textos) estão em `revisao/`. Os ids são calculados a partir do link da checagem, então são estáveis.
