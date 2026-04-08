Tópicos
1.	Verifique os cabeçalhos e tipos de dados.
R: Power Query identificou corretamente os tipos dos dados.

2.	Modifique os valores monetários para o tipo double preciso.
R: Power Query já trouxe o dado no formato solicitado.

3.	Verifique a existência dos nulos e analise a remoção.
R: O colaborador James Borg não possuía supervisor.

4.	Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente.
R: O colaborador James Borg.

5.	Verifique se há algum departamento sem gerente.
R: Nenhum.

6.	Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas.
R: Todos já preenchidos

7.	Verifique o número de horas dos projetos.
R: Ok

8.	Separar colunas complexas.
R: Feito a separação da coluna Address, tabela employee. Criadas as colunas de Adress_number, street_name, city e state através de funções no Power Query.

9.	Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção.
R: 

10.	Neste processo elimine as colunas desnecessárias. 
R: Removidos as colunas com dados do tipo Table.

11.	Realize a junção dos colaboradores e respectivos nomes dos gerente . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo.
R: Feito a mescla de consultas usando a tabela employee como primária e ela mesmo como secundária. As chaves usadas foram Super_ssn da primeira tabela e Ssn da segunda. A coluna trazida foi a de Full_name como Manager, resultando na nova tabela employee_manager.

12.	Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores.
R: Feito a mescla das colunas Fname e Lname, gerando a coluna Full_name.

13.	Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.
R: Feito a mescla de consultas usando a tabela department como primária e dept_locations como secundária. As chaves foram Dnumber da primeira tabela e Dnumber da segunda. A coluna trazida foi Dlocation, que foi utilizada na mescla junto com a coluna Dname. O resultado foi a nova coluna Department_and_loc que ficou na nova tabela department_location.

14.	Explique por que, neste caso supracitado, podemos apenas utilizar o mesclar e não o atribuir. 
R: Não é possível usar a função de acrescentar consultas, pois ela exige que os dados tenham os mesmos cabeçalhos.

15.	Agrupe os dados a fim de saber quantos colaboradores existem por gerente.
R: Um dos dados de Super_ssn ficou em branco pois James Borg não possui gerente.

16.	Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela.
R: Removidos as colunas com dados do tipo Table.

