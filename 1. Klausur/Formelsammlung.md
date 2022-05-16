---
header-includes:
- \usepackage{cancel}
---

# 1. Klausur
## 0. Rotation und Divergenz von E
Die folgenden Bedingungen müssen für jedes statische elektrische Feld $\boldsymbol{E}(\boldsymbol{x})$ gelten:
$$Rotation:\,\boldsymbol{\nabla}\times\boldsymbol{E}=\epsilon_{ijk}\cdot\partial_j\cdot E_k=0$$
$$Divergenz:\,\boldsymbol{\nabla}\cdot\boldsymbol{E}=\partial_j\cdot E_j=\frac{\rho}{\epsilon_0}$$

Der Vollständigkeit halber auch die Formel für den Gradienten:
$$Gradient:\,(\nabla g)_i=\partial_ig$$

---

## 1. Gauß'sches Gesetz
### Integralform
$$\oint_S\boldsymbol{E}\cdot d\boldsymbol{A}=\frac{1}{\epsilon_0}\cdot\int_V\rho(\boldsymbol{x})\cdot d^3x=\frac{Q_{enclosed}}{\epsilon_0}$$

---

## 2. Das elektrische Feld
### Allgemeine Zusammenhänge
$$F=q\cdot E$$$$E=-\nabla V$$$$\boldsymbol{M}=\boldsymbol{r}\times(q\cdot\boldsymbol{E})$$($\boldsymbol{r}$ entspricht dem Hebelarm)
### Bedingungen für elektrisches Feld in Elektrostatik (= Maxwell-Gleichungen in Elektrostatik)
$$\nabla\times E=0$$
$$\nabla\cdot E=\frac{\rho}{\epsilon_0}\implies Gauss'sches\,Gesetz$$
### Coulomb'scher Ausdruck für $\boldsymbol{E_i(x_m)}$
$$E_i(x_m)=\frac{1}{4\pi\cdot\epsilon_0}\cdot\int d^3x'\cdot\frac{\rho(\boldsymbol{x}_m')\cdot(\boldsymbol{x}_i-\boldsymbol{x}_i')}{{|\boldsymbol{x}_m-\boldsymbol{x}_m'|}^3}$$
*$x'$ entspricht dem Quellpunkt. $x$ entspricht dem Referenzpunkt.*

**Merksatz**: Wann verwendet man den Coulomb-Ansatz und wann das Gauß’sche Gesetz? Wenn ein Volumen existiert, auf dessen Oberfläche das elektrische Feld konstant ist -> Gauß’sches Gesetz.
Ansonsten -> Coulomb'scher Ausdruck.

### Dipolmoment
$$\vec{p}=\sum q_i\cdot\vec{r}_i$$
### Energie
Die Potentielle Energie $U_q$ eines elektrischen Feldes $E$ ist:
$$U_q(\boldsymbol{x})=q\cdot V(\boldsymbol{x})$$
Die Abstoßungsenergie $E_{ee}$ eines elektrischen Feldes ist: ($U$ entspricht der elektrischen Spannung)
$$E_{ee}=q\cdot U=q\cdot\int_{\Gamma}E\,ds$$
Die Selbstenergie $U$ eines elektrischen Feldes $E$ ist:
$$U=\frac{\epsilon_0}{2}\cdot\int E^2\,d^3x$$

---

## 3. Poisson's Gleichung
$$-\nabla^2V=\frac{\rho}{\epsilon_0}$$

---

## 4. Das elektrische Potential
$$V(\boldsymbol{x})=\frac{1}{4\pi\cdot\epsilon_0}\cdot\int\frac{\rho(\boldsymbol{x'})}{|\boldsymbol{x}-\boldsymbol{x'}|}\,d^3x'$$
Ist das elektrische Feld bekannt, gilt für das elektrische Potential:
$$V(x)=-\int_{\Gamma}E\,dl$$
Das elektrische Potential entspricht dem Wegintegral von $x_0$ nach $x$.

---

## 5. Kugelkoordinaten
![[Kugelkoordinaten.png]]
$$\vec{r}(R,\theta,\varphi)=\left[{\begin{array}{cc} R\cdot\sin{\theta}\cdot\cos{\varphi} \\ R\cdot\sin{\theta}\cdot\sin{\varphi} \\ R\cdot\cos{\theta} \\ \end{array} }\right]$$
Bzw. mit einer anderen Parametrisierung:
$$\vec{r}(R,s,t)=\left[{\begin{array}{cc} R\cdot\sin{s}\cdot\cos{t} \\ R\cdot\sin{s}\cdot\sin{t} \\ R\cdot\cos{s} \\ \end{array} }\right]$$
In Kugelkoordinaten gilt:
$$dV=r^2\cdot\sin{\theta}\,dr\,d\theta\,d\varphi$$
Zum Beispiel:
$$\int_VE\,dV=\int_0^R\int_0^{2\pi}\int_0^{\pi}E\,d\theta d\varphi dr=\int_0^R\int_0^{2\pi}\int_0^{\pi}E\cdot r^2\cdot\sin{\theta}\,dr\,d\theta\,d\varphi=4\pi\cdot\int_0^RE\cdot r^2\,dr$$

---

## 6. Kreiskoordinaten / Polarkoordinaten
![[Polarkoordinaten.png]]
$$\vec{r}(R,\varphi)=\left[{\begin{array}{cc} R\cdot\cos{\varphi} \\ R\cdot\sin{\varphi} \\ \end{array} }\right]$$
Bzw. mit einer anderen Parametrisierung:
$$\vec{r}(s,t)=\left[{\begin{array}{cc} s\cdot\cos{t} \\ s\cdot\sin{t} \\ \end{array} }\right]$$

---

## 7. Zylinderkoordinaten
![[Zylinderkoordinaten.png]]
$$\vec{r}(R,\varphi,z)=\left[{\begin{array}{cc} R\cdot\cos{\varphi} \\ R\cdot\sin{\varphi} \\ z \\\end{array} }\right]$$
Bzw. mit einer anderen Parametrisierung:
$$\vec{r}(s,t,z)=\left[{\begin{array}{cc} s\cdot\cos{t} \\ s\cdot\sin{t} \\ z \\\end{array} }\right]$$
In Zylinderkoordinaten gilt:
$$dV=r\,dr\,d\varphi\,dz$$
### Zylindersymmetrie
An den Deckflächen eines zylindersymmetrischen Systems ist $\vec{E}\bot dA$ . Daher sind diese für den Betrag des elektrischen Feldes irrelevant. ($\vec{E}=0$)

---

## 8. Integralsätze
![[Integralsätze.png]]
### Gaußscher Integralsatz
Der Satz von Gauß lautet für ein vom Rand $\partial V$ eingeschlossenes Volumen $V$ für ein beliebiges Vektorfeld mit den Komponenten $E_i$:
$$\int d^3V\partial_iE_i=\oint_{\partial V}dA_iE_i$$wobei $A_i$ die Komponenten des (stets nach außen gerichteten) Flächennormalvektors am Rand des Volumens sind.

### Stokescher Integralsatz
Der Satz von Stokes verknüpft ein Oberflächenintegral über eine (gekrümmte) Fläche mit einem Kurvenintegral über den Rand der Fläche:
$$\int_SdA_i\epsilon_{ijk}\partial_jF_k=\oint_{\partial S}ds_iF_i$$

---

## 9. Integrationsregeln
### Potenzregel
$$\int x^n\,dx=\frac{1}{n+1}\cdot x^{n+1}+C$$
### Faktorregel
$$\int c\cdot f(x)\,dx=c\cdot\int f(x)\,dx$$
### Summenregel
$$\int(f(x)+g(x))\,dx=\int f(x)\,dx+\int g(x)\,dx$$
### Differenzregel
$$\int(f(x)-g(x))\,dx=\int f(x)\,dx-\int g(x)\,dx$$
### Partielle Integration
$$\int f'(x)\cdot g(x)\,dx=f(x)\cdot g(x)-\int f(x)\cdot g'(x)$$
### Integration durch Substitution
$$\int f(x)\,dx=\int f(\varphi(u))\cdot\varphi'(u)\,du$$
### Besondere Regeln
$$\int\frac{1}{x}\,dx=\ln{(|x|)}+C$$
$$\int\sin{x}\,dx=-\cos{x}+C$$
$$\int\sinh{x}\,dx=\cosh{x}+C$$
$$\int\cos{x}\,dx=\sin{x}+C$$
$$\int\cosh{x}\,dx=\sinh{x}+C$$
$$\int\tanh{x}\,dx=\ln{(\cosh{x})}+C$$

---

### 10. Ableitungsregeln
### Ableitung einer Konstanten
$$f(x)=C\rightarrow f'(x)=0$$
### Ableitung von x
$$f(x)=x\rightarrow f'(x)=1$$
### Potenzregel
$$f(x)=x^n\rightarrow f'(x)=n\cdot x^{n-1}$$
### Faktorregel
$$f(x)=c\cdot g(x)\rightarrow f'(x)=c\cdot g'(x)$$
### Summenregel
$$f(x)=g(x)+h(x)\rightarrow f'(x)=g'(x)+h'(x)$$
### Differenzregel
$$f(x)=g(x)-h(x)\rightarrow f'(x)=g'(x)-h'(x)$$
### Produktregel
$$f(x)=g(x)\cdot h(x)\rightarrow f'(x)=g'(x)\cdot h(x)+g(x)\cdot h'(x)$$
### Quotientenregel
$$f(x)=\frac{g(x)}{h(x)}\rightarrow f'(x)=\frac{h(x)\cdot g'(x)-g(x)\cdot h'(x)}{h^2(x)}$$
### Kettenregel
$$f(x)=g(h(x))\rightarrow f'(x)=g'(h(x))\cdot h'(x)$$
### Besondere Regeln
$$f(x)=\sqrt{x}\rightarrow f'(x)=\frac{1}{2\cdot\sqrt{x}}$$
$$f(x)=e^x\rightarrow f'(x)=e^x$$
$$f(x)=\ln{(x)}\rightarrow f'(x)=\frac{1}{x}$$
$$f(x)=\sin{x}\rightarrow f'(x)=\cos{x}$$
$$f(x)=\sinh{x}\rightarrow f'(x)=\cosh{x}$$$$f(x)=\cos{x}\rightarrow f'(x)=-\sin{x}$$$$f(x)=\cosh{x}\rightarrow f'(x)=\sinh{x}$$$$f(x)=\tan{x}\rightarrow f'(x)=\frac{1}{\cos^2{x}}$$$$f(x)=\tanh{x}\rightarrow f'(x)=(1-\tanh^2{x})=\frac{1}{\cosh^2{x}}$$

---

## 11. Indexschreibweise
$$a\cdot b=a_i\cdot b_i$$
$$\vec{a}\times\vec{b}=\epsilon_{ijk}\cdot a_j\cdot b_k$$
$$\partial_ia_j=\delta_{ij}$$
$$\delta_{ij}\cdot a_i=a_j$$
$$\delta_{ij}\cdot\delta_{jk}=\delta_{ik}$$
$$\partial_ix_i=\delta_{ii}=n=3$$
$$\epsilon_{ijk}\cdot\epsilon_{klm}=det\left[{\begin{array}{cc} \delta_{il} & \delta_{im} \\ \delta_{jl} & \delta_{jm} \\ \end{array} }\right]=\delta_{il}\cdot\delta_{jm}-\delta_{jl}\cdot\delta_{im}$$
Das Levit-Civita-Symbol ändert unter Vertauschung zweier Indizes das Vorzeichen. z.B.:
$$\epsilon_{ijk}=-\epsilon_{jik}$$
$$\epsilon_{123}=1$$
$$\epsilon_{132}=-1$$
$$\epsilon_{122}=0$$

---

## 12. Taylorreihe
### Eindimensional
$$T_f(x,a)=\sum_{n=0}^{\infty}\frac{f^{(n)}(a)}{n!}\cdot(x-a)^n=f(a)+f'(a)\cdot(x-a)+\frac{f''(a)}{2}\cdot(x-a)^2+\frac{f'''(a)}{6}\cdot(x-a)^3+\dots$$
### Multidimensional
$$f(a_m+y_m)=\sum^{\infty}_{n=0}\frac{1}{n!}\cdot y_m^1\dots y_m^n\cdot\partial_m^1\dots \partial_m^n\cdot\frac{1}{r}$$
### Wichtige Taylorreihen

$$sin(x)=\sum\limits_{k=0}^{\infty}(-1)^{2k-1}\frac{x^{2k-1}}{(2k-1)!}=x-\frac{x^3}{3!}+...$$
$$cos(x)=\sum\limits_{k=0}^{\infty}(-1)^{2k}\frac{x^{2k}}{(2k)!}=1-\frac{x^2}{2!}+\frac{x^4}{4!}-...$$
$$e^x=\sum\limits_{k=0}^\infty \frac{x^k}{k!}=1+x+\frac{x^2}{2!}+...$$
$$\ln{x}=\sum\limits_{n=1}^\infty\frac{(-1)^{k+1}}{k}(x-1)^k=(x-1)-\frac{(x-1)^2}{2}+\frac{(x-1)^3}{3}-...$$
$$\sqrt{1+x}=1+\frac{x}{2}+...$$
$$\frac{1}{\sqrt{1+x}}=1-\frac{x}{2}+...$$
$$\frac{1}{1-x}=1+x+x^2+...$$


---

## 13. Allgemeine Rechenregeln
$$\hat{\boldsymbol{r}}=\vec{e}_r=\frac{\vec{r}}{|r|}$$
### Trigonometrische Zusammenhänge
$$\sin^2{x}+\cos^2{x}=1$$
$$\cosh^2{x}-\sinh^2{x}=1$$
$$\tan{x}=\frac{\sin{x}}{\cos{x}}$$

---

## 14. Regel von de L’Hospital
Die Regel von de L’Hospital erlaubt es in vielen Fällen, den Grenzwert von Funktionen selbst dann noch zu bestimmen, wenn deren Funktionsterm beim Erreichen der betreffenden Grenze einen unbestimmten Ausdruck liefert. Zum Beispiel: $\frac{0}{0}$, $0\cdot\infty$,$\infty-\infty$,$\frac{\infty}{\infty}$,$0^0$,$\infty^0$,$1^{\infty}$

Die Regel von de L’Hospital besagt dann, dass, _falls_ der Grenzwert $\lim_{x\rightarrow x_0}\frac{f'(x)}{g'(x)}$ existiert, dieser zugleich der Grenzwert $\lim_{x\rightarrow x_0}\frac{f(x)}{g(x)}$ sei, wobei $f'(x)$ und $g'(x)$ hier die ersten Ableitungen der Funktionen $f(x)$ und $g(x)$ sein sollen.

---

## 15. Geometrische Formen
### Kreis
Umfang: $2\pi\cdot r$
Fläche: $r^2\cdot\pi$

### Zylinder
Mantelfläche: $2\pi\cdot r\cdot h$
Volumen: $r^2\cdot\pi\cdot h$

### Kugel
Oberfläche: $4\pi\cdot r^2$
Volumen: $\frac{4}{3}\cdot\pi\cdot r^3$

---

## 16. Heaviside Funktion
Die Heaviside-Funktion hat für jede beliebige negative Zahl den Wert $0$, andernfalls den Wert $1$. Die Heaviside-Funktion ist mit Ausnahme der Stelle $x=0$ überall stetig.

$$\theta(x)=\begin{cases}0\quad\text{für }x<0\\1\quad\text{für }x\ge0\end{cases}$$

---

## 17. Dirac Funktion
$$\delta(x)=\begin{cases}1\quad\text{für }x=0\\0\quad\text{sonst}\end{cases}$$

---

## 18. Wirbelfreiheit
> Zeigen Sie die Rotationsfreiheit des elektrischen Feldes $E^{i}\left(x^{m}\right)$ unter Verwendung des Coulomb'schen Ausdrucks für $E^{i}\left(x^{m}\right)$ in Abhängigkeit von der Raumladungsdichte $\rho\left(x^{m}\right)$.

Der Coulomb-Ausdruck für das elektrische Feld ist:
$$E_i(x_m)=\frac{1}{4\pi\cdot\epsilon_0}\cdot\int_V\rho(\boldsymbol{x}_m')\cdot\frac{\boldsymbol{x}_i-\boldsymbol{x}_i'}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|^3}\,d^3x'$$
Das elektrische Feld ist der negative Gradient des elektrischen Potentials. Für später wird daher die folgende Nebenrechnung benötigt:
$$\partial_i\frac{1}{\underbrace{|\boldsymbol{x}_m-\boldsymbol{x}_m'|}_{\text{Abstand}}}=\partial_i\frac{1}{|\boldsymbol{x}|}=\partial_i\frac{1}{\sqrt{\boldsymbol{x}^2}}=\underbrace{-\frac{1}{2}\cdot\frac{1}{{\sqrt{\boldsymbol{x}^{2}}}^3}}_{\text{äußere Ableitung}}\cdot\partial_i\boldsymbol{x}^2=-\frac{1}{\cancel{2}}\cdot\frac{1}{\sqrt{{\boldsymbol{x}^{2}}}^3}\cdot\underbrace{\cancel{2}\cdot\boldsymbol{x}}_{innere Ableitung}\cdot\delta_{im}$$
$$=-\frac{\boldsymbol{x}_m-\boldsymbol{x}_m'}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|^3}\cdot\delta_{im}=-\frac{\boldsymbol{x}_i-\boldsymbol{x}_i'}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|^3}$$
Aus der Nebenrechnung lässt sich demnach ablesen:
$$-\boldsymbol{\nabla}\frac{1}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|}=\frac{\boldsymbol{x}_i-\boldsymbol{x}_i'}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|^3}$$
Dieser Zusammenhang lässt sich nun in den Coulomb-Ausdruck für das elektrische Feld einsetzen:
$$E_i(x_m)=\frac{1}{4\pi\cdot\epsilon_0}\cdot\int_V\rho(\boldsymbol{x}_m')\cdot\left(-\boldsymbol{\nabla}\frac{1}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|}\right)\,d^3x'$$
Dieser Ausdruck kann vereinfacht werden zu:
$$E_i(x_m)=-\boldsymbol{\nabla}\underbrace{\left(\frac{1}{4\pi\cdot\epsilon_0}\cdot\int_V\frac{\rho(\boldsymbol{x}_m')}{|\boldsymbol{x}_m-\boldsymbol{x}_m'|}\,d^3x'\right)}_{=V(\boldsymbol{x}_m)}$$
Die Rotation des elektrischen Feldes kann damit wie folgt angeschrieben werden:
$$\epsilon_{ijk}\cdot\partial_j\cdot E_k=\epsilon_{ijk}\cdot\partial_j\cdot\left(-\partial_kV\right)=-\underset{\vee}{\epsilon_{ijk}}\cdot\underset{\cup}{\partial_j\cdot\partial_k}V=0$$
$$\vee\rightarrow\text{antisymmetrisch}$$
$$\cup\rightarrow\text{symmetrisch}$$
Die Multiplikation einer symmetrischen und einer antisymmetrischen Funktion ergibt jedenfalls $0$.
Der Nachweis dafür ist wie folgt:
$$A_{ij}\cdot S_{ij}\underset{vertauschen}{=}-A_{ji}\cdot S_{ji}\underset{umbenennen}{=}-A_{ij}\cdot S_{ij}$$
$$\implies2\cdot A_{ij}\cdot S_{ij}=0$$
Dadurch folgt, dass die Multiplikation eines antisymmetrischen Vektors mit einem symmetrischen Vektor $0$ ergibt.

---

## 19. Maxwell-Gleichungen in der Elektrostatik
### Erste Maxwell-Gleichung
$$\boldsymbol{\nabla}\times\boldsymbol{E}=0$$
### Zweite Maxwell-Gleichung
$$\boldsymbol{\nabla}\cdot\boldsymbol{E}=\frac{\rho}{\epsilon_0}$$

---

## 20. Wegunabhängigkeit
> Für das elektrische Feld $E^{i}\left(x^{m}\right)$ weise man mithilfe des Stoke'schen Satzes, die Gleichheit der Transportintegrale entlang zweier Kurven $x_{1}^{i}(t)$ und $x_{2}^{i}(t)$, welche respektive gleichen Anfangs- und Endpunkt besitzen und eine Fläche $F$ beranden, nach.

![[Wegunabhängigkeit.png]]
Der Satz von Stokes verknüpft allgemein ein Oberflächenintegral über eine (gekrümmte) Fläche mit einem Kurvenintegral über den Rand der Fläche:
$$\int_SdA_i\epsilon_{ijk}\partial_jF_k=\oint_{\partial S}ds_iF_i$$
Angewandt auf das elektrische Feld $E_i(x_m)$ entspricht der Satz von Stokes:
$$\int_F\boldsymbol{\nabla}\times\boldsymbol{E}\,dF=\oint_{C}E\,ds$$
Mit der Fläche $F$ aus der Skizze, kann man das Wegintegral über $C$ auf $C_1$ und $C_2$ aufteilen: (Nachdem für eine geschlossene Kurve $C_2$ gegen den Richtungssinn der Kurve $C$ laufen muss, hat das Integral ein negatives Vorzeichen.)
$$\int_F\underbrace{\boldsymbol{\nabla}\times\boldsymbol{E}}_{=0}\,dF=\oint_{C_1}E\,ds-\oint_{C_2}E\,ds$$
Wie bereits bei der Wirbelfreiheit des elektrischen Feldes in der Elektrostatik gezeigt, ist die Rotation von $E$ gleich $0$. (Zudem ist dieser Zusammenhang eine Maxwell-Gleichung.) Das elektrische Feld ist ein **Gradientenfeld**. Damit ergibt sich:
$$0=\oint_{C_1}E\,ds-\oint_{C_2}E\,ds$$
Vereinfacht zeigt sich somit, dass das elektrische Potential unabhängig von der Kurve $C_n$ (also unabhängig von dem Weg) ist:
$$-\oint_{C_1}E\,ds=-\oint_{C_2}E\,ds$$
*Nachsatz*: Das elektrische Feld ist der negative Gradient des elektrischen Potentials. Daher gilt der Zusammenhang:
$$V(\boldsymbol{x})=-\int_{\Gamma}E\,dl$$

---

## 21. Gradientenfeld
Es gibt für ein Gradientenfeld mehrere äquivalente Definitionen:
1. Ein Vektorfeld $\boldsymbol{F}$ heißt Gradientenfeld, wenn es ein Skalarfeld $\Phi$ gibt, sodass gilt $\boldsymbol{F}=\boldsymbol{\nabla}\Phi$.
2. Das Kurvenintegral ist wegunabhängig: Der Wert des Kurvenintegrals entlang einer beliebigen Kurve $S$ innerhalb des Feldes ist nur von ihrem Anfangs- und Endpunkt abhängig, nicht dagegen von ihrer Länge.
3. Kurvenintegrale über eine beliebige geschlossene Randkurve $S$ ergeben immer Null: $\oint_S\boldsymbol{F}\,dr=0$.

Das elektrische Feld $E$ ist ein Gradientenfeld.

---

## 22. Herleitung des elektrischen Feldes eines Punktdipols 
Das Potential eines Punktdipols im Ursprung ist:
$$V=\frac{1}{4\pi\cdot\epsilon_0}\cdot\frac{p_i\cdot r_i}{r^3}$$
Allgemein ist das elektrische Feld:
$$E=-\nabla V$$
Mit den folgenden Nebenrechnungen kann daraus das elektrische Feld ermittelt werden:
$$\partial_i\left(\frac{r_j}{r^3}\right)=\frac{\delta_{ij}}{r^3}+r_j\cdot\partial_j\left(\frac{1}{r^3}\right)$$
$$\partial_j\left(\frac{1}{(r^2)^{\frac{3}{2}}}\right)=\partial_j\left(\frac{1}{(r_k\cdot r_k)^{\frac{3}{2}}}\right)=-\frac{3}{2}\cdot\frac{\partial_i(r_l\cdot r_l)}{(r_k\cdot r_k)^{\frac{5}{2}}}$$
$$=-\frac{3}{2}\cdot\frac{2\cdot\delta_{il}\cdot r_l}{r^5}$$
Damit ergibt sich das elektrische Feld zu:
$$E_i=-\frac{p_j}{4\pi\cdot\epsilon_0}\cdot\left(\frac{\delta_{ij}}{r^3}-3\cdot r_j\cdot\frac{r_i}{r^5}\right)$$
$$=\frac{1}{4\pi\cdot\epsilon_0}\cdot\left(3\cdot\frac{p_j\cdot r_j}{r^5}\cdot r_i-\frac{1}{r^3}\cdot p_i\right)$$



---

## 23. Bedingungen für Leiter 
### Feldfreiheit innerhalb eines Leiters
$$E_i\Biggl\vert_{L_0}=0$$
### Radiale Ausbreitung des elektrischen Feldes
$$E_i\bot\partial L$$
### Äquipotentialfläche
$\partial L$ (der Rand eines Leiters) ist eine Äquipotentialfläche
### Ladungsverteilungs-freiheit innerhalb eines Leiters
$$\rho(x_m)\Biggl\vert_{L_0}=0\text{ , da }\partial_iE_i(x_m)=\frac{\rho(x_m)}{\epsilon_0}$$
### Der Fluss ist senkrecht zu der Oberfläche
$$E_i\cdot n_i\Biggl\vert_{\partial L}=\frac{\sigma}{\epsilon_0}\text{ , mit $n_i$ = Flächennormale von $\partial L$}$$

---

## 24. Herleitung Energie 
Der Ausgangspunkt ist die potentielle Energie:
$$U_q = q V(x_m)$$
Für ein System mit $N$ Punktladungen gilt:
$$U=\frac{1}{2} \sum\limits_{ij=1}^N \frac{1}{4\pi\varepsilon_0}\frac{q_iq_j}{|x^m_i-x^m_j|}$$
$$q_i=\rho(x_m){d^3 x}$$
$$q_j=\rho(x_m'){d^3 x'}$$
$$U=\frac{1}{2}\int d^3x d^3x' \frac{1}{4\pi\varepsilon_0}\frac{\rho(x_m)\cdot\rho(x_m')}{{|x_m-x_m'|}}$$
Alle $x_m'$-Terme werden zu einem $V(x_m)$ zusammengefasst:
$$=\frac{1}{2}\int d^3x\rho(x_m)\cdot{V(x_m)}$$
  Durch anwenden der ersten Maxwell-Gleichung folgt: ($\partial_i E_i=\frac{\rho(x_m)}{\varepsilon_0} \rightarrow \rho(x_m)=\partial_i E_i \varepsilon_0$): 

$$\Rightarrow \frac{\varepsilon_0}{2}\int\partial_i E_i(x_m)V(x_m)d^3x =$$
Mit der umgekehrten Produktregel folgt: %%Danke Han für die Erklärung%% 
$$=\frac{\varepsilon_0}{2} \int \underbrace{ \partial_i(E_i (x_m)
V(x_m))}_{=0,\, \text{durch Vektoridentitäten}}-E_i(x_m) \partial_i V(x_m) d^3x$$
Mittels dem Zusammenhang $E_i = -\partial_i V$  ergibt sich:
$$U=\frac{\varepsilon_0}{2}\int d^3x E^2(x_m)$$

---

## 25. Multipolmoment Formeln 
### Multipol-Entwicklung
$$V(r)=\frac{1}{4\pi\varepsilon_0}\left(\frac{Q}{r}+Q_i\frac{r_i}{r^3}+P_{ij}\frac{3\cdot r_ir_j-r^2\delta_{ij}}{2\cdot r^5} +\mathcal{O}(r^{-4})\right)$$
### Einzel-Momente mittels $\boldsymbol{\rho}$ berechnen:
$$Q=\int \rho(x_m) d^3 x$$
$$Q_i=\int \rho(x_m)\cdot x_i d^3 x$$
$$P_{ij}=\frac{1}{2}\cdot\int \rho(x_m)\cdot x_i x_j d^3 x$$

--- 

# 2. Klausur

In einer neuen Datei oder?
