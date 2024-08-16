## Ajustando Polinômios com Numpy

Polinômios são expressões matemáticas com estratégias não negativas. Exemplos de funções polinomiais são **funções lineares**, **quadráticas**, **cúbicas** e **quárticas**. NumPy oferece a **polyfit()**cfunção para gerar polinômios usando mínimos quadrados. Esta função toma coordenada x , coordenada y e grau como parâmetros e retorna uma lista de coeficientes polinomiais.

O NumPy também oferece **polyval()** a avaliação do polinômio em valores dados. Esta função pega coeficientes de polinômios e matrizes de pontos e retorna valores resultantes de polinômios. Outra função é **linspace()**, que gera uma sequência de valores igualmente separados. Ela pega o início, o fim e o número de valores entre o intervalo início-fim e retorna valores igualmente separados no intervalo fechado.

## Determinante
O determinante é o conceito mais essencial da álgebra linear. É um valor escalar que é calculado a partir de uma matriz quadrada. O determinante é uma operação fundamental que nos ajuda na matriz inversa e na resolução de equações lineares. Determinantes são calculados apenas para matrizes quadradas. Uma matriz quadrada tem um número igual de linhas e colunas. O **numpy.linalgsubpacote** fornece a **det()** função para calcular o determinante de uma determinada matriz de entrada. 

## Encontrando a classificação de uma matriz
Rank é um conceito muito importante quando se trata de resolver equações lineares. O rank de uma matriz representa a quantidade de informação que é mantida na matriz. Um rank mais baixo significa menos informação, e um rank mais alto significa uma grande quantidade de informação. **Rank pode ser definido como o número de linhas ou colunas independentes de uma matriz**. O **numpy.linalg** subpacote fornece a **matrix_rank()** função. A **matrix_rank()** função pega a matriz como entrada e retorna o rank computado da matriz.

No código a **matrix_rank()** função de **numpy.linalg** é usada para gerar o posto da matriz.

## Matriz inversa usando NumPy:
Uma matriz é uma sequência retangular de números, expressões e símbolos organizados em linhas e colunas. A multiplicação de uma matriz quadrada e sua inversa é igual à matriz identidade I. Podemos escrevê-la usando a seguinte equação:

$AA^{-1} = I$

O **numpy.linalg** subpacote fornece uma função para uma operação inversa: a **inv()** função. Vamos inverter uma matriz usando o **numpy.linalg** subpacote. Primeiro, criamos uma matriz usando a **mat()** função e então encontramos o inverso da matriz usando a **inv()** função.

## Resolvendo equações lineares usando NumPy

Operações de matriz podem transformar um vetor em outro vetor. Essas operações nos ajudarão a encontrar a solução para equações lineares. NumPy fornece a **solve()** função para resolver equações lineares na forma de **Ax=B**. Aqui, **A é a matriz n*n**, **B é uma matriz unidimensional** e **x é o vetor unidimensional desconhecido**. Também usaremos a **dot()** função para calcular o produto escalar de duas matrizes de números de ponto flutuante.

## Decompondo uma matriz usando SVD

Decomposição de matriz é o processo de dividir uma matriz em partes. Também é conhecido como fatoração de matriz. Existem muitos métodos de decomposição de matriz disponíveis, como **decomposição inferior-superior ( LU )**, **decomposição QR (onde Q é ortogonal e R é triangular superior)**, **decomposição de Cholesky e SVD.**

A autoanálise decompõe uma matriz em vetores e valores. A SVD decompõe uma matriz nas seguintes partes: vetores singulares e valores singulares. A SVD é amplamente usada em processamento de sinais, visão computacional, processamento de linguagem natural ( PNL ) e aprendizado de máquina — por exemplo, modelagem de tópicos e sistemas de recomendação onde a SVD é amplamente aceita e implementada em soluções de negócios da vida real. Dê uma olhada no seguinte:

$$
A = U \Sigma V^T
$$

Aqui, A é uma matriz singular esquerda m x n , Σ é uma matriz diagonal nxn , V é uma matriz singular direita mxn e V T é a transposta de V. O **numpy.linalg** oferece a **svd()** função para decompor uma matriz. 

## Autovetores e autovalores usando NumPy
Autovetores e autovalores são as ferramentas necessárias para entender o mapeamento e a transformação linear. Autovalores são soluções para a equação Ax = λx. Aqui, A é a matriz quadrada, x é o autovetor e λ são autovalores. O numpy.linalgsubpacote fornece duas funções, eig()e eigvals(). A eig()função retorna uma tupla de autovalores e autovetores e eigvals()retorna os autovalores.

Autovetores e autovalores são os fundamentos centrais da álgebra linear. Autovetores e autovalores são usados ​​em SVD, agrupamento espectral e PCA.

calculamos os autovalores usando a **eigvals()** função do **numpy.linalg**. Após executar a decomposição de autovalores, veremos como gerar números aleatórios e uma matriz.

## Gerando números aleatórios
Números aleatórios oferecem uma variedade de aplicações, como simulação de Monte Carlo, criptografia, inicialização de senhas e processos estocásticos. Não é fácil gerar números aleatórios reais, então, na realidade, a maioria das aplicações usa números pseudoaleatórios. Números pseudo são adequados para a maioria dos propósitos, exceto em alguns casos raros. Números aleatórios podem ser gerados a partir de dados discretos e contínuos. A **numpy.random()**função gerará uma matriz de números aleatórios para o tamanho de entrada fornecido da matriz.
- No Notebook foi gerado uma matriz aleatória 3*3 usando a numpy.random.random().
  
## Distribuição binomial

A distribuição binomial modela o número de tentativas repetidas com a mesma probabilidade em cada tentativa. Aqui, cada tentativa é independente e tem dois resultados possíveis — sucesso e fracasso — que podem ocorrer em cada cliente. A fórmula a seguir representa a distribuição binomial:
$$
P(X) = \frac{n!}{(n - X)! \cdot X!} \cdot (p)^X \cdot (q)^{n-X}
$$

Aqui, p e q são as probabilidades de sucesso e fracasso, n é o número de tentativas e X é o número da saída desejada.

O numpy.random subpacote fornece uma binomial()função que gera amostras com base na distribuição binomial para determinados parâmetros, número de tentativas e probabilidade de sucesso. 

Resultado:

 Primeiro criamos o cash_balancearray de tamanho 500 com valores zero e atualizamos o primeiro valor com 500. Então, geramos valores entre 0 e 9 usando a binomial()função. Depois disso, atualizamos o cash_balancearray com base nos resultados de lançamentos de moedas e plotamos o saldo de caixa usando a biblioteca Matplotlib.

Em cada execução, o código gerará resultados diferentes ou caminhadas aleatórias. Se você quiser tornar a caminhada constante, precisará usar o valor da seed na binomial()função. Vamos tentar outra forma de distribuição para o gerador de números aleatórios: distribuição normal.

[imagem]


## Distribuição normal
Distribuições normais ocorrem frequentemente em cenários da vida real. Uma distribuição normal também é conhecida como curva de sino devido ao seu formato característico. A função de densidade de probabilidade modela a distribuição contínua. O numpy.randomsubpacote oferece muitas distribuições contínuas, como beta, gama, logística, exponencial, normal multivariada e distribuição normal. As normal()funções encontram amostras de distribuição gaussiana ou normal.
Resultado:
[imagem]

Aqui, geramos valores aleatórios usando a normal()função do numpy.random e exibimos os valores usando um histograma e gráfico de linhas ou curva de sino ou função de densidade de probabilidade teórica ( PDF ) com média 0 e desvio padrão de 1.

## Testando a normalidade dos dados usando SciPy

Uma distribuição normal é comumente usada em larga escala em operações científicas e estatísticas. Conforme o teorema do limite central, conforme o tamanho da amostra aumenta, a distribuição da amostra se aproxima de uma distribuição normal. A distribuição normal é bem conhecida e fácil de usar. Na maioria dos casos, é recomendado confirmar a normalidade dos dados, especialmente em métodos paramétricos, assumindo que os dados são distribuídos gaussianamente. Existem muitos testes de normalidade na literatura, como o teste de Shapiro-Wilk, o teste de Anderson-Darling e o teste de D'Agostino-Pearson. O **scipy.stats**  oferece a maioria dos testes de normalidade.
 - No notebook foi  usado três amostras de dados aleatórios de tamanho pequeno, médio e grande para gerar as amostras de dados para todas as três amostras usando a função **normal()**

# Técnicas para verificar a normalidade dos dados:

1. Usando um histograma: Um histograma é o método mais fácil e rápido para verificar a normalidade dos dados. Ele divide os dados em compartimentos e conta a observação em cada compartimento. Finalmente, ele visualiza os dados. Foi usado  **distplot()** da seaborn biblioteca para plotar o histograma e a estimativa da densidade do kernel.

Resultando na seguinte saida:
 ![imagem]

 - exemplo do histograma para uma amostra média, como segue:
  ![imagem]

  - exemplo do histograma para uma amostra grande:
  

  Nos três gráficos anteriores, podemos observar que, à medida que o tamanho da amostra aumenta, a curva se torna uma curva normal. Histogramas podem ser uma boa ferramenta para testar a normalidade dos dados.

  2. Teste de Shapiro-Wilk: Este teste é usado para avaliar a normalidade dos dados. Em Python, a **shapiro()**  do scipy.stats  pode ser usada para avaliar a normalidade. A **shapiro()** função retornará tuplas de dois valores: **estatísticas de teste e valor-p.** 
   
   

## Criando uma  masked array usando o numpy.ma

Na maioria das situações, os dados da vida real são barulhentos e confusos. Eles contêm muitas lacunas ou caracteres ausentes nos dados. Masked arrays são úteis nesses casos e lidam com o problema. masked arrays  podem conter valores inválidos e ausentes. O **numpy.ma** oferece toda a funcionalidade necessária para a matriz mascarada. 

No codigo no notebook foi usado a imagem facial como a fonte da imagem original e executado operações de máscara de log. Resultando na seguinte saida:

- primeiro carregamos a imagem do rosto do **scipy.misc** e criamos uma máscara aleatória usando a **randint()** função. 
- aplicamos a máscara aleatória na imagem do rosto.
- aplicamos a operação de log na imagem do rosto original e na imagem do rosto mascarada. 
- Finalmente, exibimos todas as imagens em subplots 2*2. 
  
  
O foco foi apenas na operação de log do array mascarado. 