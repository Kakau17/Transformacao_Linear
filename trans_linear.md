# Transformação Linear

\[ T: \mathbb{R}^n \to \mathbb{R}^m \]

A função deve satisfazer adição e multiplicação escalar:

\[ T(u + v) = T(u) + T(v) \]

\[ T(cu) = cT(u) \]

# Matriz de Transformações B e Vetor u

Considere a matriz de transformações \( B \) e vetor \( u \):

\[ B = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} \]

\[ u = \begin{pmatrix} 2 \\ 3 \end{pmatrix} \]

**Calcule \( T(u) \) usando a matriz \( B \).**

Ou seja, multiplicamos \( B \) por \( u \):

\[ T(u) = B \cdot u = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} \begin{pmatrix} 2 \\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\ 18 \end{pmatrix} \]

Portanto, a transformação \( T(u) \) resulta no vetor (8, 18).

# Transformação Linear Simples

Considere a transformação linear dada por:

\[ T \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 2x + 3y \\ 4x + 5y \end{pmatrix} \]

-> Encontre a matriz \( A \) que representa a transformação \( T \):

\[ A = [T(e_1) \quad T(e_2)] \]

mas, antes, como chegar em \( T(e_1) \) e \( T(e_2) \)?

\[ e_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \quad e_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \]

\[ T(e_1) = T \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 2 \cdot 1 + 3 \cdot 0 \\ 4 \cdot 1 + 5 \cdot 0 \end{pmatrix} = \begin{pmatrix} 2 \\ 4 \end{pmatrix} \]

\[ T(e_2) = T \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 2 \cdot 0 + 3 \cdot 1 \\ 4 \cdot 0 + 5 \cdot 1 \end{pmatrix} = \begin{pmatrix} 3 \\ 5 \end{pmatrix} \]

Logo,

\[ A = [T(e_1) \quad T(e_2)] = \begin{pmatrix} 2 & 3 \\ 4 & 5 \end{pmatrix} \]

-> Calcule \( T \begin{pmatrix} 1 \\ 2 \end{pmatrix} \)

\[ A \cdot T \begin{pmatrix} 1 \\ 2 \end{pmatrix} \]

\[ \begin{pmatrix} 2 & 3 \\ 4 & 5 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 2 \cdot 1 + 3 \cdot 2 \\ 4 \cdot 1 + 5 \cdot 2 \end{pmatrix} = \begin{pmatrix} 8 \\ 14 \end{pmatrix} \]

\[ T \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 8 \\ 14 \end{pmatrix} \]

# Rotação

Considere o vetor \( v = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \):

-> Aplique a transformação de rotação \( R(90^\circ) \) ao vetor \( v \). Qual é o novo vetor?

A matriz de rotação é:

\[ R(\theta) = \begin{pmatrix} \cos \theta & -\sin \theta \\ \sin \theta & \cos \theta \end{pmatrix} \]

\[ R(90^\circ) = \begin{pmatrix} \cos 90^\circ & -\sin 90^\circ \\ \sin 90^\circ & \cos 90^\circ \end{pmatrix} \  \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \] 

\[ R(90^\circ) \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \]

\[ R(90^\circ) \begin{pmatrix} 0.1 - 1.0 \\ 1.1 + 0.0 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \]


# Combinação de Transformações

Considere a transformação \( T \) que primeiro translada o vetor \((x, y)\) por \((3, -2)\) e depois rotaciona o vetor resultante por \( 45^\circ \).

1. Escreva a fórmula combinada para a transformação \( T \):

\[ (x', y') = (x + 3, y - 2) \]

Então a fórmula combinada é:

\[ T_{(x', y')} = R(45^\circ) (x + 3, y - 2) \]

2. Aplique \( T \) ao vetor \( v = (1, 1) \) e encontre o vetor resultante:

Primeiro fazemos a translação:

\[ v = (1, 1) \rightarrow (1 + 3, 1 - 2) = (4, -1) \]

Agora, a rotação:

\[ R(45^\circ) \cdot (4, -1) = \begin{pmatrix} \frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} \\ \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} \end{pmatrix} \begin{pmatrix} 4 \\ -1 \end{pmatrix}\]

\[ = \begin{pmatrix} \frac{\sqrt{2}}{2} \cdot 4 - \frac{\sqrt{2}}{2} \cdot (-1) \\ \frac{\sqrt{2}}{2} \cdot 4 + \frac{\sqrt{2}}{2} \cdot (-1) \end{pmatrix} = \begin{pmatrix} \frac{4\sqrt{2}}{2} + \frac{\sqrt{2}}{2} \\ \frac{4\sqrt{2}}{2} - \frac{\sqrt{2}}{2} \end{pmatrix} = \begin{pmatrix} \frac{5\sqrt{2}}{2} \\ \frac{3\sqrt{2}}{2} \end{pmatrix} \]

Logo, o vetor resultante que temos é \( v = (\frac{5\sqrt{2}}{2}, \frac{3\sqrt{2}}{2}) \)


# Autovalores e Autovetores

- Autovetor: vetor que não muda de direção, nem rotaciona. Ele só aumenta ou diminui.
- Autovalor: quanto o vetor aumentou ou diminuiu.

<br>

\[ (x, y) \rightarrow T(x, y) = (x + y, -2x + 4y) \]

##### Verifique se \( \vec{v} = \begin{pmatrix} 1 \\ 2 \end{pmatrix} \) é um autovetor de \( T \):

\[ T \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 1 + 2 \\ -2 \cdot 1 + 4 \cdot 2 \end{pmatrix} = \begin{pmatrix} 3 \\ 6 \end{pmatrix} = 3 \cdot \begin{pmatrix} 1 \\ 2 \end{pmatrix} \]

3 -> autovalor
(1, 2) -> autovetor
Portanto, sim, \( \vec{v} = (1, 2) \) é um autovetor de \( T \).

<br>

##### Encontrar um Autovetor de T

\[ (x, y) \rightarrow T(x, y) = (x + y, -2x + 4y) \]

Vamos imaginar que temos uma transformação representada por uma matriz \(A\):

\[ A = \begin{pmatrix} 1 & 1 \\ -2 & 4 \end{pmatrix} \rightarrow 1x + 1y, -2x + 4y\] 

Precisamos dos autovalores e autovetores:

**1º : Autovalores**

\[ A \cdot \vec{v} = \lambda \cdot \vec{v} \]

\( A \) = matriz transformação
\( v \) = autovetor
\(lambda\) = autovalor


Agora subtraimos \(\lambda\) de \(A\):

\[ A - \lambda I = \begin{pmatrix} 1 - \lambda & 1 \\ -2 & 4 - \lambda \end{pmatrix} \]

(Lembrando que \( I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \))

E calculamos o determinante:

\[ \text{det}(A - \lambda I) = 0 \]

\[ \text{det}\begin{pmatrix} 1 - \lambda & 1 \\ -2 & 4 - \lambda \end{pmatrix} = 0 \]

\[ (1 - \lambda)(4 - \lambda) - (-2 \cdot 1) = 0 \]

\[ \lambda_1 = 3, \quad \lambda_2 = 2 \]

**2º : Autovetores**

Agora, para cada autovalor, encontramos o autovetor correspondente:

Para \(\lambda = 3\):

\[ (A - 3I) \cdot \vec{v} = 0 \]

\[ \begin{pmatrix} 1 - 3 & 1 \\ -2 & 4 - 3 \end{pmatrix} \vec{v} = 0 \]


\[ \begin{pmatrix} -2 & 1 \\ -2 & 1 \end{pmatrix} \vec{v} = 0 \]

(1) \(-2v_1 + v_2 = 0\)
(2) \(-2v_1 + v_2 = 0\)

\(v_2 = 2v_1\)

Agora escolhemos um valor qualquer para \(v_1\) (normalmente se escolhe 1)

\(v_2 = 2 . 1 = 2\)

Logo, um autovetor correspondente é \(\vec{v} = (1, 2)\)

No exercício passado, multiplicamos tudo por \( \frac{1}{2}\) por conveniência:

\(\vec{v} = (\frac{1}{2}, 1)\)

Como conferir:

\(A \cdot \vec{v} = \begin{pmatrix} 1 & 1 \\ -2 & 4 \end{pmatrix} \begin{pmatrix} \frac{1}{2} \\ 1 \end{pmatrix} = \)

\( \begin{pmatrix} \left( 1 \cdot \frac{1}{2} \right) + \left( 1 \cdot 1 \right) \\ \left( -2 \cdot \frac{1}{2} \right) + \left( 4 \cdot 1 \right) \end{pmatrix} = \begin{pmatrix} \frac{3}{2} \\ 3 \end{pmatrix} = 3 \cdot \begin{pmatrix} \frac{1}{2} \\ 1 \end{pmatrix} \)

Lembra que o número em evidência é o autovalor, e a matriz é o autovetor? \(\begin{pmatrix} \frac{1}{2} \\ 1 \end{pmatrix} = (\frac{1}{2}, 1)\), não? Então podemos afirmar que \(\vec{v} = (\frac{1}{2}, 1)\) é um autovetor de \(T\).

<br>

Agora, para \(\lambda = 2\):

\[(A - 2I) \cdot \vec{v} = 0 \]

\[ \begin{pmatrix} 1 - 2 & 1 \\ -2 & 4 - 2 \end{pmatrix} \cdot \vec{v} = 0 \]

\[ \begin{pmatrix} -1 & 1 \\ -2 & 2 \end{pmatrix} \cdot \vec{v} = 0 \]

(1) \(-v_1 + v_2 = 0\)  
(2) \(-2v_1 + 2v_2 = 0\)

(1) \(v_2 = v_1\)

Agora escolhemos um valor qualquer para \(v_1\) (nesse caso, escolhi 1):  
\(v_2 = 1\)

Logo, um autovetor correspondente é: \( \vec{v} = (1, 1) \)

Como conferir:

\(A \cdot \vec{v} = \begin{pmatrix} 1 & 1 \\ -2 & 4 \end{pmatrix} \begin{pmatrix} 1 \\ 1 \end{pmatrix} = \)

\( \begin{pmatrix} \left( 1 \cdot 1 \right) + \left( 1 \cdot 1 \right) \\ \left( -2 \cdot 1 \right) + \left( 4 \cdot 1 \right) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix} = 2 \cdot \begin{pmatrix} 1 \\ 1 \end{pmatrix} \)

Lembra que o número em evidência é o autovalor, e a matriz é o autovetor? \(\begin{pmatrix} 1 \\ 1 \end{pmatrix} = (1, 1)\), não? Então podemos afirmar que \(\vec{v} = (1, 1)\) é um autovetor de \(T\).