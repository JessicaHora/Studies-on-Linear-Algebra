## Ajustando Polinômios com Numpy

Polinômios são expressões matemáticas com estratégias não negativas. Exemplos de funções polinomiais são **funções lineares**, **quadráticas**, **cúbicas** e **quárticas**. NumPy oferece a **polyfit()**cfunção para gerar polinômios usando mínimos quadrados. Esta função toma coordenada x , coordenada y e grau como parâmetros e retorna uma lista de coeficientes polinomiais.

O NumPy também oferece **polyval()** a avaliação do polinômio em valores dados. Esta função pega coeficientes de polinômios e matrizes de pontos e retorna valores resultantes de polinômios. Outra função é **linspace()**, que gera uma sequência de valores igualmente separados. Ela pega o início, o fim e o número de valores entre o intervalo início-fim e retorna valores igualmente separados no intervalo fechado.

## Determinante
O determinante é o conceito mais essencial da álgebra linear. É um valor escalar que é calculado a partir de uma matriz quadrada. O determinante é uma operação fundamental que nos ajuda na matriz inversa e na resolução de equações lineares. Determinantes são calculados apenas para matrizes quadradas. Uma matriz quadrada tem um número igual de linhas e colunas. O **numpy.linalgsubpacote** fornece a **det()** função para calcular o determinante de uma determinada matriz de entrada. 

## Encontrando a classificação de uma matriz
Rank é um conceito muito importante quando se trata de resolver equações lineares. O rank de uma matriz representa a quantidade de informação que é mantida na matriz. Um rank mais baixo significa menos informação, e um rank mais alto significa uma grande quantidade de informação. **Rank pode ser definido como o número de linhas ou colunas independentes de uma matriz**. O **numpy.linalg** subpacote fornece a **matrix_rank()** função. A **matrix_rank()** função pega a matriz como entrada e retorna o rank computado da matriz.

```
# importar bibliotecas necessárias 
importar numpy como np 
de numpy.linalg importar matrix_rank 

# Criar uma matriz 
mat=np.array([[5, 3, 1],[5, 3, 1],[1, 0, 5]]) 

# Calcular a classificação da matriz 
print("Matriz: \n", mat) 
print("Classificação:",matrix_rank(mat))

```
