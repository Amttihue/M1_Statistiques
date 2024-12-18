# TD5

### 11/12/2024

## Exercice 9

On définit l'hypothèse nulle

a)

1) $H_0$ : "Les deux caisses de citrons proviennent de la même population."
2) On définit la V.A.
   
   $U=\frac{\overline{X_1}-\overline{X_2}}{\sqrt{\frac{{s'_1}^2}{n_1-1}+\frac{{s'_2}^2}{n_2-1}}}$ qui suit une loi N(0,1) pour $n_1$,$n_2$ grand (c'est le cas).

3) On définit une région d'acceptation symétrique par rapport à 0 (-> tout bilatéral) au risque d'erreur de 5%
    
    On cherche a,b tel que $\mathbb(a \leq U \leq b)=0.95$

    Donc $a = u_{0.025} = -b = -u_{0.975}$

    La région d'acceptatio nest [-1.96;1.96]

4) On estime une valeur de U en fonction de nos données $u = \frac{130-127}{\sqrt{\frac{36}{40-1}+\frac{49}{30-1}}}=1.856$
   
   $u \in [-1.96;1.96]$, on ne peut pas rejeter l'hypothèse nulle. Il est probable que les citrons proviennent de la même populaiton au regarde de ce test.

b) 

  1) $H_0$ : "Les deux caisses de citrons proviennent de la même population."
2) On définit la V.A.
   
   $F=\frac{(n_1-1) {s'_1}^2}{(n_2-1) {s'_2}^2}$ qui suit une loi Fisher-Snedecor de degrés de libertés $(n_1-1;n_2-1)=(39;29)$ grand (c'est le cas).

3) On définit une région d'acceptation symétrique par rapport à 0 (-> tout bilatéral) au risque d'erreur de 5%
    
    On cherche a,b tel que $\mathbb(a \leq U \leq b)=0.95$

    Donc $a = f_{0.025} = -b = -f_{0.975}$

    Avec les tables :
        
    f_{0.025} = 0.48 pour (dl1,dl2) = (30,30)
    f_{0.025} = 0.54 pour (dl1,dl2) = (50,30)
    f_{0.975} = 2.07 pour (dl1,dl2) = (30,30)
    f_{0.975} = 1.97 pour (dl1,dl2) = (50,30)
    
    
    On choisi un intervalle d'acceptation le plus large soit [0.48;2.07]
    
    python donne [0.510;2.033]

4) On calcule une estimation en fnoction des données

    $f=\frac{(40-1)+36}{(30-1)+49}=0.988$

    On ne rejette pas l'hypothèse nulle. Les citrons peuvent provenis d'une même population.


****

### 18/12/2024

## Exercice 7

1. Compléter le tableau 

   | Nom/résultats            | Très bons | Bons | Passables | Médiocres | Effectif marginal |
   |--------------------------|-----------|------|-----------|-----------|-------------------|
   | Nom du début d'alphabet  | 40        | 50   | 20        | 10        | 120               |
   | Nom au milieu d'alphabet | 45        | 120  | 5         | 10        | 180               |
   | Nom en fin d'alphabet    | 35        | 110  | 45        | 10        | 200               |
   | Effectif marginal        | 120       | 280  | 70        | 30        | 500               |

2. L'idée du test consiste à sommer les écarts des valeurs de notre tableau avec les valeurs théoriques si deux caractères étaient indépendants.
   
   $\mathbb{P}($très bon$)=\frac{120}{500}\rightarrow u_{0,1} = 120$

   $\mathbb{P}($bon$)=\frac{280}{500}\rightarrow u_{0,2} = 280$

   $\mathbb{P}($passable$)=\frac{70}{500}\rightarrow u_{0,3} = 70$

   $\mathbb{P}($médiocre$)=\frac{30}{500}\rightarrow u_{0,4} = 30$

   $\mathbb{P}($ 1ier tier de l'alphabet $)=\frac{120}{500}\rightarrow u_{1,0} = 120$
   
   $\mathbb{P}($ 2e tier de l'alphabet $)=\frac{180}{500}\rightarrow u_{2,0} = 180$
   
   $\mathbb{P}($ 3e tier de l'alphabet $)=\frac{200}{500}\rightarrow u_{3,0} = 200$

   On va diviser le tableau des effectifs théoriques

   $\mathbb{P}($ TB et 1ier tiers $)=\frac{120}{500} \times \frac{120}{500}$
   
   donc $u_{1,1} = 500 \times \mathbb{P}($TB et 1ier tier$)=\frac{144}{5} = 28.8$

   $u_{3,1} = 500 \times \frac{280}{500} \times \frac{120}{500}=48$

   etc...


   | Nom/résultats            | Très bons | Bons  | Passables | Médiocres | Effectif marginal |
   |--------------------------|-----------|-------|-----------|-----------|-------------------|
   | Nom du début d'alphabet  | 28.8      | 67.2  | 16.8      | 7.2       | 120               |
   | Nom au milieu d'alphabet | 43.2      | 100.8 | 25.2      | 10.8      | 180               |
   | Nom en fin d'alphabet    | 48        | 112   | 28        | 12        | 200               |
   | Effectif marginal        | 120       | 280   | 70        | 30        | 500               |

   
   