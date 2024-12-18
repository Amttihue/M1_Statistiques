# TD4

## Exercice 4

Le caractère étudié est l'existence d'une voiture rouge dans le foyer.

En Italie, ce caractère prend une proportion p = 0.457

1. On définit l'hypothèse nulle telle que : le village est Italien
2. 
   On étudie la V.A. F égal à la fréquence du caractère dans notre échantillon
   
   nF suit une loi binomiale $B(n;p)$
   
   n est assez grand et p pas trop proche de 0 ni de 1, $\\$on peut estimer que $F \sim N(p,p(1-p)/n)$
   
   donc $\frac{F-p}{\sqrt{\frac{p(1-p)}{n}}}\sim N(0,1)$

3.  
   On définit alors la région critique qui permet de rejeter l'hypothèse. Ici, on choisit un intervalle centré (t est bilatéral) afin de savoir s'il s'agit d'un village italien. 
   
   Au risque d'erreur de 5%, on trouve un intervalle de reget $R[-1.96;1.96]$

4. 
   Pour l'échantillon des 50 foyers, on trouve $g=1.5988$
   
   Ici $g \in [-1.96;1.96]$
   
   i.e. g n'appartient pas à l'intervalle de rejet.
   Il est probable que le village soit italien.


****
### 04/12/2024

## Exercice 5

1. On définit l'hypothèse nulle $H_0$ par "l'affirmation du constructeur est vraie", c'est à dire, la durée de vie moyenne des écrans est d'au moins 10000h.

    Remarque : Ici, on n'aura pas un test bilatéral (avec une région d'acceptation définie par deux limites a et v) mais un test unilatéral (avec une région d'acceptation définie par une limite a)

2. On choisit pour variable aléatoire discriminant la moyenne $\overline{X}$

    La taille de l'échantille est grande (n = 200) donc la V.A. Y = $\frac{\overline{X}-\mu}{o\sqrt{n}}$ suit une loi normale centrée réduite.

    Ici on a pour $\mu$ = 10000.

3. Pour déterminer la région d'acceptation, on va déterminer une limite a tel que l'on ait 95% de chances d'avoir y dans cet intervalle.

    On cherche $a$ tel que $\mathbb{P}(a<Y)=0.05$

    Ici, $a = u_{0.05}$. Par asymétrie de la loi normale, $u_{0.05}=-u_{0.05}$

    La taille de la loi normale centrée réduite donne $u_{0.95}=1.65$ d'où un intervalle d'acceptation $[-1.65;+\infty[$

    Et l'intervalle de rejet au risque d'erreur de 5% sera $]-\infty;-1.65]$

4. On calcule une estimation de Y en utilisant $s'^2$ au lieu de $\sigma^2.$

    $y = \frac{9700-10000}{120/\sqrt{200}} \approx -35$ 
    
    Donc $Y \in \ ]-\infty;-1.65]$ au risque de se trouper à 5%, l'affirmation du constructeur est vraie


****
### 11/12/2024



