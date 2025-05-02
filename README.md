# <h1 align="center">OrçaTech</h1>
Orçatech é um sistema de automação financeira que integra RPA, processamento de dados e inteligência artificial para ajudar os usuários a gerenciar suas despesas de forma eficaz. O projeto automatiza a extração de dados de diversas fontes, processa e organiza as informações em um banco de dados, e as apresenta em um dashboard interativo no Power BI.

## 🚀Tecnologias Utilizadas
- ``UiPath``: Ferramenta de RPA (Robotic Process Automation) utilizada para automatizar tarefas repetitivas, como acessar contas bancárias, baixar extratos, buscar faturas em e-mails e planilhas. No Orcatech, o UiPath é responsável por coletar automaticamente os dados financeiros que serão processados posteriormente.
- ``Python``: Linguagem de programação escolhida para processar, organizar e analisar os dados extraídos. Utilizando bibliotecas como pytesseract para OCR, pandas para manipulação de dados e scikit-learn para criação de modelos de IA, o Python realiza a extração de informações relevantes (data, valor, descrição) e treina algoritmos de machine learning para fornecer feedbacks inteligentes aos usuários.
- ``SQLite``: Banco de dados local utilizado para armazenar todas as transações financeiras de forma estruturada, sem a necessidade de servidores externos. No projeto, o SQLite registra informações como data, valor, descrição e categoria das despesas, servindo como a base de dados que alimenta o dashboard.
- ``Power BI``: Plataforma de Business Intelligence usada para visualizar e analisar os dados financeiros armazenados no SQLite. Através de dashboards interativos e gráficos dinâmicos, o Power BI permite que os usuários acompanhem seus gastos, recebam alertas e insights sobre seus padrões de consumo.

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

## ***Relação de Atores***

| ID  | Nome do ator   | Descrição                                                                 |
| ----|----------------|---------------------------------------------------------------------------|
| A1  | Usuário        | Responsável por fazer login, fazer cadastro, enviar fatura, categorizar faturas, registrar faturas no Dashboard, pedir relatório e recusar relatório. |
| A2  | Bot            | Responsável por achar faturas no e-mail do usuário, analisar os dados do Dashboard e dar feedback ao usuário. |
| A3  | IA (Inteligência Artificial) | Responsável por analisar as faturas recebidas e emitir um relatório das faturas. |
| A4  | Administrador  | Responsável por gerenciar o sistema, incluindo funções administrativas como gerenciamento de usuários e configuração do sistema. |

## ***Relação de Casos de Uso***

| ID  | Caso de Uso                        | Descrição                                                                | Atores envolvidos                              |
| --- | ----------------------------------- | ------------------------------------------------------------------------ | --------------------------------------------- |
| CU1 | Fazer login                        | O usuário faz login no sistema.                                          | Usuário                                        |
| CU2 | Fazer cadastro                     | O usuário se cadastra no sistema.                                        | Usuário                                        |
| CU3 | Enviar fatura                      | O usuário envia uma fatura para o sistema.                               | Usuário                                        |
| CU4 | Categorizar fatura                 | O usuário categoriza a fatura enviada.                                   | Usuário                                        |
| CU5 | Registrar faturas no Dashboard     | O usuário registra as faturas enviadas no Dashboard.                     | Usuário                                        |
| CU6 | Pedir relatório                    | O usuário solicita a geração de um relatório de faturas.                 | Usuário                                        |
| CU7 | Recusar relatório                  | O usuário recusa o relatório solicitado.                                 | Usuário                                        |
| CU8 | Achar faturas no e-mail do usuário | O bot localiza as faturas no e-mail do usuário.                          | Bot                                            |
| CU9 | Analisar dados do Dashboard        | O bot analisa os dados disponíveis no Dashboard.                         | Bot                                            |
| CU10 | Dar feedback ao usuário           | O bot fornece feedback com base nas análises realizadas.                | Bot                                            |
| CU11 | Analisar faturas recebidas        | A IA analisa as faturas recebidas para gerar insights.                   | IA (Inteligência Artificial)                   |
| CU12 | Emitir relatório de faturas       | A IA gera um relatório com base nas faturas analisadas.                  | IA (Inteligência Artificial)                   |

## Sprint BackLog

| ID  | Item/História do Usuário  |  Prioridade | Estimativa  | Responsável | Critérios de aceitação |  
| --- | ------------------------- | ----------- | ----------- | ----------- | ---------------------- |
| SB1  | Configurar o repositório  |  Alta | 1 SP  | Álefh | Repositório criado com README e branch protection. | 
| SB2  | Criar diagrama de Casos de Uso e Entidade-Relacionamento e incluir no repositório  |  Alta | 2 SP  | Álefh e Fábio | Diagramas revisados e anexados no repositório. | 
| SB3  | Fazer a relação de Atores e Relação de Casos de Uso  |  Alta | 1 SP  | Álefh | Relações revisadas e documentados no README. | 
| SB4  | Estruturar projeto Python (virtualenv, requirements.txt, organização de pastas)  |  Alta | 2 SP  | Álefh | Ambiente funcionando, dependências instaladas e estrutura inicial criada. | 
| SB5  | Criar script de conexão e criação de tabelas no SQLite  |  Média | 3 SP  | Álefh | Banco de dados .db criado localmente com tabelas Transação, Categoria e Usuário. |
| SB6  | Desenvolver robot RPA (UiPath) para baixar extratos bancários  |  Alta | 5 SP  | Álefh | Robot funcionando: extrato baixado automaticamente em pasta configurada. |
| SB7  | Implementar OCR com pytesseract para extrair texto de PDFs de extrato  |  Médio | 5 SP  | Fábio | Texto extraído corretamente de amostras de PDF. |
| SB8  | Criar script de parsing para extrair data, valor e descrição usando regex  |  Alto | 3 SP  | Fábio | Script funcionando com 3 formatos diferentes de extrato. |
| SB9  | Configurar dashboard inicial no Power BI com conexão ao SQLite  |  Médio | 3 SP  | Fábio | Dashboard mostrando tabela de transações e gráfico de despesas por categoria. |
| SB10 | Esboçar primeiro modelo de IA usando scikit-learn para previsão de gastos  |  Baixa | 2 SP  | Álefh | Modelo treinado com dados dummy, previsões exibidas no console. |
| SB11 | Criar testes unitários iniciais para scripts de OCR e parsing (pytest)  |  Média | 3 SP  | Helder | Testes com 70%+ de cobertura e passando no pipeline de CI/CD. |



















