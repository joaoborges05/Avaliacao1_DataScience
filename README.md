# Avaliação 1 — Data Science (Wine Recognition Dataset)

Avaliação da disciplina de Ciência de Dados (Universidade Positivo, prof. Leandro Escobar),
utilizando o *Wine Recognition Dataset* (`sklearn.datasets.load_wine`).

## Estrutura do repositório

- `avaliacao_wine.ipynb` — notebook único, que é o relatório completo (capa, preparação dos
  dados, questões teóricas 1–3 e questões práticas 4–10).
- `figuras/` — gráficos exportados em PNG (`qN_descricao.png`), também exibidos no notebook.
- `prompts.txt` — registro dos prompts usados com IA, organizado por questão.
- `requirements.txt` — dependências Python do projeto.

## Como rodar

```bash
python -m venv .venv
.venv\Scripts\activate          # Windows (PowerShell: .venv\Scripts\Activate.ps1)
pip install -r requirements.txt
jupyter notebook avaliacao_wine.ipynb
```

Dentro do Jupyter, use **Kernel → Restart & Run All** para garantir que o notebook roda do
início ao fim sem erros e regenera todas as figuras em `figuras/`.

## Como exportar

### PDF

```bash
pip install nbconvert[webpdf]
# a primeira execução baixa o Chromium via pyppeteer/playwright, se necessário
jupyter nbconvert --to webpdf avaliacao_wine.ipynb
```

Alternativa (requer LaTeX instalado):

```bash
jupyter nbconvert --to pdf avaliacao_wine.ipynb
```

### DOCX

Gere primeiro o HTML e depois converta com [pandoc](https://pandoc.org/installing.html):

```bash
jupyter nbconvert --to html avaliacao_wine.ipynb
pandoc avaliacao_wine.html -o avaliacao_wine.docx
```
