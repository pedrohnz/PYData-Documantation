#       Guia Data Science

### Instalações 

- [x] Python 3.8;
- [x] Jupyter;
- [x] Visual Studio Code;

### Listas

`
lista1 = [1,2,3]
` 
- Um array comum

Lista complexa :
`
lista2 = [
    [1,2,3],
    [4,5,6],
    [7,8,9]
]
` 
- Uma matrix com colunas e linhas :

Linhas x Colunas:

 1 2 3 
 4 5 6 
 7 8 9 


### Colocando dentro de uma matriz (append)
```Python
- Inicializando a matriz: 
nomes = [["Pedro","João","Guilherme"],["Julia","Milena","Vitória"]]

- Dados a serem adicionados
idades = [[14,12,8],[14,15,14]]

- Adicionando os dados
for i in idades:
    nomes.append(i)

```

### Transformando listas floats em int (append to float)
```Python
-Inicializando uma lista
x = [14,21,23]
-Inicilizando a lista que vai virar float
new = []

for i in x:
    new.append(float(i))  - Transformando os intengers em flaoters

```

### Dicionários
- São listas com chave: valor (JSON)
```Python
dicionario = {
    "Guia" : "Python para ML",
    "Pessoa" : "Pedro Henrique",
    "Idade" : 14
}
- Para recolher um valor usasse a chave
print(dicionario['Guia']) 
- Variavel que recebe a uma chave , tera o valor
da mesma chave!
a = dicionario['Idade']
print(a)
- Input = [  a = 14   ]
- Adicionar valor a um dicionario:
dicionario["Dia"] = "16/09"
- Para saber quais são as chaves:
dicionario.keys()
- Para saber quais são os valores:
dicionario.values()
```

### Manipulando strings

```Python
frase = "Estou gostando do curso"
- Pegar um caractere da string
frase[2]
- Pegar de um a outro caractere da string
frase[2:6]
- Pegar de um ao resto da string
frase[5:]
- Saber quantos tem de algum caractere na string
print(frase.count('t'))
- O tanto de caracteres da string
len(frase)
- Recolocar caracteres da string
frase.replace('curso','aprender')
```
### Funções lambda(anonimas)
```Python
- Função normal longa
def somaQuadrados(a, b):
    somaQ = a**2 + b**2
    return somaQ

somaQuadrados(2,3)

- Função lambda parametros : retorno
somaQuadradosLambda = lambda a,b: a**2 + b**2

somaQuadradosLambda(2,3)

```

### Mapeamento 
```Python
kph = [40,57,50,60,20,10,64,61,21,100]
-Função para converter map(converter)
mph = map(lambda x: x/1.61,kph)
list(mph)
- Resumo : o map pega uma lista/tupla e converte
para o que o usuario necessitar
```
### Numpy
```Python
import numpy as np
- Cria array do numpy (Ele é automaticamente mais rapido que do python normal)
a = np.array([1,2,3])
- Array multidimensional
b = np.array([(2,5,7),(7,6,8),(10,2,5)])
print(b)
- Criar array de zeros com 4 linhas e 3 colunas
c = np.zeros((4, 3))
#print(c)
- Criar array com 20 linhas e 20 colunas
d = np.eye(20)
#print(d)
- Somar um array
b.sum()
- Media de um array
b.mean()
- Linha de um array
b.std()
```
### Pandas

```Python
import pandas as pd
- Variavel com função para ler um arquivo com da-
dos (execel, apis , csv)
teste = pd.read_csv('C:/home/pedroh/Data/Python/excel/athlete_events.csv')
- Pegar os 5 primeiros dados da tabela
teste.head(5)
- Output :
	ID	Name	Sex	Age	Height	Weight	Team	NOC	Games	Year	Season	City	Sport	Event	Medal
0	1	A Dijiang	M	24.0	180.0	80.0	China	CHN	1992 Summer	1992	Summer	Barcelona	Basketball	Basketball Men's Basketball	NaN
1	2	A Lamusi	M	23.0	170.0	60.0	China	CHN	2012 Summer	2012	Summer	London	Judo	Judo Men's Extra-Lightweight	NaN
2	3	Gunnar Nielsen Aaby	M	24.0	NaN	NaN	Denmark	DEN	1920 Summer	1920	Summer	Antwerpen	Football	Football Men's Football	NaN
3	4	Edgar Lindenau Aabye	M	34.0	NaN	NaN	Denmark/Sweden	DEN	1900 Summer	1900	Summer	Paris	Tug-Of-War	Tug-Of-War Men's Tug-Of-War	Gold
4	5	Christine Jacoba Aaftink	F	21.0	185.0	82.0	Netherlands	NED	1988 Winter	1988	Winter	Calgary	Speed Skating	Speed Skating Women's 500 metres	NaN

- Inicializando um dicionario
alunos = {'Nome' : ['Ricardo','Pedro','Roberto','Carlos'],
         'Nota' : [4,10,5.5,8],
         'Aprovado' : ['Não','Sim','Não','Sim']}
- Criando uma tabela de dados(dataframe) apartir
do dicionario
dataframe = pd.DataFrame(alunos)

print(dataframe)
- Output:
Nome  Nota Aprovado
0  Ricardo   4.0      Não
1    Pedro  10.0      Sim
2  Roberto   5.5      Não
3   Carlos   8.0      Sim

- Pegando os primeiros numeros do novov dataframe
dataframe.head()

- Output :
Nome	Nota	Aprovado
0	Ricardo	4.0	Não
1	Pedro	10.0	Sim
2	Roberto	5.5	Não
3	Carlos	8.0	Sim

- Mostrar quantas colunas X linhas tem:
dataframe.shape
- Mostrar sobre os dados númericos a média , percentil , mediana , etc...
dataframe.describe()
- Ver uma coluna de dados do dataframe
dataframe['Coluna']
- Procurar dado no dataframe
dataframe.loc[[1]]
- Output :
Nome	Nota	Aprovado
1	Pedro	10.0	Sim
- Procurar por string
dataframe.loc[dataframe['Aprovado'] == "Não"]
- Output :
Nome	Nota	Aprovado
0	Ricardo	4.0	Não
2	Roberto	5.5	Não

- Renomear colunas de um dataframe  
                    - Nome da coluna : Substituição     ,      Para não mostrar apenas mudar
teste.rename(columns={'Name':'Nome','Sex':'Sexo','Age':'Idade'}, inplace=True)
- Remover uma coluna do dataframe
            - Coluna , axis=1 == Coluna
teste.drop('ID',axis=1,inplace=True)

```

### Plots
```Python
import matplotlib.pyplot as plt
- Criar histograma coluna X linhas
dt.hist(column='Idade',bins=10)
- Mostrar grafico
plt.show()
```
![Hist](https://github.com/pedrohnz/PYData-Documantation/blob/master/histograma.png)
```Python
- Criar grafico de caixa
dt.boxplot(column='Idade')
plt.show()
```
![Box](https://github.com/pedrohnz/PYData-Documantation/blob/master/boxplot.png)
```Python
x = [1,2,3,4,5,6,7,8,9,10]
y = [1,2,3,4,5,6,7,8,9,10]
- Grafico de pontos de x a y
plt.scatter(x,y)
plt.show()
```
![Ponto](https://github.com/pedrohnz/PYData-Documantation/blob/master/pontos.png)
```Python
import numpy as np 
- Criar array de 0 a 1000 de 1 em 1
x1 = np.arange(0,1000,1)
- Plotar o array de x1 a x1**2
plt.plot(x1,x1**2)
plt.show()
```
![Plot](https://github.com/pedrohnz/PYData-Documantation/blob/master/plot.png)
