**Descrição do desafio módulo 3 – Processamento de Dados Simplificado com Power BI**
1.	Criação de uma instância na Azure para MySQL.
2.	Criar o Banco de dados com base disponível no github.
3.	Integração do Power BI com MySQL no Azure .
4.	Verificar problemas na base a fim de realizar a transformação dos dados.

**Diretrizes para transformação dos dados**
1.	Verifique os cabeçalhos e tipos de dados.
2.	Modifique os valores monetários para o tipo double preciso.
3.	Verifique a existência dos nulos e analise a remoção.
4.	Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente.Observei que há colaborador sem gerente mas não o eliminei pois percebi que ele é gerente dos gerentes.
5.	Verifique se há algum departamento sem gerente
6.	Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas.
7.	Verifique o número de horas dos projetos.
8.	Separar colunas complexas.
9.	Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção.O resultado da mescla de tabela foi a tabela ** azure_company   employee_departament**.
10.	Neste processo elimine as colunas desnecessárias. 
11.	Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.Realizei a junção através da mescla de tabelas obtendo a tabela ** azure_company employee_manager**.
12.	Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores. Fiz a junção das colunas com nomes e obtive a coluna Name.
13.	Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.Fiz a mescla de tabelas e obtive a tabela azure_company dept_locations.
14.	Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir. Usei o mesclar pois tem que ter uma coluna em comum entre as consultas, ou seja, uma chave que possibilite fazer a mesclagem, no caso a coluna Dnumber

![image](https://github.com/user-attachments/assets/b293fa42-9288-4fbb-b37d-d7baa8607c5a)    ![image](https://github.com/user-attachments/assets/9e4abb14-157d-441c-9742-bfb15a7e6034)


 

15.	Agrupe os dados a fim de saber quantos colaboradores existem por gerente. Fiz  aplicando a opção “Agrupar por”.
16.	Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela.
