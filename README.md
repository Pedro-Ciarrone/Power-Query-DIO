# Projeto de Power BI DIO - 2

Este projeto foi realizado com base a partir dos scripts SQL presentes no repositório do Curso de Power BI da DIO (Digital Innovation One), com os arquivos estando ['Módulo 3'](https://github.com/julianazanelatto/power_bi_analyst/tree/main/Módulo%203/Desafio%20de%20Projeto) ministrado pela professora e Data Analytics Engineer [Juliana Macarenhas](https://www.linkedin.com/in/juliana-mascarenhas-ds/). 

## Etapa 1: MySQL

Primeiramente, realizei os passos descritos na série de vídeos do desafio para [criar o banco de dados MySQL na Azure](https://web.dio.me/course/coleta-e-extracao-de-dados-com-power-bi/learning/0ed1f1c5-601d-402b-9230-eccb791a184d?back=/track/santander-bootcamp-2023-ciencia-de-dados-com-python&tab=undefined&moduleId=undefined). Com isto feito, foram realizados os downloads dos scripts já citados e a execução deles no MySQL Workbench. Na execução do script de inserção de dados, ocorreu um erro com a inserção de valor NULL na coluna Super_ssn da tabela employee. Para resolver isto, precisei alterar o script original para que esta coluna pudesse aceitar nulos, assim, executei o código:

ALTER TABLE employee MODIFY Super_ssn CHAR(9) DEFAULT NULL; 

Com esta alteração feita, o código funcionou normalmente e pude partir para o Power BI.

## Etapa 2: Power BI

No Power BI, obtive os dados para transformá-los no Power Query. Dentro do Power Query, comecei retirando as colunas de constraints, em seguida, alterei os tipos de dados nas colunas necessárias, adicionei o Super_ssn para o colaborador que não possuia, alterei os nomes das colunas para que estes fossem mais lógicos e explícitos.
