# 2. Klausur 
## Altfragen
### 2019
1. Zeigen Sie die Quellfreiheit des Magnetfelds $B^{i}\left(x^{m}\right)$ unter Verwendung des Amperéschen Ausdrucks, welcher $B^{i}\left(x^{m}\right)$ in Abhängigkeit von der Volumsstromdichte $J^{i}\left(x^{m}\right)$ darstellt.
2. Für zwei Flächen $F_{1}, F_{2}$, welche durch dieselbe Kurve $\gamma$ berandet wer$\operatorname{den}\left({\mathrm{d} . \mathrm{h} . \partial F_{1}=\partial F_{2}=\gamma}\right.$ ), weise man die Gleichheit des magnetischen Flusses durch diese Flächen, unter Verwendung der magnetostatischen Maxwellgleichungen, nach.

###  2013
1. Zeigen Sie unter Zuhilfenahme des Biot-Savart'schen Ausdrucks für das Magnetfeld $B^{i}\left(x^{m}\right)$ in Abhängigkeit von der Volumsstromdichte $J^{i}\left(x^{m}\right)$ die Divergenzfreiheit von $B^{i}\left(x^{m}\right)$.

2. Unter Verwendung der magnetostatischen Maxwellgleichungen bestimme man die Rotation der Volumsstromdichte $J^{i}\left(x^{m}\right)$. Den so gewonnen Ausdruck löse man nach $B^{i}\left(x^{m}\right)$ unter Zuhilfenahme der Green-Funktion des Laplace-Operators auf.

###  2013 Ersatztest
1. Unter Verwendung des Biot-Savart'schen Ausdrucks für das Magnetfeld $B^{i}\left(x^{m}\right)$ in Abhängigkeit von der Volumsstromdichte $J^{i}\left(x^{m}\right)$ zeige man die Abwesenheit von magnetischer Ladung.

2. Zeigen Sie unter Verwendung der zweiten magnetostatischen Maxwellgleichung, dem Ampéreschen Gesetz, die Divergenzfreiheit der Stromdichte $J^{i}\left(x^{m}\right)$

###  2011 
 1. Weisen Sie die Quellfreiheit des magnetischen Feldes, unter Benutzung des Biot-Savart'schen Ausdrucks für das Magnetfeld $B^{i}\left(x^{m}\right)$ in Abhängigkeit von der Volumsstromdichte $J^{{i}}\left(x^{m}\right)$, nach.

2. Zeigen Sie, dass die stationäre (zeitunabhängige) Kontinuitätsgleichung eine direkte Konsequenz des Ampere'schen Gesetzes zwischen Magnetfeld $B^{i}\left(x^{k}\right)$ und Volumsstromdichte $J^{\prime}\left(x^{k}\right)$ darstellt.


## Formelsammlung 

### Gegenüberstellung der Maxwellgleichungen
| |Magnetostatik|Elektrostatik|
|---|:---:|:---:|
|1.MG|$\varepsilon_{ijk}\partial_j B^k(x^m)=\mu_0 J^i(x^m)$|$\partial_i E^i(x^m) = \frac{\rho(x^m)}{\varepsilon_0}$|
|2.MG|$\partial_i B^i(x^m) =0$|$\varepsilon_{ijk} \partial_j E^k (x^m)=0$|

### Kraftgesetze 

Ampèresches Kraftgesetz:
$$F_{12}^i=\frac{\mu_0}{4\pi}\int ds_1\,  \varepsilon_{ijk}\, I^j_1(s_1) \int d s_2 \, \frac{e_{klm}\, I^l_2 (s_2) \left(x^m_1(s_1)-x_2^m (s_2)\right)}{\lvert x_1^p(s_1)-x_2^p(s_2)\rvert^3}$$
Coulombsches Kraftgesetz:
$$F_{12}^i = \frac{1}{4\pi\varepsilon_0} \frac{q_1 q_2 (x_1^i-x_2^i)}{\lvert x_1^m-x_2^m\rvert^3}$$

### Magnetfeld mittels  Ampèrescher Ausdruck 

$$\begin{aligned}B^i(x^m) &= \frac{\mu_0}{4\pi} \int d^3 x' \frac{\varepsilon_{ijk}\, J^j(x'^m)(x^k-x'^k)}{\lvert x^m-x'^m\rvert^3} = \\&=\underbrace{\varepsilon_{ijk}}_{\varepsilon_{ikj}}(-\partial_k) \underbrace{\left( \int d^3 x' \frac{J^j(x'^m)}{\lvert x^m-x'^m \rvert} \frac{\mu_0}{4\pi}\right)}_{A^j(x^m)}=\varepsilon_{ikj}\partial_kA^j(x^m)\\\Rightarrow \partial_i B^i(x^m) &= \underset{\vee}{\varepsilon_{ijk}} \underset{\cup}{\partial_i \partial_j}A^k(x^m)=0\end{aligned}$$

### E-feld mittels  Coulombscher Ausdruck 

$$\begin{aligned}E^i(x^m)&=\frac{1}{4\pi\varepsilon_0}\int d^3x' \frac{\rho(x'^m)(x^i-x'^i)}{\lvert x^m-x'^m\rvert^3} =\\&= - \partial_i \underbrace{\left(\frac{1}{4\pi\varepsilon_0} \int d^3 x' \frac{\rho(x'^m)}{\lvert x^m -x'^m\rvert}\right)}_{ := V(x^m)}=\\&=-\partial_i V(x^m)\\\Rightarrow \varepsilon_{ijk}\,\partial_j E^k&(x^m)=\underset{\vee}{\varepsilon_{ijk}} \underset{\cup}{\partial_i \partial_j}V(x^m)=0\end{aligned}$$
