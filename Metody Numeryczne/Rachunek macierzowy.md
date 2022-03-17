### Macierze dolno i górnotrójkątne
![[Pasted image 20220317111339.png]]

### Macierz hermitowska
$H$ - sprzężenie macierzy

Spełnia równanie $A^H=A$

![[Pasted image 20220317111453.png]]
### Normy macierzy i wektorów
Jest to nieujemna liczba określająca długość. Oznaczamy jako $\parallel ... \parallel$

![[Pasted image 20220317111814.png]]
![[Pasted image 20220317112127.png]]

Norma kolumnowa (macierzowa $L_1$) - w każdej kolumnie policz normę wektora i największa z nich będzie normą macierzy.

Norma spektralna (macierzowa $L_2$) - największa co do modułu wartość własna macierzy ( $\det{(A - \lambda I)}=\sigma$ )

### Promień spektralny macierzy
Największa co do modułu wartość własna macierzy. (nie to samo co $L_2$)

### Współczynnik uwarunkowania macierzy
$$Cond(A)=\| A^{-1} \| * \| A \|$$
$$Cond(A)=\frac{\sup\sqrt{\sigma_i}}{\inf\sqrt{\sigma_i}}, \sigma_i \epsilon Spect(A^TA)$$
$$A=A^T \Rightarrow Cond=\frac{\sup\sigma_i}{\inf \sigma_i}, \sigma_i \epsilon Spect(A)$$
![[Pasted image 20220317114037.png]]
