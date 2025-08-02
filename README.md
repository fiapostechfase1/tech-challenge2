# 🔮 Previsão do IBOVESPA com Machine Learning

Este repositório apresenta a solução desenvolvida para a **Fase 2 do POSTECH Tech Challenge**, cujo objetivo foi construir um modelo de aprendizado de máquina capaz de prever se o índice **IBOVESPA** fechará em alta ou em baixa no pregão seguinte.

## 📌 Desafio
Desenvolver um modelo preditivo com **acurácia mínima de 75%** para prever a variação diária do IBOVESPA, utilizando dados históricos da B3, engenharia de atributos e técnicas de aprendizado supervisionado.

## 📈 Abordagem
O projeto foi dividido em etapas:

- **Coleta e limpeza dos dados:** Dados históricos do IBOVESPA com cerca de 30 anos foram tratados e padronizados.
- **Engenharia de atributos:** Criação de variáveis derivadas como:
  - Lags (`ultimo_d-1`, `variacao_d-1`, etc.)
  - Momentum (3, 5, 10, 15 dias)
  - Médias móveis simples e exponenciais (SMA, EMA)
  - RSI (Índice de Força Relativa)
  - Amplitude e variação percentual
- **Modelagem:** Teste de diferentes algoritmos:
  - Regressão Logística
  - Random Forest
- **Validação:** Separação do conjunto de teste com base nos últimos 30 dias da série temporal, respeitando a ordem cronológica.
- **Avaliação:** Acurácia, matriz de confusão, precision, recall e F1-score.

## 🧠 Modelo Final
O modelo com melhor desempenho foi a **Regressão Logística**, utilizando como variável mais relevante a **SMA de 3 dias**, alcançando:

- ✅ **Acurácia no teste: 77,2%**
- ✅ Baixa diferença entre treino e teste
- ✅ Simples, interpretável e eficiente

## 🗃️ Estrutura do Projeto
├── content/
│ └── Dados Históricos - Ibovespa_10anos.csv
├── tech_challenge_fase_2.ipynb
├── Documento Descritivo e Slides/
│ └── Modelo-Preditivo-para-o-IBOVESPA.pdf
  └── Tech_Challenge_-_Fase_2_-_Modelo_Machine_Learning_Preditivo_IBOVESPA.pdf
├── Vídeo de Apresentação/
│ └── Link do Vídeo.txt
└── README.md


## 📹 Apresentação
Um vídeo pitch de até 5 minutos acompanha o projeto explicando os principais pontos do desenvolvimento e da solução final.

## 🧑‍💻 Tecnologias
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

## 👨‍🏫 Contribuidores
- Bernardo Segovia Guimarães *(Data Scientist & Aluno FIAP)*
- Eduardo Luiz Sales do Prado Soares *(Data Scientist & Aluno FIAP)*
- Erick David de Souza Santos *(Data Scientist & Aluno FIAP)*
- Gabriel Perez Rodrigues *(Data Scientist & Aluno FIAP)*
- Renato dos Santos Ferreira *(Data Scientist & Aluno FIAP)*

---

## 🏁 Resultado
A meta de acurácia foi superada com sucesso, provando a eficácia da modelagem supervisionada mesmo em problemas complexos como a previsão do comportamento do mercado financeiro.

---
