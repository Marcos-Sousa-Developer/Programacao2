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

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv anos
```

## Operação classes
Gráficos da distribuição de jogos por formato de jogo. Os jogos de xadrez online podem ser jogados com várias restrições de tempo de jogo; dividem-se em 4 classes: rapid, daily, bullet e blitz. <br>
Apresentação por omissão do top-5 dos formatos mais populares, isto é, dos formatos com maior número de jogos ao longo de todos os anos.
No entanto, caso a opção -c n esteja presente na linha de comandos, o gráfico apresenta as n classes mais populares, isto é, com maior número de
jogos. 

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv classes -c 3
```

## Operação vitorias 
Gráfico de barras em que as abcissas são os nomes das jogadoras e as ordenadas são as percentagens de vitórias quando o jogo se inicia com as peças brancas e quando se inicia com as peças pretas.
Este gráfico mostra, por omissão, dados referentes apenas às cinco jogadoras com mais jogos jogados. A opção -c n controla o número de
jogadoras a apresentar.
Em alternativa à opção -c, este comando aceita uma outra opção, -u u1 . . . un , que permite especificar os nomes das n jogadoras a comparar com nomes de utilizador u1 , . . . , un .

#### **Run it on terminal or open the code (main.py) and test it** 
```bash
python3 projeto.py xadrez.csv vitorias -u budu44 advantagelucy
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
