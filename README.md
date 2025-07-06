# Análise: Relação entre Hábitos Digitais, Bem-Estar e Produtividade

Este repositório contém uma Análise Exploratória de Dados sobre a relação entre os hábitos digitais diários, o bem-estar e a produtividade de indivíduos.

## Descrição do Projeto

O objetivo deste projeto é investigar as relações entre o uso de mídias sociais, a percepção de bem-estar e duas medidas de produtividade: a autoavaliada e a real. A análise parte da hipótese inicial sobre a discrepância entre essas duas métricas e expande a investigação para descobrir quais fatores estão mais fortemente associados à produtividade no trabalho.

## Problema e Hipóteses

O estudo foi guiado pelas seguintes questões e hipóteses iniciais:

**Pergunta Principal:** Existe uma discrepância entre a produtividade que as pessoas acham que têm e a sua produtividade real? O uso de mídias sociais influencia essa relação?
- Quanto mais tempo uma pessoa passa nas redes sociais, menor é a nota que ela dá para a sua própria produtividade?
- Quanto mais tempo nas redes sociais, menor a produtividade real e mensurável da pessoa?
- Existe uma correlação positiva entre a produtividade autoavaliada e a produtividade real?

## O Conjunto de Dados (Dataset)

Para este estudo, foi utilizado o conjunto de dados público "Social Media vs Productivity", obtido a partir da plataforma de ciência de dados Kaggle. O dataset contém informações sobre os hábitos e o bem-estar de aproximadamente 30.000 indivíduos, incluindo 19 atributos como:

* **Dados Demográficos:** Idade, Gênero, Status de Emprego.
* **Métricas de Uso:** Tempo em Mídia Social, Notificações Diárias, Horas de Trabalho.
* **Métricas de Bem-Estar:** Nível de Stress, Horas de Sono, Satisfação Trabalho-Vida.
* **Métricas de Produtividade:** Pontuação Autoavaliada e Pontuação Real.

## Metodologia e Ferramentas

A análise foi conduzida utilizando Python em um ambiente Google Colab. As principais etapas metodológicas e ferramentas utilizadas foram:

* **Análise Exploratória de Dados:**
    * Análise estrutural e descritiva (`.info()`, `.describe()`).
    * Análise de relações com Matriz de Correlação e Gráficos de Dispersão (Scatter Plots).
    * Análise de distribuições com Histogramas e Boxplots.
* **Pré-Processamento:**
    * Tratamento de Outliers com a técnica de Capping (Percentis 1 e 99).
    * Tratamento de Valores Ausentes com Imputação pela Mediana.
    * Codificação de Variáveis Categóricas com One-Hot Encoding.
    * Escalonamento de Features com Padronização (StandardScaler).
* **Principais Bibliotecas:** `Pandas`, `Matplotlib`, `Seaborn`, `Scikit-learn`.

## Principais Descobertas e Insights

A análise dos dados revelou os seguintes insights principais:

* A descoberta mais significativa foi a **correlação positiva e muito forte entre a "Satisfação Trabalho-Vida" e a Produtividade Real (coeficiente de 0.88)**.
* A "Satisfação Trabalho-Vida" também se correlaciona fortemente com a **Produtividade Autoavaliada (0.85)**, embora a relação com a produtividade real seja ligeiramente mais forte.
* Foi identificado um **"piso" nos dados de autoavaliação**, sugerindo um **viés de desejabilidade social**, onde os indivíduos evitam se atribuir notas de produtividade extremamente baixas.
* Variáveis que intuitivamente parecem importantes, como `NÍVEL_STRESS`, `HORAS_SONO` e `TEMPO_DIÁRIO_EM_MÍDIA_SOCIAL`, **não apresentaram correlação linear significativa** com a produtividade real no escopo desta análise.

A conclusão é que o bem-estar e o equilíbrio entre vida e trabalho são os fatores mais proeminentes associados à produtividade neste dataset.


* **Ursula Machado Weinstein**
* GitHub: https://github.com/ursula2025/analise-de-dados
