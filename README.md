# <h1 align="center">OrçaTech</h1>
Orçatech é um sistema de automação financeira que integra RPA, processamento de dados e inteligência artificial para ajudar os usuários a gerenciar suas despesas de forma eficaz. O projeto automatiza a extração de dados de diversas fontes, processa e organiza as informações em um banco de dados, e as apresenta em um dashboard interativo no Power BI.

# 🔗Principais Funcionalidades
- ✅Extração Automática de Dados:  
    -  Utiliza UiPath para coletar informações de extratos bancários, comprovantes, faturas e planilhas.

-  ✅Processamento e Validação dos Dados:
    -  Emprega Python com bibliotecas como pandas e pytesseract para converter PDFs e imagens em dados estruturados, normalizando informações essenciais como data, descrição, valor e categoria.

-  ✅Armazenamento:
    -  Organiza os dados extraídos em um banco de dados SQLite, facilitando consultas e análises futuras.

-  ✅Dashboard Interativo:
    -  Integração com Power BI para visualização dos dados através de gráficos e relatórios, permitindo acompanhamento detalhado e análise dos padrões de despesas.

-  ✅Feedback Inteligente com IA:
    -  Um módulo de inteligência artificial analisa o histórico financeiro para fornecer feedbacks e sugestões personalizadas, ajudando o usuário a otimizar seu orçamento e identificar possíveis desvios nos gastos.
    
## 🚀Tecnologias Utilizadas
- ``UiPath``
- ``Python``
- ``SQLite``
- ``Power BI``

## ***Requisitos funcionais***

|Identificador| Descrição| Prioridade|
| -------- | -------- | -------- |
|RF01|O sistema deve permitir acessar e coletar automaticamente dados de diversas fontes: extratos bancários (PDF, relatórios, planilhas), comprovantes (e-mails, fotos) e outros.|Alta|
|RF02|O sistema deve permitir classificar as transações em categorias pré-definidas (alimentação, transporte, lazer, etc.) com possibilidade de correção manual se necessário.|Média|
|RF03|O sistema deve permitir organizar e armazenar as informações processadas em um formato estruturado (SQLite), facilitando consultas e análises futuras.|Alta|
|RF04|O sistema deve permitir integrar os dados a uma ferramenta de BI (Power BI, Tableau ou dashboards customizados via Dash/Plotly) para exibir gráficos interativos e filtros.|Alta|
|RF05|O sistema deve permitir analisar os dados históricos por meio de modelos preditivos e técnicas de machine learning para oferecer sugestões, alertas e projeções personalizadas.|Alta|
|RF06|O sistema deve permitir automatizar a execução do fluxo (extração, processamento, atualização) em intervalos programados, com registro de logs para monitoramento e depuração.|Alta|
|RF07|O sistema deve permitir ao usuário adicionar e/ou remover categorias, bem como ajustar regras de categorização para adequar-se a situações específicas não previstas inicialmente.|Média|
|RF08|O sistema deve permitir a exportação de relatórios financeiros e previsões geradas pela IA em formato PDF, XLS ou CSV, para facilitar compartilhamentos e análises offline.|Alta|
|RF09|O sistema deve registrar e armazenar feedbacks explícitos do usuário sobre as recomendações da IA, para que estes sejam considerados em ciclos futuros de aprendizado.|Média|
|RF10|O sistema deve permitir a evolução periódica dos modelos de IA, treinando novamente com novos dados e feedback do usuário para melhorar a assertividade das previsões e sugestões.|Alta|
|RF11|O sistema deve permitir o cadastro do usuário com o email e senha.|Média|

## ***Requisitos não-funcionais***

|Identificador| Descrição| Tipo|
| -------- | -------- | -------- |
|RNF01|O sistema deve suportar um aumento no volume de dados e múltiplas fontes, incluindo a atualização dinâmica da camada de IA conforme novos dados são integrados.|Escalabilidade|
|RNF02|O sistema deve processar e atualizar as informações rapidamente, assegurando que o dashboard e os feedbacks da IA sejam exibidos com dados atualizados em tempo hábil.|Desempenho|
|RNF03|O sistema deve oferecer uma interface intuitiva e responsiva, que permita ao usuário navegar e compreender os dados e feedbacks facilmente, mesmo sem conhecimento técnico.|Usabilidade e Interface|
|RNF04|O sistema deve ser desenvolvido com uma arquitetura modular, com código bem documentado, facilitando atualizações, correções e a adição de novas funcionalidades.|Manutenibilidade e Modularidade|
|RNF05|O sistema deve garantir alta disponibilidade do sistema, com mecanismos de backup e recuperação de falhas para minimizar impactos operacionais.|Disponibilidade|
|RNF06|O sistema deve oferecer um mecanismo de autenticação e autorização robusto, impedindo acessos indevidos e preservando diferentes níveis de permissão.|Segurança|
|RNF07|O sistema deve ter a capacidade de integrar-se facilmente com APIs e outros sistemas externos, garantindo troca de dados eficiente.|Integração|
|RNF08|O sistema deve ser uma aplicação web, acessível em qualquer navegador (desktop ou celular), com layout que se adapte bem a telas grandes e pequenas.|Aplicação|
