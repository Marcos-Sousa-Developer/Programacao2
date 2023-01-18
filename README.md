<p align="center">
    <img src="https://www.pngmart.com/files/3/Chess-PNG-Image.png" alt="Logo" width="80" height="80">
</p>

# <h1 align="center">Analisador de Jogos de Xadrez</h3>
<h4 align="center">Projeto para a cadeira de Programação 2 (2020/2021)</h5>

<hr>

# Objetivo
O objetivo deste trabalho é desenvolver um analisador de jogos de xadrez. O ficheiro xadrez.csv contém informação sobre mais de 100 mil jogos de xadrez jogados pelas melhores jogadora do mundo.

<hr>

# Instruções 

## Operação anos
Tratam-se de dois gráficos sobrepostos na mesma figura, com um eixo das abcissas comum, e dois eixos distintos para as ordenadas, um à esquerda (como habitualmente), e outro à direita.

* Gráfico de barras, onde:
    * As abcissas são os anos (2009, . . . , 2021).
    * As ordenadas são o número de jogos.
* Gráfico de curva, onde:
    * As abcissas são os anos (2009, . . . , 2021).
    * As ordenadas são o número de jogadoras.

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv anos
```

## Operação classes
Gráficos da distribuição de jogos por formato de jogo. Os jogos de xadrez online podem ser jogados com várias restrições de tempo de jogo; dividem-se em 4 classes: rapid, daily, bullet e blitz. <br>
Apresentação por omissão, o top-5 dos formatos mais populares, isto é, dos formatos com maior número de jogos ao longo de todos os anos.
No entanto, caso a opção -c n esteja presente na linha de comandos, o gráfico apresenta as n classes mais populares, isto é, com maior número de
jogos. 

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv classes -c 3'
```

## Função edicoes 
Devolve o número mínimo de operações de edição necessárias para transformar uma palavra na outra 
As operações de edição podem ser as seguintes:
* Inserir uma letra numa qualquer posição 
* Apagar uma letra
* Substituir uma letra por outra letra

Por exemplo, a distância entre 'para' e 'prol' é 3 porque precisamos de três operações para transformar uma na outra, isto é, para -> pra -> pro -> prol. <br>
A informação é representada numa matriz onde cada linha corresponde às letras da 1ª palavra, e as colunas as letras da 2ª palavra. No exemplo dado, a matriz seria inicializada assim: <br>

```     
     p  r  o  l
  [[ 0  1  2  3  4]
 p [ 1  0  0  0  0]
 a [ 2  0  0  0  0]
 r [ 3  0  0  0  0]
 a [ 4  0  0  0  0]]
``` 

Cada ```posição [i][j]``` da matriz irá representar a distância entre as ```palavra1[:i]``` e ```palavra2[:j]```. A solução final depois de preencher a matriz, estará na célula do canto inferior direito.</p> 

É possível preencher a matriz a começar nas linhas acima, da esquerda para a direita.
Para este exemplo a matriz, depois de preenchida, irá ter os seguintes valores:

```   
     p  r  o  l
  [[ 0  1  2  3  4]
 p [ 1  0  1  2  3]
 a [ 2  1  1  2  3]
 r [ 3  2  1  2  3]
 a [ 4  3  2  2  3]]
```

#### **Run it on terminal or open the code (main.py) and test it** 
```bash
python3 -c 'from main import *; print(edicoes("YOUR TEXT HERE", "YOUR TEXT HERE"))'
``` 
## Função sugerir 
Recebe um vocabulário, uma palavra, uma função de distância e um inteiro positivo n de sugestões e devolve uma lista de n palavras do vocabulário mais próximas da palavra dada, de acordo com a função de distância 

#### **Run it on terminal or open the code (main.py) and test it** 
```bash
python3 -c 'from main import *; print(sugerir("YOUR VOCABULARY LIST, "YOUR TEXT HERE", "YOUR DISTANCE FUNCTION", maxSugestoes=5))'
``` 

## Função corretor 
Recebe um vocabulário, um texto, uma função de distância e um inteiro positivo n de sugestões e imprime um relatório com as correções sugeridas 

#### **Run it on terminal or open the code (main.py) and test it** 
```bash
python3 -c 'from main import *; print(corretor("YOUR VOCABULARY LIST, "YOUR TEXT HERE", "YOUR DISTANCE FUNCTION", maxSugestoes=5))'
``` 
