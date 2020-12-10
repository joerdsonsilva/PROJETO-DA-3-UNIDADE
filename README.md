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

  Projetar um Equalizador de áudio utilizando filtros ativos passa-banda de segunda ordem e amplificadores operacionais (amp-op). Por fim, este relatório tem como finalidade mostrar de forma didática como o projeto proposto foi elaborado.

# 1.1 Objetivos Específicos
 O equalizador deve ter 3 estágios, sendo um para frequências graves, um para frequências médias, e um para frequências agudas. A definição das faixas de frequências pode ser observada na Figura 1. Além disso, deve-se ter algum mecanismo de controle de ganho/volume individual (em cada estágio), e um geral (master).
 
 <p align="center">
	<https://github.com/joerdsonsilva/PROJETO-DA-3-UNIDADE/issues/1#issue-760817268>
		</p>
	
# 2. DESENVOLVIMENTO

 Um Equalizador permite que você melhore a qualidade de som, ou seja, permite ajustar os níves e efeitos sonoros e assim possa obter o melhor dos seu aparelho eletrônico, como por exemplo alto-falantes ou fones de ouvidos.
 O projeto tem como finalidade apresentar um equalizador de áudio fácil de usar com o controle de volume individual e um geral, similar ao que acontece na prática.

# 2.1 Memorial Descritivo

 Como mencionado anteriormente, o circuito será constituído por um filtro ativo, do tipo passa banda de segunda ordem, com implementação de amp-op. Dessa forma, para construir a topologia do filtro passa-banda é necessário a junção de dois filtros ativos, o filtro ativo passa-altas e o filtro ativo passa-baixas, respectivamente nessa ordem a junção. Nesta seção, será apresentado o desenvolvimento do projeto, apresentando o memorial descritivo da parte teórica, e por fim, os resultados obtidos. 
 
 # 2.1.1. _Memorial de Cálculo_
  
  A topologia do projeto, é composta por três filtros passa banda, um estágio para cada faixa de frequência, ou seja, para as faixas de frequência grave, médias e agudas, conforme mostrado na Figura 1. Sendo implementador em um amp-op somador, com reguladores de ganho individuais e o geral.
  
  A seguir será apresentado o memorial de cálculo, vale destacar que o circuito implementou o circuito denominado _Sallen-Key de componentes iguais_. 
  
  Considerações:
 
  * Frequência Gaves - adotou-se uma faixa de frequência de 20 Hz à 500 Hz, onde 20 Hz é a frequencia de corte do filtro passa-altas (f_ol) e 500 Hz a frequência de corte do filtro passa-baixas (f_oh).
  
  * Frequência Médias - adotou-se uma faixa de frequência de 250 Hz à 4 kHz, onde 250 Hz é a frequencia de corte do filtro passa-altas (f_ol) e 2 kHz a frequência de corte do filtro passa-baixas (f_oh). Como pode-se notar, levou-se em consideração a faixa de frequência de transição entre as frequências.

* Frequência Aguda - adotou-se uma faixa de frequência de 2 kHz à 20 kHz, onde 2 kHz é a frequencia de corte do filtro passa-altas (f_ol) e 20 kHz a frequência de corte do filtro passa-baixas (f_oh).






# Filtros ativos
Todo mundo tem um conceito intuitivo sobre a função de um filtro. Em quase todos os sistemas eletrônicos existem algum tipo de filtro, principalmente no campo da telecomunicação e da instrumentação industrial, na qual se fazem mais presente em meios aos circuitos. Por exemplo, atualmente, os filtros ativos são elementos básicos nos circuitos de redes de comunicação de dados, posto que os equipamentos de computadores são conectados à rede telefônica através de MODEM, que são a base de filtros ativos. 
Um filtro elétrico por definição é “ um quadripolo capaz de atenuar determinadas frequências do espectro de sinal de entrada e permite a passagem das demais”. Em sua maioria, os filtros são constituídos de componentes passivos como resistores e capacitores. Nos filtros ativos utilizam amplificadores, associados aos elementos passivos, nos quais tem função de produzir amplificação de tensão, buferização ou isolamento do sinal. Os filtros ativos podem ser classificados como passa-baixa, passa-alta ou passa-banda, que é o a junção dos dois outros tipos de filtros e objeto de pesquisa do presente trabalho. 

O equalizador é composto de filtros ativo passa-banda de segunda ordem (onde são construidos por meio de um filtro ativo passa-baixa e um passa-alta, ambos de segunda ordem e com componentes iguais) e divididos nos 3 estagios de frequência (graves, médios e agudos). 


# Filtro passa-baixa - frequências graves
Para as frequências graves, temos que o filtro passa-banda irá atuar entre as frequências de 20Hz a 500Hz, de modo que os componentes dos filtros atuem de acordo com esssas frequências. Podemos calcular os componentes da seguinte forma:

Podemos observar que, os componentes calculados para os filtros são de valores comerciais, sendo para alguns, o uso de associação série ou paralela para obter o valor projetado.

# Filtro passa-baixa - frequências médias
Para as frequências médias, temos que o filtro passa-banda irá atuar entre as frequências de XXHz a XXXHz (o filtro passa-banda de frequências médias atuará entre as frequências graves e agudas. Devido a isso, foi considerado uma faixa de transição entre os graves-médios e agudos-médios (isso ocorre devido a quantidade de estágios, pois nãp é possível compreender todas as faixas de frequências e sub frequências), de modo que existe uma faixa onde as frequências atuam em conjunto), de modo que os componentes dos filtros atuem de acordo com esssas frequências. Podemos calcular os componentes da seguinte forma:

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


Um filtro ideal possuiria uma banda passante totalmente plana (sem atenuação), atenuando completamente todas as frequências fora desta banda (mas prática, nenhum filtro passa-faixa é ideal pois não atenua todas as frequências fora da faixa desejada) e inalterando as frequências dentro as faixas projetadas. O equalzador projetado possui uma 

d) Elaboração da PCB

e) BOM (Bill of materials)

_Elaborar a lista de materiais

f) Finalização e elaboração de vídeo explicativo.

g) Envio dos arquivos fonte.


