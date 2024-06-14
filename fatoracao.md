# Fatoração LU

Use a fatoração LU para resolver o seguinte sistema linear:
\(x_1 + x_2 + x_3 = -2\)
\(2x_1 + x_2 - x_3 = 1\)
\(2x_1 - x_2 + x_3 = 3\)

---

(Caso a explicação abaixo esteja um tanto confusa, tem o pdf "fatoracao.pdf" com a versão colorida e bonitinha.)

---

Primeiro precisamos escrever a matriz \(A\):
\[A = \begin{pmatrix} 1 & 1 & 1 \\ 2 & 1 & -1 \\ 2 & -1 & 1 \end{pmatrix} \cdot \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \\ 3 \end{pmatrix}\]

\[L = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}\]
\[U = \begin{pmatrix} 1 & 1 & 1 \\ 2 & 1 & -1 \\ 2 & -1 & 1 \end{pmatrix}\]

Precisamos que os valores 2,2,−1 virem 0. Para isso, iremos para a fase "Multiplicador".

<br>

### Multiplicador 1
\(m_{21} = \frac{L_{21}}{U_{11}} = \frac{2}{1} = 2\)

(\(U_{21}\)  corresponde ao número que está na 2ª linha da 1ª coluna da matriz \(U\). \(U_{11}\) corresponde ao número que está na 1ª linha da 1ª coluna da matriz \(U\)).

<br>

Agora fazemos a substituição da matriz \(L\):
\(L = \begin{pmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} \)

E voltamos para \(U\):
\(U = \begin{pmatrix} 1 & 1 & 1 \\ 2 - 2(1) & 1 - 2(1) & -1 - 2(1) \\ 2 & -1 & 1 \end{pmatrix} = \begin{pmatrix} 1 & 1 & 1 \\ 0 & -1 & -3 \\ 2 & -1 & 1 \end{pmatrix}\)

2 virou 0. Faltam 2 e -1!

<br>

### Multiplicador 2
\(m_{31} = \frac{L_{31}}{U_{11}} = \frac{2}{1} = 2\)
(\(U_{31}\)  corresponde ao número que está na 3ª linha da 1ª coluna da matriz \(U\). \(U_{11}\) corresponde ao número que está na 1ª linha da 1ª coluna da matriz \(U\)).

Agora fazemos a substituição da matriz \(L\):
\(L = \begin{pmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 2 & 0 & 1 \end{pmatrix}\)


E voltamos para \(U\):
\(U = \begin{pmatrix} 1 & 1 & 1 \\ 0 & -1 & -3 \\ 0 & -3 & -1 \end{pmatrix}\)

2 virou 0! Falta somente -1 (que, agora, virou -3).

<br>

### Multiplicador 3
\(m_{32} = \frac{L_{32}}{U_{22}} = \frac{-3}{-1} = 3\)
(\(U_{32}\)  corresponde ao número que está na 3ª linha da 2ª coluna da matriz \(U\). \(U_{22}\) corresponde ao número que está na 2ª linha da 2ª coluna da matriz \(U\)).


Agora fazemos a substituição da matriz \( L \):
\(L = \begin{pmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 2 & 3 & 1 \end{pmatrix}\)

E voltamos para \(U\):
\(U = \begin{pmatrix} 1 & 1 & 1 \\ 0 & -1 & -3 \\ 0 & 0 & 8 \end{pmatrix}\)

-1 virou 0!! Agora precisamos encontrar \(x_1, x_2, x_3\)!!

<br>

### Encontrando valores de x

\(Ax = b\) (como \( A = LU \), podemos dizer que:)
\(LUx = b\) (vamos trocar \(Ux\) por \(y\), porque os matemáticos fazem assim)

\(Ly = b\)
\(\begin{pmatrix} 1 & 0 & 0 \\ 2 & 1 & 0 \\ 2 & 3 & 1 \end{pmatrix} \begin{pmatrix} y_1 \\ y_2 \\ y_3 \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \\ 3 \end{pmatrix}\)

\(1y_1 + 0y_2 + 0y_3 = -2 \rightarrow y_1 = -2\)
\(2y_1 + 1y_2 + 0y_3 = 1 \rightarrow 2(-2) + y_2 = 1 \rightarrow y_2 = 5\)
\(2y_1 + 3y_2 + 1y_3 = 3 \rightarrow 2(-2) + 3(5) + y_3 = 3 \rightarrow y_3 = -8\)

<br>

\(Ux = y\)
\(\begin{pmatrix} 1 & 1 & 1 \\ 0 & -1 & -3 \\ 0 & 0 & 8 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} -2 \\ 5 \\ -8 \end{pmatrix}\)

\(0x_1 + 0x_2 + 8x_3 = -8 \rightarrow x_3 = -1\)
\(0x_1 - 1x_2 - 3x_3 = 5 \rightarrow -x_2 - 3(-1) = 5 \rightarrow x_2 = -2\)
\(1x_1 + 1x_2 + 1x_3 = -2 \rightarrow x_1 + (-2) + (-1) = -2 \rightarrow x_1 = 1\)

Prontinho! Encontramos \(x_1, x_2, x_3\).


<br>