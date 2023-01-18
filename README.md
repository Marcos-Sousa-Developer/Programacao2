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
Mostra dois gráficos sobrepostos na mesma figura, com um eixo das abcissas comum, e dois eixos distintos para as ordenadas, um à esquerda (como habitualmente), e outro à direita. 

* Gráfico de barras onde as abcissas são os anos (2009, . . . , 2021) e as ordenadas são o número de jogos (representado á esquerda). 
* Curva em que as abcissas são as mesmas do gráfico anterior, isto é, o valor dos anos, e as ordenadas são o número de jogadoras (representado á direita). 

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv anos
```

## Operação classes
Mostra gráficos da distribuição de jogos por formato de jogo. Os jogos de xadrez online podem ser jogados com várias restrições de tempo de jogo; dividem-se em 4 classes: rapid, daily, bullet e blitz. <br>
Cada uma destas classes tem vários formatos,representando o tempo para cada jogador, como por exemplo: 180 (cada jogador tem 180 segundos, ou seja, três minutos), 600+2 (cada jogador tem 600 segundos, ou seja, dez minutos, com incrementos de dois segundos a cada
jogada), 1/259200 (cada jogador tem três dias para fazer o próximo lance). <br>
Apresenta-se por omissão o top-5 dos formatos mais populares, isto é, dos formatos com maior número de jogos ao longo de todos os anos.
No entanto, caso a opção -c n esteja presente na linha de comandos, o gráfico apresenta as n classes mais populares, isto é, com maior número de
jogos. 

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv classes -c 3
```

## Operação vitorias 
Gráfico de barras em que as abcissas são os nomes das jogadoras e as ordenadas são as percentagens de vitórias quando o jogo se inicia com as peças brancas e quando se inicia com as peças pretas. <br>
Este gráfico mostra, por omissão, dados referentes apenas às cinco jogadoras com mais jogos jogados. A opção -c n controla o número de
jogadoras a apresentar. <br>
Em alternativa à opção -c, este comando aceita uma outra opção, -u u1 . . . un , que permite especificar os nomes das n jogadoras a comparar com nomes de utilizador u1 , . . . , un .

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv vitorias -u budu44 advantagelucy
``` 
As opções -c e -u não podem ser utilizadas em conjunto.

## Operação seguinte 
Mostra um gráfico de barras das top-5 jogadas mais prováveis após uma dada jogada. A jogada por omissão é e4 (que corresponde
a avançar o peão de rei duas casas). Neste caso ficamos a saber que, após a jogada e4, as jogadas mais comuns são: c5 (avançar o peão da coluna c duas
casas; a chamada defesa siciliana), e5 (avançar o peão de rei duas casas), e6 (avançar o peão de rei uma casa), c6 (avançar o peão da coluna c uma casa) e Nf6 (mover o cavalo de rei para f6). <br>
A jogada a considerar pode ser passada na  linha de comandos, como opção. Por exemplo, -j e4 indica que o gráfico irá apresentar as jogadas mais prováveis que sucedem à jogada e4. <br>
À semelhança do caso anterior, este comando mostra por omissão o top-5 das jogadas mais comuns e aceita a opção -c n para especificar o número de jogadas n a considerar.

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv seguinte -j e4'
```  
ou 

```bash
python3 projeto.py xadrez.csv seguinte
``` 

## Operação mate 
Mostra dois gráficos, com um eixo das abcissas comum representando o nome das jogadoras e dois eixos de ordenadas distintos. <br>
Do lado esquerdo temos o eixo do número de jogos, que corresponde às ordenadas do gráfico de barras e que mostra o número de jogos ganhos por
xeque-mate e o número de jogos ganhos de qualquer modo. <br>
Do lado direito temos o eixo das ordenadas, correspondente à curva das percentagens de jogos ganhos por xeque-mate. <br>
À semelhança de gráficos anteriores, este comando mostra por omissão as 5 jogadoras com mais jogos ganhos. A opção -c n especifica o número de
jogadoras a mostrar.

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv mate
``` 

## Comando extrair 
Este comando extrai informação do ficheiro original para um outro ficheiro csv.
* A opção -o nome_ficheiro especifica o nome do ficheiro a criar com os novos dados. O valor por omissão é out.csv. Se este ficheiro já existir,
o seu conteúdo deverá ser rescrito. 
* A opção -r expressão_regular identifica as linhas de interesse. O seu valor por omissão é '.*'
* A opção -d coluna indica a coluna na qual a expressão regular é testada. O valor por omissão é wgm_username.

#### **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv extrair -r '2020' -d end_time
``` 
#### Outro exemplo **Run it on terminal** 
```bash
python3 projeto.py xadrez.csv extrair -r '^a' -o xadrez_a.csv
``` 
Todos os gráficos descritos acima podem ser gerados a partir de ficheiros produzidos por este comando (em vez de usar o ficheiro xadrez.csv com
todos os jogos). 

#### **Run it on terminal** 
```bash
python3 rojeto.py out.csv vitorias
``` 

