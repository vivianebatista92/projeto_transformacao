# 🏡 Projeto de Transformação de Dados — Precificação de Imóveis no Turismo

Este projeto tem como objetivo realizar **transformações e limpezas de dados** para apoiar uma futura solução de **precificação inteligente** de imóveis voltados ao aluguel de curto prazo, com foco no setor de turismo.

Os dados utilizados representam imóveis e sua disponibilidade ao longo do tempo, e foram extraídos de arquivos JSON com informações detalhadas de hospedagem.

---

## 🎯 Objetivo

- Normalizar e tratar os dados brutos vindos de arquivos JSON.
- Transformar colunas aninhadas e listas em dados estruturados.
- Realizar limpezas, correções de tipo e padronizações.
- Aplicar manipulações textuais para análises futuras.
- Gerar um dataset pronto para ser explorado por modelos de precificação e inteligência de mercado.

---

## 📁 Estrutura do Projeto

| Arquivo                         | Descrição                                                  |
|--------------------------------|-------------------------------------------------------------|
| `projeto_transformacao.ipynb`  | Notebook principal com todas as etapas de transformação     |
| `dados_hospedagem.json`        | Dataset com detalhes dos imóveis (características e preços) |
| `moveis_disponiveis.json`      | Dataset com a disponibilidade diária dos imóveis            |

---

## 🧪 Etapas Desenvolvidas

### 🔹 Leitura e Normalização
- Leitura do JSON com informações aninhadas.
- Uso do `json_normalize` para transformar os dados em um dataframe plano.

### 🔹 Explosão de Listas
- Aplicação de `.explode()` para desagrupar valores em listas (ex: camas, banheiros, preços por noite).

### 🔹 Conversão de Tipos
- Conversão de colunas numéricas para `int` e `float`.
- Remoção de símbolos como `$` e vírgulas em colunas financeiras.

### 🔹 Tratamento Textual
- Transformação de textos para letras minúsculas.
- Limpeza de caracteres especiais com regex.
- Tokenização (split por palavra) em descrições e comodidades.

### 🔹 Manipulação Temporal
- Leitura do segundo JSON com datas de disponibilidade.
- Conversão da coluna de data para `datetime`.
- Agrupamento por mês para contar a quantidade de imóveis disponíveis.

---

## 🔧 Tecnologias Utilizadas

- **Python 3**
- **Pandas**
- **NumPy**
- **Regex**
- **Jupyter Notebook / Google Colab**

---

## 📊 Insights Possíveis (Próximas Etapas)

Com o dataset tratado, agora é possível:
- Criar dashboards de análise de disponibilidade por mês.
- Avaliar comodidades que impactam no preço.
- Modelar a precificação com base em localização, avaliação, número de quartos, etc.
- Avaliar sazonalidade da oferta de imóveis.

---

## 📌 Observação
Este projeto faz parte da minha formação em Análise de Dados, com foco no domínio de ETL e pré-processamento de dados aplicados a problemas reais de mercado.
