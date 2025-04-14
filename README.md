# <h1 align="center">OrçaTech</h1>



## ***Requisitos funcionais***

|Identificador| Descrição| Prioridade|
| -------- | -------- | -------- |
|RF01|O sistema deve permitir acessar e coletar automaticamente dados de diversas fontes: extratos bancários (PDF, relatórios, planilhas), comprovantes (e-mails, fotos) e outros.|Alta|
|RF02|O sistema deve permitir classificar as transações em categorias pré-definidas (alimentação, transporte, lazer, etc.) com possibilidade de correção manual se necessário.|Média|
|RF03|O sistema deve permitir organizar e armazenar as informações processadas em um formato estruturado (CSV, SQLite, MySQL), facilitando consultas e análises futuras.|Alta|
|RF04|O sistema deve permitir integrar os dados a uma ferramenta de BI (Power BI, Tableau ou dashboards customizados via Dash/Plotly) para exibir gráficos interativos e filtros.|Alta|
|RF05|O sistema deve permitir analisar os dados históricos por meio de modelos preditivos e técnicas de machine learning para oferecer sugestões, alertas e projeções personalizadas.|Alta|
|RF06|O sistema deve permitir automatizar a execução do fluxo (extração, processamento, atualização) em intervalos programados, com registro de logs para monitoramento e depuração.|Alta|

## ***Requisitos não-funcionais***

|Identificador| Descrição| Tipo|
| -------- | -------- | -------- |
|RNF01|O sistema deve suportar um aumento no volume de dados e múltiplas fontes, incluindo a atualização dinâmica da camada de IA conforme novos dados são integrados.|Escalabilidade|
|RNF02|O sistema deve processar e atualizar as informações rapidamente, assegurando que o dashboard e os feedbacks da IA sejam exibidos com dados atualizados em tempo hábil.|Desempenho|
|RNF03|O sistema deve oferecer uma interface intuitiva e responsiva, que permita ao usuário navegar e compreender os dados e feedbacks facilmente, mesmo sem conhecimento técnico.|Usabilidade e Interface|
|RNF04|O sistema deve ser desenvolvido com uma arquitetura modular, com código bem documentado, facilitando atualizações, correções e a adição de novas funcionalidades.|Manutenibilidade e Modularidade|
|RNF05|O sistema deve garantir alta disponibilidade do sistema, com mecanismos de backup e recuperação de falhas para minimizar impactos operacionais.|Disponibilidade|
