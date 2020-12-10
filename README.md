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
 
![](https://user-images.githubusercontent.com/75510214/101711689-d9d17e00-3a72-11eb-89d7-e5ea764948a4.png)

	
# 2. DESENVOLVIMENTO

 Um Equalizador permite que você melhore a qualidade de som, ou seja, permite ajustar os níves e efeitos sonoros e assim possa obter o melhor dos seu aparelho eletrônico, como por exemplo alto-falantes ou fones de ouvidos.
 O projeto tem como finalidade apresentar um equalizador de áudio fácil de usar com o controle de volume individual e um geral, similar ao que acontece na prática.

# 2.1 Memorial Descritivo

 Como mencionado anteriormente, o circuito será constituído por um filtro ativo, do tipo passa banda de segunda ordem, com implementação de amp-op. Dessa forma, para construir a topologia do filtro passa-banda é necessário a junção de dois filtros ativos, o filtro passa-altas e o filtro  passa-baixas, respectivamente nessa ordem a junção. Nesta seção, será apresentado o memorial descritivo da parte teórica, e por fim, os resultados obtidos. 
 
 # 2.1.1. _Memorial de Cálculo_
  
  A topologia do projeto, é composta por três filtros passa banda, um estágio para cada faixa de frequência, ou seja, para as faixas de frequência grave, médias e agudas, conforme mostrado na Figura 1. Sendo implementador em um amp-op somador, com reguladores de ganho individuais e o geral.
  
  A seguir será apresentado o memorial de cálculo, vale destacar que o circuito implementou o circuito denominado _Sallen-Key de componentes iguais_. 
  
  Considerações:
 
  * Frequência Gaves - adotou-se uma faixa de frequência de 20 Hz à 500 Hz, onde 20 Hz é a frequencia de corte do filtro passa-altas (f_ol) e 500 Hz a frequência de corte do filtro passa-baixas (f_oh).
  
  * Frequência Médias - adotou-se uma faixa de frequência de 250 Hz à 4 kHz, onde 250 Hz é a frequencia de corte do filtro passa-altas (f_ol) e 2 kHz a frequência de corte do filtro passa-baixas (f_oh). Como pode-se notar, levou-se em consideração a faixa de frequência de transição entre as frequências.

* Frequência Aguda - adotou-se uma faixa de frequência de 2 kHz à 20 kHz, onde 2 kHz é a frequencia de corte do filtro passa-altas (f_ol) e 20 kHz a frequência de corte do filtro passa-baixas (f_oh).

![memorial de cálculoo](https://user-images.githubusercontent.com/75510214/101712624-b3acdd80-3a74-11eb-8665-cda093d8e783.png)

 # 2.1.2. _Simulações_

Após encontrar os valores de Resistores (R) e capacitores (C), foi implentados os circuitos.

A Figura 2 mostra a topologia do circuito para a frequencia grave, e na sua resposta para frequência de corte na Figura 3 .

![Filtro p freq grave](https://user-images.githubusercontent.com/75510214/101713258-12bf2200-3a76-11eb-80e7-ebf3858cef55.png)

![figura 3](https://user-images.githubusercontent.com/75510214/101715546-69c6f600-3a7a-11eb-9aa4-680bf8a73847.png)

A Figura 4 apresenta a topologia para o filtro passa banda de frequência média e a Figura 5, sua resposta de frequência de corte.

![figura 4](https://user-images.githubusercontent.com/75510214/101715743-c0343480-3a7a-11eb-85e0-93083fde7448.png)

![fig 5](https://user-images.githubusercontent.com/75510214/101716690-94b24980-3a7c-11eb-8cb3-60964ff9199d.png)

Agora será apresentado o filtro passa banda de frequência aguda na Figura 6 e sua frequência de corte, Figura 7.

![fig 6](https://user-images.githubusercontent.com/75510214/101716924-10ac9180-3a7d-11eb-9682-1e31188d61ad.png)

![fig 7](https://user-images.githubusercontent.com/75510214/101716943-1f934400-3a7d-11eb-8c41-7955209426e7.png)

Após analisar cada circuito separadamente, e confirmar que foram satisfeita as condições iniciais, foi implemantado os circuitos em um amp-op somador, como mostrado na Figura 8, e sua frquência de corte na Figura 9. O circuito utilizou um fonte de sinal de entrada de 500 mV, e amplificadores do tipo 741. Além disso, foram utilizados potenciômetros para realizar o controle de ganho/volume individual e geral. Desse modo, as demais informações constaram no projeto.

![fig 8](https://user-images.githubusercontent.com/75510214/101717114-726cfb80-3a7d-11eb-95c0-0427e64f1fa2.png)

![fig 9](https://user-images.githubusercontent.com/75510214/101717124-78fb7300-3a7d-11eb-8fde-57ef9d994162.png)







