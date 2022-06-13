## 0. Allgemeine Formeln
### Ampérescher Ausdruck für das Magnetfeld
$$B_i(x_m)=\frac{\mu_0}{4\pi}\int_{wire}d^3x'\,\frac{\epsilon_{ijk}J_i(x_m')(x_k-x_k')}{|x_m-x_m'|^3}$$

### Ampéresches Gesetz in Integralform
$$\oint_C\boldsymbol{B}\cdot dl=\mu_0\int_S\boldsymbol{J}\cdot d\boldsymbol{A}=\mu_0\cdot I_{enclosed}$$

### Biot-Savart'scher Ausdruck für das Magnetfeld
$$\boldsymbol{B}(\boldsymbol{x})=\frac{\mu_0}{4\pi}\int_{wire}d^3x'\,\frac{I\,dl\times\boldsymbol{\hat{r}}}{r^2}=\frac{\mu_0}{4\pi}\int_{wire}d^3x'\,\frac{I\,dl\times(\boldsymbol{x}-\boldsymbol{x}')}{|\boldsymbol{x}-\boldsymbol{x}'|^3}$$

### Green'sche Funktion des Laplaceoperators
$$G=-\frac{1}{4\pi}\int d^3x'\frac{1}{|x_m-x_m'|}$$

---

## 1. Magnetostatische Maxwell-Gleichungen
### 1. Maxwell-Gleichung
#### Elektrostatik
$$\boldsymbol{\nabla}\cdot \boldsymbol{E}=\partial_iE_i(x_m)=\frac{\rho(x_m)}{\epsilon_0}$$

#### Magnetostatik
$$\boldsymbol{\nabla}\times\boldsymbol{B}=\epsilon_{ijk}\partial_jB_k(x_m)=\mu_0\cdot J_i(x_m)$$

### 2. Maxwell-Gleichung
#### Elektrostatik
$$\boldsymbol{\nabla}\times\boldsymbol{E}=\epsilon_{ijk}\partial_jE_k(x_m)=0$$

#### Magnetostatik
$$\boldsymbol{\nabla}\cdot\boldsymbol{B}=\partial_iB_i(x_m)=0$$

---

## 2. Nabla Rechenregeln
1. $\boldsymbol{\nabla}\cdot\boldsymbol{\nabla}=\boldsymbol{\nabla}^2=\boldsymbol{\Delta}$
2. $\boldsymbol{\nabla}\times\left(\boldsymbol{\nabla}\times\boldsymbol{A}\right)=\boldsymbol{\nabla}\left(\boldsymbol{\nabla}\cdot\boldsymbol{A}\right)-\boldsymbol{\nabla}^2\boldsymbol{A}$
3. $\boldsymbol{\nabla}\cdot\left(\boldsymbol{\nabla}\varphi\right)=\boldsymbol{\nabla}^2\varphi$
4. $\boldsymbol{\nabla}\cdot\left(\boldsymbol{\nabla}\times\boldsymbol{A}\right)=0$
5. $\boldsymbol{\nabla}\times\left(\boldsymbol{\nabla}\varphi\right)=0$

---

## 3. Quellenfreiheit des magnetischen Feldes
> Zeigen Sie die Quellfreiheit des Magnetfelds $B_i(x_m)$ unter Verwendung des Amperéschen Ausdrucks, welcher $B_i(x_m)$ in Abhängigkeit von der Volumsstromdichte $J_i(x_m)$ darstellt.

Die Quellenfreiheit des magnetischen Feldes $\boldsymbol{B}$ ist über den magnetischen Hüllenfluss definiert. Dieser besagt, dass der durch eine geschlossene Fläche austretende magnetische Fluss zu jedem Zeitpunkt gleich Null sein muss:
$$\oint_{\partial V}\boldsymbol{B}\cdot dA=0$$
Der Gauß'sche Integralsatz besagt, dass für ein vom Rand $\partial V$ eingeschlossenes Volumen $V$, für ein beliebiges Vektorfeld $\boldsymbol{B}$, geschrieben werden kann:
$$\int d^3V\partial_iB_i=\oint_{\partial V}dA_iB_i$$
Somit kann die Quellenfreiheit des magnetischen Feldes $\boldsymbol{B}$ wie folgt beschrieben werden:
$$\oint_{\partial V}\boldsymbol{B}\cdot dA=\int_V\text{div }\boldsymbol{B}\cdot dV=0$$
In differentieller Form entspricht dieser Zusammenhang:
$$\text{div }\boldsymbol{B}=0$$

---

Das Magnetfeld $\boldsymbol{B}$ kann über den Ampéreschen Ausdruck, welcher das magnetische Feld $\boldsymbol{B}$ in Abhängigkeit von der elektrischen Stromdichte $\boldsymbol{J}$ definiert, angeschrieben werden:
$$B_i(x_m)=\frac{\mu_0}{4\pi}\cdot\int d^3x'\,\frac{\epsilon_{ijk}\cdot J_i\cdot\left(x_k-x_k'\right)}{|x_m-x_m'|^3}$$
Für später wird die folgende Nebenrechnung benötigt:
$$\partial_k\frac{1}{\underbrace{|\boldsymbol{x}_m-\boldsymbol{x}_m'|}_{\text{Abstand}}}=\partial_k\frac{1}{|\boldsymbol{x}|}=\partial_k\frac{1}{\sqrt{\boldsymbol{x}^2}}=\underbrace{-\frac{1}{2}\cdot\frac{1}{{\sqrt{\boldsymbol{x}^{2}}}^3}}_{\text{äußere Ableitung}}\cdot\partial_k\boldsymbol{x}^2=-\frac{1}{\cancel{2}}\cdot\frac{1}{\sqrt{{\boldsymbol{x}^{2}}}^3}\cdot\underbrace{\cancel{2}\cdot\boldsymbol{x}}_{innere Ableitung}\cdot\delta_{km}$$
$$=-\frac{\boldsymbol{x}_m-\boldsymbol{x}_m'}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|^3}\cdot\delta_{km}=-\frac{\boldsymbol{x}_k-\boldsymbol{x}_k'}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|^3}$$
Aus der Nebenrechnung lässt sich demnach ablesen:
$$-\boldsymbol{\nabla}\frac{1}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|}=\frac{\boldsymbol{x}_k-\boldsymbol{x}_k'}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|^3}$$
Dieser Zusammenhang lässt sich nun in den Ampéreschen Ausdruck für das magnetische Feld $\boldsymbol{B}$ einsetzen:
$$B_i(x_m)=\frac{\mu_0}{4\pi}\cdot\int d^3x'\,\epsilon_{ijk}\cdot J_i\cdot\left(-\partial_k\frac{1}{|x_m-x_m'|}\right)$$
Das Kreuzprodukt $\epsilon_{ijk}$ sowie die Ableitung $\partial_k$ können aus der Integration heraus gehoben werden, nachdem sie nicht von $x'$ abhängig sind. Dadurch folgt:
$$B_i(x_m)=\epsilon_{ijk}\cdot\left(-\partial_k\right)\cdot\underbrace{\left(\frac{\mu_0}{4\pi}\cdot\int d^3x'\,\frac{J_i}{|x_m-x_m'|}\right)}_{=A_j\left(x_m\right)}$$
Der hintere Teil der Gleichung entspricht nun dem magnetischen Vektorpotential $\boldsymbol{A}$. Demnach kann der Ausdruck wie folgt vereinfacht werden:
$$B_i(x_m)=\epsilon_{ijk}\cdot\left(-\partial_j\right)\cdot A_k\left(x_m\right)$$

---

Wie bereits in der Einleitung des Beispiels beschrieben, muss für die Quellenfreiheit des magnetischen Feldes $\boldsymbol{B}$ in differentieller Form gelten:
$$\text{div }\boldsymbol{B}=\partial_iB_i(x_m)=0$$
Eingesetzt folgt entsprechend:
$$\partial_iB_i(x_m)=\partial_i\epsilon_{ijk}\partial_jA_k(x_m)=\epsilon_{ijk}\partial_i\partial_jA_k(x_m)$$
Setzt man die Symmetrien der einzelnen Ausdrücke ein, kann geschrieben werden:
$$\partial_iB_i(x_m)=\underset{\vee}{\epsilon_{ijk}}\underset{\cup}{\partial_i\partial_j}A_k(x_m)$$
Mit:
$$\vee\rightarrow\text{antisymmetrisch}$$
$$\cup\rightarrow\text{symmetrisch}$$
Die Multiplikation einer symmetrischen und einer antisymmetrischen Funktion ergibt jedenfalls $0$. Der Nachweis dafür ist wie folgt:
$$A_{ij}\cdot S_{ij}=-A_{ji}\cdot S_{ji}\underset{umbenennen}{=}-A_{ij}\cdot S_{ij}$$
$$\implies2\cdot A_{ij}\cdot S_{ij}=0$$
Dadurch folgt, dass die Multiplikation eines antisymmetrischen Vektors mit einem symmetrischen Vektor immer $0$ ergibt. Entsprechend wurde gezeigt, dass gilt:
$$\partial_iB_i(x_m)=0$$
Das magnetische Feld ist somit quellenfrei!

---

> Zeigen Sie unter Zuhilfenahme des Biot-Savart’schen Ausdrucks für das Magnetfeld $B_i(x_m)$ in Abhängigkeit von der Volumsstromdichte $J_i(x_m)$ die Divergenzfreiheit von $B_i(x_m)$.

Gemäß dem Biot-Savart-Gesetz erzeugt ein Stromleiter mit dem infinitesimalen Längenelement $d\boldsymbol{l}$, welcher sich an dem Ort $\boldsymbol{r}'$ befindet und von einem Strom $I$ durchflossen wird, am Ort $\boldsymbol{r}$ die magnetische Flussdichte $d\boldsymbol{B}$:
$$d\boldsymbol{B}=\frac{\mu_0}{4\pi}\frac{I\,d\boldsymbol{l}\times\boldsymbol{\hat{r}}}{r^2}$$
Der Vektor $\boldsymbol{\hat{r}}$ ist dabei wie folgt definiert:
$$\boldsymbol{\hat{r}}=\frac{\vec{r}}{|r|}$$
Umgeschrieben entspricht der Ausdruck für die magnetische Flussdichte $\boldsymbol{B}$ am Ort $\boldsymbol{r}$ somit:
$$d\boldsymbol{B}(\boldsymbol{r})=\frac{\mu_0}{4\pi}\cdot I\,d\boldsymbol{l}\times\frac{\boldsymbol{r}-\boldsymbol{r}'}{|\boldsymbol{r}-\boldsymbol{r}'|^3}$$
Durch Aufsummieren der infinitesimalen Anteile und durch Umwandeln des entstehenden Wegintegrals in ein Volumensintegral folgt die Integralform des Biot-Savart-Gesetzes: ($\boldsymbol{J}$ entspricht der elektrischen Stromdichte)
$$\boldsymbol{B}(\boldsymbol{r})=\frac{\mu_0}{4\pi}\cdot\int_V\boldsymbol{J}(\boldsymbol{r})\times\frac{\boldsymbol{r}-\boldsymbol{r}'}{|\boldsymbol{r}-\boldsymbol{r}'|^3}\,dV'$$
Dieser kann in die bereits eingangs beschriebene Berechnung eingesetzt werden.

---

>Unter Verwendung des Biot-Savart’schen Ausdrucks für das Magnetfeld $B_i(x_m)$ in Abhängigkeit von der Volumsstromdichte $J_i(x_m)$ zeige man die Abwesenheit von magnetischer Ladung.

Die Abwesenheit von magnetischer Ladung ist äquivalent zu der Quellfreiheit des magnetischen Feldes.

---

## 4. Ampéresches Gesetz und Stromdichte
> Für zwei Flächen $F_1$ und $F_2$, welche durch dieselbe Kurve $\gamma$ berandet werden (d.h. $\partial F_1=\partial F_2=\gamma$), weise man die Gleichheit des magnetischen Flusses durch diese Flächen, unter Verwendung der magnetostatischen Maxwellgleichungen, nach.

![Integralsätze.png](./images/Integralsätze.png)
Der magentische Fluss $\Phi$ ist allgemein als das Flächenintegral über die magnetische Flussdichte $\boldsymbol{B}$ definiert:
$$\Phi=\int_{\partial V}\boldsymbol{B}\cdot dA$$
Der Satz von Gauß lautet für ein vom Rand $\partial V$ eingeschlossenes Volumen $V$, für ein beliebiges Vektorfeld mit den Komponenten $B_i$:
$$\int_V\partial_iB_i\,dV=\oint_{\partial V}B_i\,dA$$
Die zweite Maxwell-Gleichung in der Magnetostatik lautet:
$$\partial_iB_i(x_m)=0$$
Demnach folgt für das Flächenintegral:
$$\int_V\underbrace{\partial_iB_i}_{=0}\,dV=\oint_{\partial V}B_i\,dA$$
$$0=\oint_{\partial V}B_i\,dA$$
Nachdem sowohl die Fläche $F_1$, als auch die Fläche $F_2$ ein Rand $\partial V$ des Volumens $V$ sind, folgt:
$$\oint_{F_1}B_i\,dA=\oint_{F_2}B_i\,dA=0$$
# TODO! Reicht das als Nachweis? (ggf. Stokes, um auf den Rand zu kommen?)

---

> Unter Verwendung der magnetostatischen Maxwellgleichungen bestimme man die Rotation der Volumensstromdichte $J_i(x_m)$. Den so gewonnen Ausdruck löse man nach $B_i(x_m)$ unter Zuhilfenahme der Green-Funktion des Laplace-Operators auf.

Die erste Maxwell-Gleichung der Magnetostatik lautet:
$$\boldsymbol{\nabla}\times\boldsymbol{B}=\mu_0\cdot\boldsymbol{J}$$
Ermittelt man basierend darauf die Rotation der Volumensstromdichte $\boldsymbol{J}$, folgt daraus:
$$\boldsymbol{\nabla}\times\left(\boldsymbol{\nabla}\times\boldsymbol{B}\right)=\boldsymbol{\nabla}\times\left(\mu_0\cdot\boldsymbol{J}\right)$$
Gemäß der Rechenregeln für den Rotations-Operator ergibt sich daraus:
$$\boldsymbol{\nabla}\left(\boldsymbol{\nabla}\cdot\boldsymbol{B}\right)-\boldsymbol{\nabla}^2\boldsymbol{B}=\boldsymbol{\nabla}\times\left(\mu_0\cdot\boldsymbol{J}\right)$$
Nachdem die Divergenz der magnetischen Flussdichte $\boldsymbol{\nabla}\cdot\boldsymbol{B}$ gemäß der zweiten Maxwell-Gleichung der Magnetostatik gleich $0$ ist, folgt:
$$0-\boldsymbol{\nabla}^2\boldsymbol{B}=\boldsymbol{\nabla}\times\left(\mu_0\cdot\boldsymbol{J}\right)$$
Umgeformt nach der magnetischen Flussdichte $\boldsymbol{B}$ ergibt sich daraus:
$$\boldsymbol{B}=-\mu_0\cdot\frac{\boldsymbol{\nabla}\times\boldsymbol{J}}{\boldsymbol{\nabla}^2}$$
Die Green-Funktion des Laplaceoperators entspricht außerdem:
$$G=-\frac{1}{4\pi}\cdot\int d^3x'\frac{1}{|x_m-x_m'|}$$
# TODO! wohin verschwindet das ^-2?
Setzt man die Green-Funktion des Laplaceoperators in die Formel für die magnetische Flußdichte $\boldsymbol{B}$ ein, folgt daraus:
$$\boldsymbol{B}=+\frac{\mu_0}{4\pi}\cdot\int d^3x\frac{\epsilon_{ijk}\partial_jJ_k}{|x_m-x_m'|}$$
Der resultierende Ausdruck entspricht dem Ampére'schen Ausdruck für das magnetische Feld $\boldsymbol{B}$.

---

> Zeigen Sie unter Verwendung der zweiten magnetostatischen Maxwellgleichung, dem Ampéreschen Gesetz, die Divergenzfreiheit der Stromdichte $J_i(x_m)$.

# TODO!

---

> Zeigen Sie, dass die stationäre (zeitunabhängige) Kontinuitätsgleichung $\partial_iJ_i=-\frac{\partial\rho}{\partial t}$ eine direkte Konsequenz des Ampere’schen Gesetzes zwischen Magnetfeld $B_i(x_k)$ und Volumsstromdichte $J_i(x_k)$ darstellt.

Das Ampére'sche Gesetz in Integralform lautet:
$$\oint_C\boldsymbol{B}\cdot dl=\mu_0\int_S\boldsymbol{J}\cdot d\boldsymbol{A}=\mu_0\cdot I_{enclosed}$$
# TODO!

---

## 5. 