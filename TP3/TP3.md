# TD3 (Correction) 

## Exercice 3

L'étendue d'un intervalle $[a,b]$ c'est l'écartement de l'intervalle, donc $b - a$.

Pour $Ip = \bigg(\frac{p - 1}{\sqrt n} ; \frac{p+1}{\sqrt n}\bigg)$

L'étendue est donc
$\Delta I = \frac{p + 1}{\sqrt n} - \frac{p - 1}{\sqrt n} = \frac{2}{\sqrt n}$

On résout alors

$\Delta I = 0.02$  
$\Leftrightarrow \frac{2}{\sqrt n} = 0.02$  
$\Leftrightarrow 2 = 0.02 * \sqrt n$  
$\Leftrightarrow 2 = \frac{2}{100} * \sqrt n$  
$\Leftrightarrow 100 = \sqrt n$  
$\Leftrightarrow n = 10000$  

Ainsi, pour avoir une étendue de 0.002, il faudra un échantillon de 10000 individus  

b) Ici, $n = 400$, on cherche l'étendue conrrespondant à l'intervalle de fluctuation  

i.e. $\frac{2}{\sqrt{400}} = \frac{2}{20} = 0.1$  

c) Ici on cherche n tel que :  
$\Delta I = \frac{2}{\sqrt{n}} \leq 0.04$

On résout $\frac{2}{\sqrt n} \leq 0.04 \Leftrightarrow 2 \leq \frac{4}{100} * \sqrt n$  
$\Leftrightarrow \frac{100}{2} \leq \sqrt n$  
$\Leftrightarrow 50 \leq \sqrt n$  
$\Leftrightarrow 2500 \leq n$  

## Exercice 4

On cherche un seuil centré de 5%  
"Centré" signifie qu'on a une marge de chaque côté de 2.5%

Pour trouver la limite de la marge, on fait donc $1 - 0.025 = 0.975$

On cherche donc cette valeur dans le tableau, ce qui nous donne $1.96$

Par symétrie, $u_{0.025} = -u_{0.975}$ et l'intervalle centré est $[-1.96;1.96]$

Au seuil de 2%, on cherche $u$ tel que l'aire verte vale $0.99$.

Par lecture, on lit $u_{0.99} = 2.33$

Par symétrie, $u_{0.01} = -u_{0.99}$

b) décentré à gauche, au seuil de 5%  
on cherche directement $u_{0.95} = 1.65$

L'intervalle devient $]-\infty ; 1.65]$

Décentré à gauche au seuil de 1%, on cherche $u_{0.99} = 2.33$ d'où $]-\infty;2.33]$

c) décentré à droite au seuil de 5%, on cherche $u_{0.05}$  
par asymétrie, $u_{0.05} = u_{0.95}$  
or on lit dans la table $u_{0.95} = 1.65$  
donc l'intervalle devient $[-1.65; +\infty[$  

## Exercice 5
b) décentré à gauche au seuil de 5%  
on cherche $c$  
on trouve $c = 25$  
L'intervalle est donc $[0, 25]$  
décentré à gauche au seuil de 1%  
on trouve $c = 30.58$ (pas dans le cours, erreur du prof)  
et l'intervalle est $[0,30.58]$  

c) décentré à droite au seuil de 5%  
on cherche   
on trouve $7.26$  
L'intervalle est $[7.26;+\infty[$  

d) centré au seuil de 5%  
(donc borné à $0.025$ à gauche et $0.975$ à droite)  
on trouve $c_{0.025} = 6.26$  
et $c_{0.975} = 27.49$  
L'intervalle est $[6.26;27.49]$  


****

27/11/2024

## Exercice 6
Pour avoir un intervalle centré à 5%, on cherche 

P(X<f_0.025) = 0.025
On trouve 0.28
P(X<f_0.975) = 0.975
On trouve 14.08

Ainsi P(f_0,025 < X < f_0,975) = 0.95

L'intervalle centré au seuil de 5% est [0.28;14.08]

## Exercice 7
Si X suit une loi de Student à 21 degrés de liverté, on regarde la taille sous la ligne dl21 /!\ La taille se donne t tq 

P(|T|>t)=P(T\in[-r;r]) = p
        = P(-t<T<t)=1-p

Pour p = 0.05, on lit t=2.080
soit l'intervalle [-2.080;2.080]

Pour p = 0.07, on lit t = 2.831 soit l'intervalle [-2.831,2.831]

## Exercice 8
On a $F\sim N(p,5^2/n)$ et l'échantillon donne $f=19.5$%

pt : F ne suit pas la loi normale centré réduite pour laquelel on a la taille -> il faut centrer et réduire F

F-p est une VA centré 
$\frac{F-p}{5/\sqrt n}$ est une VA qui suit la loi normale centrée réduite

Pour un intervalle décentré à gauche, on cherche $P(\frac{F-p}{5/\sqrt n}<u_n)=1-\alpha$

Soit $P(p<-F+u_n\times \frac{F-p}{5/\sqrt n}) = 1-\alpha \\ P(p>F-u_\alpha \times \frac{F-p}{5/\sqrt n}) = 1-\alpha$

/!\ c'est l'intervalle décentré à droite, il faut donc chercher $P(\frac{F-p}{5/\sqrt n}>u_\alpha) = 1-\alpha$

$<=> P(p<F-u_\alpha+\frac{5}{\sqrt n}) = 1-\alpha$

Pour $\alpha =0.05$, on trouve $u_{0.05}=-u_{0.95}=-1.65$

Donc l'intervalle est $IC =]-\infty ;0.195+1.65 \times \frac{5}{225}] = ]-\infty; 0.745]$

/!\ p est une proportion donc comprise entre $0\leq p \leq 1$


Pour l'intervalle centré au seuil de 5%, on va chercher $P(-u_{0.975}<\frac{F-p}{5/\sqrt n} <u_{0.975})=0.05$
$\\<=> P(F+u_{0.975} \times \frac{5}{\sqrt n}>p>F-u_{0.975}\times \frac{5}{\sqrt n})=0.05$

Après lecture de la taille, on trouve $u_{0.975}=1.96$

Soit $IC = [0.195-1.96\times \frac{5}{\sqrt 225};0.195+1.96 \times \frac{5}{\sqrt 225}]$
$\\ \simeq[-0.455;0.845]$

Au seuil de 1%, on fait de même avec $u_{0.995} = 2.57$






















<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({ tex2jax: {inlineMath: [['$', '$']]}, messageStyle: "none" });
</script>