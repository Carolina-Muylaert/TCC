# Análise das políticas anticíclicas no Brasil com VEC estrutural durante a pandemia da covid-19

Este repositório apresenta um estudo econométrico desenvolvido para o TCC em Data Science e Analytics da USP/Esalq em R para analisar os impactos das políticas anticíclicas sobre o crescimento econômico brasileiro, com ênfase no período da pandemia da COVID-19.

A pesquisa utiliza modelos Vetoriais com Correção de Erros (VEC/VECM), testes de estacionariedade, cointegração de Johansen e Funções Impulso-Resposta (IRF) para investigar as relações dinâmicas entre importantes variáveis macroeconômicas brasileiras. 

---

# Objetivo

Avaliar os efeitos das políticas:

* Monetária (taxa Selic);
* Fiscal (gastos públicos e dívida pública);
* Creditícia (expansão do crédito);

sobre o Produto Interno Bruto (PIB) brasileiro no contexto de políticas anticíclicas utilizadas em períodos de crise econômica.

---

# Base de Dados

Os dados utilizados foram obtidos a partir de bases oficiais:

* Instituto Brasileiro de Geografia e Estatística — SIDRA/IBGE
* Banco Central do Brasil — SGS/Bacen

## Séries utilizadas

* PIB trimestral;
* IPCA;
* Taxa Selic;
* Crédito;
* Dívida pública;
* Gastos públicos com saúde e seguridade social.

## Período analisado

A amostra abrange dados trimestrais entre:

**Janeiro de 1996 até dezembro de 2021.**

---

# Metodologia

O projeto foi estruturado nas seguintes etapas:

## 1. Coleta e tratamento dos dados

* Importação automática das séries via APIs do SIDRA e SGS;
* Deflação das variáveis nominais;
* Conversão de séries mensais para frequência trimestral;
* Aplicação de logaritmo;
* Dessazonalização das séries com sazonalidade estatisticamente significativa.

---

## 2. Análise exploratória

Foram realizadas análises de:

* tendência;
* sazonalidade;
* autocorrelação;
* comportamento temporal das séries.

---

## 3. Testes de estacionariedade

Aplicação dos testes:

* ADF (Augmented Dickey-Fuller);
* KPSS.

Objetivo:

* verificar presença de raiz unitária;
* identificar ordem de integração das séries temporais.

---

## 4. Cointegração

Aplicação dos testes de Johansen:

* Trace Test;
* Maximum Eigenvalue Test.

Objetivo:

* verificar relações de equilíbrio de longo prazo entre as variáveis macroeconômicas.

---

## 5. Modelo VEC/VECM

Estimativa do modelo Vetorial com Correção de Erros (VECM) para capturar:

* relações de longo prazo;
* ajustes de curto prazo;
* dinâmica conjunta das variáveis econômicas.

---

## 6. Causalidade de Granger

Análise de causalidade temporal entre as variáveis macroeconômicas.

---

## 7. Função Impulso-Resposta (IRF)

A Função Impulso-Resposta (Impulse Response Function – IRF) foi utilizada para avaliar como choques em determinadas variáveis afetam o PIB ao longo do tempo.

A IRF permite analisar:

* direção dos impactos;
* intensidade dos efeitos;
* persistência temporal;
* velocidade de dissipação dos choques.

Os choques analisados incluem:

* inflação;
* Selic;
* crédito;
* gastos públicos;
* dívida pública.

---

# Principais Resultados

Os resultados indicam que:

* O PIB, os gastos públicos e o crédito apresentam relação positiva com o PIB;
* A relação positiva dos gastos e do crédito com o PIB ocorre principalmente no curto prazo;
* A Selic e a dívida pública afetam negativamente o PIB no longo prazo;
* A Função Impulso-Resposta (IRF) mostra que PIB, gastos e crédito exercem impactos positivos sobre o PIB;
* Os efeitos positivos dos gastos públicos e do crédito sobre o PIB persistem ao longo do tempo;
* A Selic e a dívida pública afetam negativamente o PIB no curto prazo, porém esses efeitos tendem a se dissipar ao longo do horizonte temporal analisado;
* Políticas fiscais e monetárias expansionistas podem contribuir para sustentar os níveis de demanda agregada;
* O aumento da dívida pública e da taxa Selic exige cautela, sobretudo no curto prazo.

---

# Bibliotecas Utilizadas

Principais pacotes utilizados no projeto:

```r
tidyverse
BETS
sidrar
vars
tsDyn
tseries
seasonal
seastests
mFilter
```

---

# Possíveis Extensões

O projeto pode ser expandido para:

* modelos SVAR;
* modelos Bayesianos;
* decomposição da variância do erro de previsão;
* análise de diferentes períodos de crise;
* inclusão de variáveis externas;
* previsão macroeconômica.

---
