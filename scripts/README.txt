
# Para executar os códigos utilize o python 2.7 #

Pacotes extras necessários:
-numpy
-networkx
-progressbar2

Caso não tenha o gerenciador de pacotes PIP para python, instale utilizando:

	sudo apt-get install python-pip

Para instalar os pacotes necessários, rode os seguintes comandos:

	sudo python2 -m pip install numpy
	sudo python2 -m pip install networkx
	sudo python2 -m pip install progressbar2

Para rodar o programa:

	Descompactar os arquivos de dados "perm_5.txt até perm_100.txt" dentro da 
	pasta do programa, então executar:
	
		python2 prepareData.py

---------------------------------------------------------------------------------
Códigos fonte:

prepareData.py
	
	Executa o programa principal de acordo com a entrada de dados 
	escolhida e a função que o usuário deseja executar.

createPermutations.py
	
	Cria permutações de tamanhos 5 a 10 e retorna uma lista com todas as permutações
	e outra com uma amosta de 30% de cada conjunto.

countCycles.py

	Recebe uma lista com o conjunto de todas as permutações e coleta dados do grafo
	de ciclos alternados construido para uma permutação. Verifica o total de ciclos,
	numero de ciclos ímpares, numero de ciclos unitários, tam. do maior ciclo, tam. do
	menor ciclo e numero de ciclos orientados. Retorna um array com os dados de para
	cada permutação de cada tamanho.

featureBpStrip.py

	Recebe uma permutação por vez e extrai informações sobre breakpoint e strips,
	como o numero de breakpoints, numero de strips unitárias, tam. da maior strip,
	numero de strips crescentes, numero de strips decrescentes.

getInputs.py

	Determina a função que vai ser executada, por exemplo, a função que coleta as features
	ou executa o SRS ou GRS. Retorna a lista de features + o tamanho da permutaçẽos ou 
	retorna a distancia de reversão + tamanho da permutação.

extractNumberOfReversal.py

	Coleta do site http://mirza.ic.unicamp.br:8080/bioinfo/index.jsf o número exato de
	reversões para permutações dadas.

simpleReversalSort.py

	Algoritmo simples usando reversões, Simple Reversal Sort (SRS).

greedySortingByReversal.py

	Algoritmo guloso usando reversões, Greedy Reversal Sort (GRS)