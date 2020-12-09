UNIVERSIDADE FEDERAL RURAL DO SEMI-ÁRIDO

DEPARTAMENTO DE ENGENHARIAS

CENTRO MULTIDISCIPLINAR DE CARAÚBAS

DISCIPLINA: CIRCUITOS ELTRÔNICOS II

DOCENTE: DR. PROF. FRANCISCO DE ASSIS BRITO FILHO

DISCENTES :  
             
	     ERIKA OLIVEIRA DOS SANTOS
	     JOERDSON TIAGO BATISTA DA SILVA
	     YURI FERNANDES DA SILVEIRA

# EQUALIZADOR DE ÁUDIO

				 

# 1. OBJETIVO

  Projetar um Equalizador de áudio utilizando filtros ativos, passa-banda de segunda ordem e amplificadores operacionais. Por fim, este relatório tem como finalidade mostrar de forma didática como o projeto proposto foi elaborado.

# 1.1 Objetivos específicos

  O equalizador deve ter 3 estágios, sendo um para frequências graves, um para frequências médias, e um para frequências agudas. A definição das faixas de frequências pode ser observada na Figura 1. Ainda, deve ter algum mecanismo de controle de ganho/volume individual (em cada estágio), e um geral (master).

# 2. DESENVOLVIMENTO

Nesta seção, será apresentado o desenvolvimento do projeto, desde o projeto teórico aos resultados obtidos.

- Etapas do Projeto

a) Criar github de repostitório para o projeto ✅

b) Projeto teórico

O equalizador é composto de filtros ativo passa-banda de segunda ordem (onde são construidos por meio de um filtro ativo passa-baixa e um passa-alta, ambos de segunda ordem e com componentes iguais) e divididos nos 3 estagios de frequência (graves, médios e agudos). 

# Filtro passa-baixa - frequências graves
Para as frequências graves, temos que o filtro passa-banda irá atuar entre as frequências de 20Hz a 500Hz, de modo que os componentes dos filtros atuem de acordo com esssas frequências. Podemos calcular os componentes da seguinte forma:

Podemos observar que, os componentes calculados para os filtros são de valores comerciais, sendo para alguns, o uso de associação série ou paralela para obter o valor projetado.

# Filtro passa-baixa - frequências médias
Para as frequências médias, temos que o filtro passa-banda irá atuar entre as frequências de XXHz a XXXHz, de modo que os componentes dos filtros atuem de acordo com esssas frequências. Podemos calcular os componentes da seguinte forma:

# Filtro passa-baixa - frequências agudas
Para as frequências agudas, temos que o filtro passa-banda irá atuar entre as frequências de 2kHz a 20kHz, de modo que os componentes dos filtros atuem de acordo com esssas frequências. Podemos calcular os componentes da seguinte forma:

# Mecanismo de controle de ganho
O equalizador deve conter um mecanismo de controle de ganho invidual (em cada estágio) e um geral (controle o ganho total), de modo a atuar atuar nas frequências mais graves, médias e agudas dos filtros, assim como no ganho geral do equalizador. Para obter esse mecanismo de controle, será usado potênciometros, posicionados nos filtros (para obter o ganho individual dos estágioss) e no somador (para obter o ganho total) ....... Temos que o ganho do filtro foram definidos da seguinte forma:

Para as frequências graves:

Para as frequências médias:

Para ass frequências agudas:

Para o controle de ganho individual, o potênciometro será posicionado no R2 dos filtro passa-baixas, de modo que se variar o potênciometro com uma resistência mais baixa (R2<X), o ganho do estágio diminui e se varia com uma resistência maior (R2>X), o ganho aumenta. 

Para o controle de ganho master, o potenciômetro é posicionado na resistência de referência Rf, pois cada entrada do somador (saída dos filtros) adiciona um nível de tensão que é multiplicado pelo seu fator de ganho e, como as resistências de de entrada do somador são iguais (R=1k), o potênciometro na posição de Rf afeta diretamente o ganhov (equação X), visto que se eu aumentar o valor de Rf (Rf>1k=R), aumento o ganho total do meu equalizador, e se eu diminuir Rf (Rf<1k=R), terei um ganho total menor do meu equalizador (tendo como base o ganho incial projetado para o equalizador).


c) Captura de esquemático e simulações

d) Elaboração da PCB

e) BOM (Bill of materials)

_Elaborar a lista de materiais

f) Finalização e elaboração de vídeo explicativo.

g) Envio dos arquivos fonte.


