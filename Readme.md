Dashboard de Análise Estatística com R e Shiny
Este projeto consiste em uma aplicação web interativa desenvolvida em linguagem R, utilizando o framework Shiny para a visualização de dados e execução de inferências estatísticas em tempo real. A arquitetura é baseada no modelo reativo, permitindo a atualização dinâmica de outputs conforme a alteração de inputs de controle.

Arquitetura da Aplicação
O sistema está segmentado em dois componentes principais:

UI (User Interface): Definição da camada de apresentação utilizando fluidPage, componentes de input (sliders, seletores) e placeholders de saída (plots, tabelas).

Server: Implementação da lógica de negócio, onde as expressões reativas (reactive(), observeEvent()) gerenciam o fluxo de dados e os cálculos estatísticos.

Métodos Estatísticos Implementados

A aplicação processa conjuntos de dados através dos seguintes métodos:

1. Análise Descritiva e Exploratória (EDA)
Medidas de Tendência Central: Cálculo de média, mediana e moda.

Medidas de Dispersão: Desvio padrão, variância e intervalo interquartil (IQR).

Distribuição de Frequências: Histogramas com estimativa de densidade por kernel (KDE).

2. Modelagem Preditiva e Inferencial
Regressão Linear Multipla: Estimativa de parâmetros via Mínimos Quadrados Ordinários (OLS).

Testes de Hipóteses: Implementação de Teste t de Student, ANOVA e Teste de Qui-quadrado para verificação de significância estatística.

Correlação: Matrizes de correlação de Pearson e Spearman para identificação de colinearidade.

Stack Tecnológica e Dependências
A execução do dashboard depende das seguintes bibliotecas do ecossistema R:

shiny: Core framework para a interatividade web.

ggplot2 / plotly: Motores de renderização gráfica de alta performance.

dplyr / tidyr: Manipulação e transformação de estruturas de dados (DataFrames).

stats: Pacote base para funções estatísticas avançadas.

shinydashboard: Framework para estruturação de layouts administrativos.

Otimização e Performance
Para garantir a escalabilidade do dashboard, foram aplicadas as seguintes técnicas:

Caching Reativo: Uso de bindCache() para evitar reprocessamento de cálculos onerosos.

Async Operations: Implementação opcional de processamento assíncrono para operações de I/O intensivas.

Data Pruning: Filtragem de datasets em nível de servidor antes da renderização no cliente.