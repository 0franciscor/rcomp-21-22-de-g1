RCOMP 2021-2022 Project - Sprint 1 - Member 1201386 Folder
===========================================

## Edifício 1

### Medida do edifício:
- 30m × 20m = 600 metros quadrados

## Edifico 1 - Piso 0

### Medida da escala:

- 5m (real) = 2,7cm (escala)

### Informações Calculadas: 
| Room  |	Comprimento (m) |	Largura (m)	 | Área (m2)  |Quantidade de outlets |
|-------|-------------------|----------------|------------|----------------------|
|1.0.1  |6,6667          	|3,0556     	 |20,3708	  |	6	            	 |
|1.0.2  |6,6667          	|4,4444     	 |29,6295	  |	0	           	     |
|1.0.3  |6,6667          	|4,4444     	 |29,6295	  |	6	            	 |
|1.0.4  |6,6667          	|6,6667     	 |44,4449	  |	10	            	 |
|1.0.5  |5              	|3,0556     	 |15,278	  |	4	            	 |
|1.0.6  |5               	|3,0556     	 |15,278	  |	4	            	 |
|1.0.7  |5               	|3,0556     	 |15,278	  |	4	            	 |
|1.0.8  |5               	|5          	 |25    	  |	6	            	 |
|1.0.9  |4,6296          	|5,9259     	 |27,4345	  |	6	            	 |
|1.0.10 |7,2222          	|5,9259     	 |42,798	  |	10	            	 |

### Plano da Cablagem Estruturada:

![1201386](1201386_Building1_Floor0_Cabos.jpg)

### Justificações Relevantes:
  
#### Outlets

- As áreas comuns, como o átrio de entrada, as casas de banho e as escadas, não
  necessitam de outlets.
  
- A distribuição dos outlets foi realizada tendo em consideração os melhores locais
  para que o room em questão não fosse muito afetado, para que não ficassem próximas de portas
  e para que seja possível com maior facilidade aproveitar o meio da sala para trabalhar.

- No posicionamento dos outlets foi também pensado de modo que entre os mesmos, a distância máxima seja
  de três metros, para que em qualquer parte da sala onde o equipamento do utilizador se encontre
  consiga com o patch cord que é fornecido ter acesso a uma tomada de rede.
  
- A quantidade de outlets por room foi obtida utilizando a proporção de 2 outlets para cada 
  10 metros quadrados de área.

####  Consolidation Points

####  Horizontal cross-connect

- Este piso apresenta apenas um HC, pois este tem uma cobertura de cerca de 1000 metros
  quadrados e o edifício apresenta apenas 600 metros quadrados de área.

####  Intermediate cross-connect

- O datacentre do edifício e do campus está localizado na sala 1.0.2 portanto o Intermediate cross-connect
  foi colocado nesta sala localizado no mesmo armário técnico que o Horizontal cross-connect.

####  Main cross-connect

- O datacentre do edifício e do campus está localizado na sala 1.0.2 portanto o main cross-connect
  foi colocado nesta sala. 
  
- O Main cross-connect é responsável por distribuir para o Intermediate cross-connect deste edifício e dos outros
  a fibra ótica monomodo através da passagem para o exterior, por este motivo do MC sai 1 cabo de fibra ótica monomodo
  que se conecta ao IC deste edifício.
  
- Optou-se que este fica-se no meio da sala para uma melhor manutenção futura.

### Inventário Total Piso 0:

| Equipamento |	Quantidade |
|-------------|------------|
|Outlets	  |	56		   |

## Edifico 1 - Piso 1

### Medida da escala:

- 5m (real) = 2,7cm (escala)

### Informações Calculadas:
| Room  |	Comprimento (m) |	Largura (m)	 | Área (m2)  |Quantidade de outlets |
|-------|-------------------|----------------|------------|----------------------|
|1.1.1  |6,6667          	|3,0556     	 |20,3708	  |	0	            	 |
|1.1.2  |6,6667          	|7,5926     	 |50,6176	  |	12	            	 |
|1.1.3  |6,6667          	|8,5185     	 |56,7903	  |	12	            	 |
|1.1.4  |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.5  |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.6  |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.7  |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.8  |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.9  |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.10 |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.11 |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.12 |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.13 |5               	|2,7778     	 |13,889	  |	4	            	 |
|1.1.14 |7,2222          	|5,9259     	 |42,798	  |	10	            	 |

### Plano da Cablagem Estruturada:

![1201386](1201386_Building1_Floor1_Cabos.jpg)

### Justificações Relevantes:

- A sala 1.1.1 é uma área de armazenamento e não são necessárias tomadas de rede lá,
  e o mesmo aplica-se às casas de banho e a áreas comuns como corredores e átrios.

- Do piso anterior, através de uma calha técnica, 2 cabos de fibra ótica emergem 
  provenientes do IC.

#### Consolidation Points

-
  
####  Horizontal cross-connect

- Este piso apresenta apenas um HC, pois este tem uma cobertura de cerca de 1000 metros
  quadrados e o edifício apresenta apenas 600 metros quadrados de área.

- O HC está localizado na sala 1.1.1 num armário técnico, visto o cliente ter dado a indicação que esta sala
  podia ser usada para abrigar uma cross-connect por ser uma área de armazenamento.

- O HC é responsável pelas salas 1.1.2 e 1.1.3.


### Inventário Total Piso 1:

| Equipamento |	Quantidade |
|-------------|------------|
|Outlets	  |	74		   |

### Inventário Total Do Edifício 

| Equipamento |	Quantidade |
|-------------|------------|
|Outlets	  |	136		   |
