# CLASSIFICAÇÃO COM RANDOM FORESTS ANALISANDO DADOS DE UMA SEGURADORA

<p align="center">
  <img width="1000" height="400" src="https://i.ytimg.com/vi/goPiwckWE9M/maxresdefault.jpg"/>
</p>


**Aviso:** O seguintes dados foram criados para esse exercício, a empresa não existe, o contexto, o CEO, e as questões de negócios existem apenas para elaboração desse contexto.

# Sobre

Esse projeto é um exercício de treinamento sobre algoritmos random forest classifier, os dados foram criados, e é uma empresa de seguro fictícia. 


# Questão de negócio

A questão do negócio é prever se os novos clientes da seguradora vai acionar o seguro no futuro.



# Planejamento da Solução

Fazer uma análise exploratória inicial com os dados: 

![imagen hist](https://user-images.githubusercontent.com/82332461/141700204-ad899a36-5747-43eb-9512-97bc37804e55.png)


**1- Análise das variáveis serviço e idade:**
 
 
 ![serviçoeidade](https://user-images.githubusercontent.com/82332461/141700326-ae1a59ef-94e6-44b9-879c-46b2fd8660db.png)


O boxplot apresenta a variável 1, 2 e 3 (1 = nunca utilizaram o seguro, 2 = utilizaram algum tipo de serviço e 3 = sofreu algum tipo de furto) no eixo de serviço e um intervalo de idades no eixo idade. A conclusão principal é que tem um volume concentrado no serviço 1 com idade entre 18 anos até 55 anos, o serviço 2 um volume entre 55 anos até 75 anos e o serviço 3 o volume está  entre 40 anos até 65 anos.


**2- Análise das variáveis serviço e preço do seguro:**

![serviçopreçodoseguro](https://user-images.githubusercontent.com/82332461/141700733-0afaa0c9-0ee8-49df-ad61-5fb229d85402.png)


A conclusão principal deste boxplot é um volume concentrado no serviço 1 que os preços são mais baratos e se concentra até R$1000,00, o serviço 2 é o maior volume onde as pessoas já acionaram algum tipo serviço e o serviço 3 o volume mostra que o maiores valores dos seguros estão concentrado nesse tipo de serviço.



**3- Análise das variáveis serviço e CEP:**

![serviçocep](https://user-images.githubusercontent.com/82332461/141701042-8278d881-7390-4314-8a5c-8bd8c88ec8fd.png)


Esse boxplot mostra que o serviço 1 e o serviço 2 os CEP's não tem uma alteração relevante nos dados, já o serviço 3 o volume mostra que existe uma concentração de prestação desse serviço nos CEP’s  entre 1920 até o 19045, o que pode ser um índice grande de furtos na região.


# Treino e Teste


As variáveis para treino foram divididas em 70% e teste 30%, o algoritmo random forest classifier foi colocado como estimators igual a 500. 
O resultado da matriz de confusão foi dada da seguinte maneira:

0 → Nunca usou o seguro;

1 → Usou algum tipo de serviço;

2 → Sofreu algum tipo de furto.

![matriz](https://user-images.githubusercontent.com/82332461/141701493-bd02ca09-422c-4aac-9077-b8b3b162ef09.png)

**Acurácia do Modelo**

                   precision    recall  f1-score   support

               1       0.93      0.93      0.93        68
               2       0.87      0.68      0.76        40
               3       0.82      1.00      0.90        42

        accuracy                           0.88       150
       macro avg       0.87      0.87      0.86       150
    weighted avg       0.88      0.88      0.88       150



# Resultado 

Depois do treino e teste é hora de colocar o modelo para produção da previsão.

E os resultado foi:

1 → Que não vão usar o seguro = 15.

2 → Que vão usar algum tipo de serviço = 5.

3 → Que pode sofrer furto = 1.





 





