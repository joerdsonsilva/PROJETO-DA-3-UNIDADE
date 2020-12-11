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

# 1.1. Objetivos Específicos
 O equalizador deve ter 3 estágios, sendo um para frequências graves, um para frequências médias, e um para frequências agudas. A definição das faixas de frequências pode ser observada na Figura 1. Além disso, deve-se ter algum mecanismo de controle de ganho/volume individual (em cada estágio), e um geral (master).
 
![](https://user-images.githubusercontent.com/75510214/101711689-d9d17e00-3a72-11eb-89d7-e5ea764948a4.png)

	
# **2. DESENVOLVIMENTO**

 Um Equalizador permite que você melhore a qualidade de som, ou seja, permite ajustar os níves e efeitos sonoros para assim obter um melhor desempenho dos seus aparelhos eletrônicos, como por exemplo alto-falantes ou fones de ouvidos.
 O projeto tem como finalidade apresentar um equalizador de áudio fácil de usar com o controle de volume individual e um geral, similar ao que acontece na prática.

# 2.1. Memorial Descritivo

 Como mencionado anteriormente, o circuito é constituído por um filtro ativo, do tipo passa banda de segunda ordem, com implementação de amp-op. Dessa forma, para construir a topologia do filtro passa-banda é necessário a junção de dois filtros ativos, o filtro passa-altas e o filtro  passa-baixas, respectivamente nessa ordem a junção. Nesta seção, é apresentado o memorial descritivo da parte teórica, e por fim, os resultados obtidos. 
 
 # 2.1.1. _Memorial de Cálculo_
  
  A topologia do projeto, é composta por três filtros passa banda, um estágio para cada faixa de frequência, ou seja, para as faixas de frequência grave, médias e agudas, conforme mostrado na Figura 1. Sendo implementador em um amp-op somador, com reguladores de ganho individuais e o geral.
  
  A seguir será apresentado o memorial de cálculo, vale destacar que o circuito implementou o circuito denominado _Sallen-Key de componentes iguais_. 
  
  Considerações:
 
 Os amplificadores operacionais (amp-op) também são comumente empregados na construção de filtros ativos. Um circuito de filtro pode ser construído utilizando-se componentes passivos: resistores e capacitores. Além disso, um filtro ativo usa adicionalmente um amplificador para produzir aplicações de tensão e bufferização ou isolação do sinal. Um filtro que apresenta uma resposta constante de CC até uma frequência de corte 𝑓_𝑂𝐻 e impeça que qualquer sinal passe além da frequência é chamado de _filtro passa-baixas_ ideal. Um filtro que permite a passagem somente de sinais de frequência acima de uma frequência de corte 𝑓_𝑂𝐿 é um _filtro passa-altas_. Por fim, quando um circuito permite a passagem de sinais acima de uma frequência de corte e abaixo de uma segunda frequência de corte, é chamado de _filtro passa-banda_.
 
 A seguir os critérios utilizados para as faixas de frequências:

  * Frequência Graves - adotou-se uma faixa de frequência de 20 Hz à 500 Hz, onde 20 Hz é a frequencia de corte do filtro passa-altas (f_OL) e 500 Hz a frequência de corte do filtro passa-baixas (f_OH).
  
  * Frequência Médias - adotou-se uma faixa de frequência de 250 Hz à 4 kHz, onde 250 Hz é a frequencia de corte do filtro passa-altas (f_OL) e 4 kHz a frequência de corte do filtro passa-baixas (f_OH). Como pode-se notar, levou-se em consideração a faixa de frequência de transição entre as frequências.

* Frequência Aguda - adotou-se uma faixa de frequência de 2 kHz à 20 kHz, onde 2 kHz é a frequencia de corte do filtro passa-altas (f_OL) e 20 kHz a frequência de corte do filtro passa-baixas (f_OH).

![memorial de cálculoo](https://user-images.githubusercontent.com/75510214/101712624-b3acdd80-3a74-11eb-8665-cda093d8e783.png)

 # 2.1.2. _Simulações_

Após encontrar os valores de Resistores (R) e capacitores (C), foi implentados os circuitos. A Figura 2 mostra a topologia do circuito para a frequencia grave, e na sua resposta para frequência de corte na Figura 3 .

![FIG 2](https://user-images.githubusercontent.com/75510214/101814172-8b68c180-3afc-11eb-91e9-5c3b05025bb3.png)

![figura 3](https://user-images.githubusercontent.com/75510214/101715546-69c6f600-3a7a-11eb-9aa4-680bf8a73847.png)

A Figura 4 apresenta a topologia para o filtro passa banda de frequência média e a Figura 5, sua resposta de frequência de corte.

![figura 4](https://user-images.githubusercontent.com/75510214/101814182-8dcb1b80-3afc-11eb-9e9a-512f902621fa.png)

![fig 5](https://user-images.githubusercontent.com/75510214/101716690-94b24980-3a7c-11eb-8cb3-60964ff9199d.png)

Agora será apresentado o filtro passa banda de frequência aguda na Figura 6 e sua frequência de corte, Figura 7.

![fig 6](https://user-images.githubusercontent.com/75510214/101814217-991e4700-3afc-11eb-8a4b-178596ce9c3a.png)

![fig 7](https://user-images.githubusercontent.com/75510214/101716943-1f934400-3a7d-11eb-8c41-7955209426e7.png)

Após analisar cada circuito separadamente, e confirmar que foram satisfeita as condições iniciais, foi implemantado os circuitos em um amp-op somador, como mostrado na Figura 8, e sua frquência de corte na Figura 9. O circuito utilizou um fonte de sinal de entrada de 500 mV, e amplificadores do tipo 741. Além disso, foram utilizados potenciômetros para realizar o controle de ganho/volume individual e geral. Desse modo, as demais informações constaram no projeto.

![fig 8](https://user-images.githubusercontent.com/75510214/101814228-9c193780-3afc-11eb-9cdb-ef0fd1b61d36.png)

![fig 9](https://user-images.githubusercontent.com/75510214/101814241-a0455500-3afc-11eb-9a5d-11551c0e8e29.png)

Podemos observa com a figura 9 que, a largura da banda não se mostrou completamente plana mas atende as caracteristicas pedidas no projeto. Temos que um filtro ideal possuiria uma banda passante totalmente plana (figura 1), e iria atenuar completamente todas as frequências fora desta banda, porem na na prática não ocorre dessa forma. A banda passante teve algumas oscilações, porem as frequências de corte das extremidades (que define o limite da banda onde as frequências não são atenuadas) coincidiram para uma respota esperada.

# 2.2 Esquemático do PCB

 A seguir é ilustrado o layout e a PCB em 3D. Vale destacar que durante as simulações do projeto e o  _layout_ da PCB , o _software_ utilizado foi o proteus. 

![Captura de Tela (752)](https://user-images.githubusercontent.com/75510214/101816261-940ec700-3aff-11eb-96b6-e7637389eba6.png)

![Captura de Tela (751)](https://user-images.githubusercontent.com/75510214/101816268-95d88a80-3aff-11eb-9bd1-cb50f33345ab.png)


# 2.3 Lista dos Materiais (BOM)

Nesta seção será apresentado a lista dos materiais, utilizados para elaborar o projeto, bem como seu valor.

Tabela 1 - Lista de Materiais

![tabela 1](https://user-images.githubusercontent.com/75510214/101815480-5fe6d680-3afe-11eb-9aa1-d64833c96633.jpeg)

Fonte dos preços: Bau da eletrônica, Solda Fria, Paresteck e Amazon.

# CONCLUSÃO

A partir das etapas de análise implementadas, foi possível concretizar os objetivos pretendidos com a determinação das faixas de frequências graves, médias e agudas. A análise teórica realizada apresentou resultados convergentes com os obtidos na simulação do circuito. Assim, portanto, a modelagem simplificadora adotada apresenta validade significativa.

# **Anexos**

Nesta seção, será anexado o link com um vídeo explicativo dos integrantes do projeto.

Vídeo de Erika (<https://drive.google.com/file/d/1qVSOvwzjrLqCxzhiHRnqsLTnm3BblINS/view>
<https://drive.google.com/file/d/1W7HToCUN6iWY3q03z0qC4lZ3TPHgU_lA/view>)

Vídeo de Joerdson ( )

Vídeo de Yuri (<https://drive.google.com/file/d/1RKlBarmfgpW-UrKd1QoHDpdVuPZ0AN3d/view?usp=sharing>)

