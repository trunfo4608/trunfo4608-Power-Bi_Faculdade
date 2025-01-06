# Gestão Faculdade

1 - Projeto Power Bi focado na gestão de uma Faculdade.
    
2 - Dashboard possui 5 abas: Capa, Campos, Alunos, Financeiro e Geral.
	
3 - "Relatório Campos" Mostra ao usuário a visão dos campos que a faculdade possui.Essa
    aba já possui de cara um componente importado "ChicletSlicer" onde trás todos os campos de faculdade.
	Do lado direito você tem uma navegação que permite ao usuário ir a uma outra página onde ele vai visualizar um
	gráfico de colunas clusterizado com a inadimplência por campos. Logo abaixo diversos gráficos de inadimplência por curso,
	total de alunos e total matrículas. Algo que vale salientar é uma tabela onde mostra o percentual de faturamento por curso,
	para trazer esses percentuais foi usado uma função DAX diferente que se assemelha muito a uma formula excel, onde você trava 
	o valor da coluna e divide pela soma da mesma, retornando assim o valor de cada curso.
    	
	
4 - "Relatório Alunos" Mostra todos os alunos matrículados nos seus respectivos cursos, seus campos e dados cadastrais.
    Temos um visual importado "TEXT FIELTER" onde filtra o aluno por matrícula e ao lado duas segmentações por dados para filtrar por campus ou curso.
	Abaixo temos um visual customizado agindo em paralelo com uma tabela, onde permite trazer as informações de dados cadastrais do aluno que for selecionado
	na tabela mais abaixo, nesse visual algo interessante é o componente "SIMPLE IMAGE"	que trás a foto o aluno e o componente "CLUSTER MAP" que mostra o valor
	faturado por campus.
	
	
5 - "Relatório Financeiro" Temos uma visão geral da área financeira, nesta aba temos o faturamento por campus, faturamento por curso e a inadimplência por curso.
    Temos bastante campos importados como "ROTATING TITLE" que mostra o faturamento por campus e o "CARD BROWSER" que trás um visual bastante interessante
	ao usuário onde mostra o faturamento X o percentual devedor.
	
	
6 - "Relatório Geral" Temos mais informações sobre o faturamento, valor inadimplente e total de alunos. Campos customizados "ROTATING TITLE" trazendo nomes dos campos e total de alunos.
    Abaixo temos o campo do tipo "TORNADO" onde trás o valor faturado x inadimplente, gráfico de pizza e um indicador. 


7 - Estrutura do relatório: 12 tabela(s) dimensõe(s), 2 tabela(s) fato, 1 tabela de tempo e 3 tabela(s) de medida.
    Muitas funções DAX na elaboração das medidas e também função DAX para criação de "JOINS" (F-ALUNOS_INADIMPLENTES = FILTER(GENERATE('D-ALUNO','F-DADOS'),'D-ALUNO'[Matricula] = 'F-DADOS'[Matricula.Aluno] && 'F-DADOS'[SITUACAO] = 2))
	entre tabelas para fazer algumas customizações;	

	  
OBS: O DashBoard se encontra disponível no [link](https://app.powerbi.com/view?r=eyJrIjoiOWI5ZWVjZWEtNWZiZS00ODc1LTg1MDUtZDg3YzQ0NDJhZTM1IiwidCI6IjcyNzEzYTdjLThkN2UtNDZkNy04MWQxLTUzOWZiOWMzMmI4YyJ9)
     a seguir.
