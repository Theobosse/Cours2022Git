---
title: Raisinoment par récurence
created: '2021-09-07T06:19:20.025Z'
modified: '2021-09-14T07:07:07.004Z'
---

# Raisinoment par récurence

## Tex Help
$$
\left
\{
  \begin{array}
    {rcr}x+2y & = & -1 \\
    -x+4y & = & 0 \\
    -x+4y & = & 0 \\
  \end{array}
\right.$$

Hello $\left\{\begin{array}{rcr}x+2y & = & -1 \\-x+4y & = & 0 \\-x+4y & = & 0 \\\end{array}\right.$
## 1) Principe

On donne une propriété qui depends d'un entier naturel n notée P(n)
On veut montrer que cette propriété est vraie pour tout entier naturel n
On pourra le démontrer de la façon suivante
INITIALATION: on montre que la propriété est VRAIE pour n = 0
Et
HéréDITé: On montre que poun tout entier naturel n;
  - Si $P(n)$ est VRAIE
  - Alors $P(n+1)$ est VRAIE

On poura affirmer selon le principe de raisonnement par récurrance, pour tout entier naturel naturel n, P(n) est VRAI

## 2) Exemple

Exemple N°1:

$(u_n) = \{ u_0=600, pour \;u_n+1 = 0,85u_n + 300$

Démonterer en utilisant le raisonement par récurence pour tout n $\in \N$, $u_n=-1400*0,85^n+2000$

<u>Notation</u> : Soit n $\in \N$, on note P(n) : **$"u_n=-1400*0,85^n+2000"$**

<u> INITIALISATION: </u> on montre que P(o) est *VRAIE*
On sait que $u_n = 600$

on calcule: $u_0=-1400*0,85^0+2000 =-1400*1+2000 = 600$
On a prouvé que $u_0 = -1400*0,85⁰+2000$

<u>BILAN</u>: P(0) est *VRAIE*

<u>HéRéDITé</u>: Soit $n \in \N$

Hypothèse de récurence: $u_n=-1400*0,85^n+2000$ 
Conclustion$_\text{ce que on doit démonter}$: $u_{n+1} = -1400*0,85^{n+1}+2000$  

<u>PREUVE</u>: D'apres la relation de récurence $u_{n+1} = 0,85^{u_n} + 300$

D'apres l'hypothese de récurence
$u_n =  -1400*0,85^{n}+2000$

> Donc:  $u_{n+1} = 0,85*(-1400*0,85^{n}+2000) + 300$
Soit: $u_{n+1} = 0,85*(-1400*0,85^{n})+0,85*2000 + 300$
Soit: $u_{n+1} = -1400*0,85^{1}0,85^n + 1700 +300$
Soit: $u_{n+1} = -1400*0,85^{n+1} + 2000$
**C'est ce que l'on devait démonterer**

Donc:  $u_{n+1} = 0,85*(-1400*0,85^{n}+2000) + 300$
Donc:  $u_{n+1} = 0,85*-1400*0,85^{n}+0,85 * 2000 + 300$
Soit: $u_{n+1} = 0,85^{n+1} *- 1400 + 0,85*2000 + 300$
Soit: $u_{n+1} = 0,85^{n+1} *- 1400 + 1700 + 300$
Soit: $u_{n+1} = -1400*0,85^{n+1} + 2000$

<u>BILAN</u>: D'apres le princepe de raisement par récurrence pour tout $n \in \N$, P(n) est *VRAIE*


Exemple N°2: Inégalité de BERNOULLI

$Soit\;a \in ]0; + \infin[$
On a pour tout $n \in \N: (1+a)^n \ge 1+na$
On pose pour $n \in \N P(n): "(1+a)^n \ge 1+na"$

On doit donc montrer que $(1+a)⁰ \ge 1+0*a$
Or $(1+a)⁰ = 1\; et \;1+0*a = 1 \;et \;1>1 \;on\; a: (1+a)⁰ 1+0*a$


Hérédité: Soit $n \in \N$

Hypothèse de récurence **HR** : $(1+a)^n \ge 1+na$
Conclustion          **CCL** : $(1+a)^{n+1} \ge 1+(n+1)a$

Preuve:
On rappelle que $X^{n+1} = X*X^n$

On a : $(1+a)^{n+1} = (1+a)*(1*a)^n$

Sachant que a $\in ]0; +inf[\;;0<1+a$
D'apres l'hypothèse de récurence:
$(1+a)^n \ge 1+na$
Comme 1+a est positif on garde le sens de l'inégalité

Donc : $(1+a)*(1+a)^n \ge 1+na*(1+a)$      *(1)*
 CAR $(1+a) \ge 0$

Or:  $(1+a)*(1+a)^n = (1+a)^{n+1}$
ET $1+na*(1+a) = 1+na+a+na²$

Soit $(1+a)(1+na) = 1+(n+1)a+na²$
or $na² \ge 0$ donc $(1+a)(1+na)\ge 1+(n+1)a$    *(2)*


En utilisant: (1) et (2)

$(1+a)^{n+1} \ge (1+a)(1+na)$
et: $(1+a)(1+na) \ge 1+(n+1)a$

Donc: $(1+a)^{n+1} \ge 1+(n+1)a$    *CQFD*

**Bilan: pour tout n \in \N, P(n) est *VRAIE* d'apres le principe de raisonement par récurrence**

---

### 3) Autre cas pratique

Dans certains cas, on doit démonterer que la propriété est VRAI a partir d'un certain rang: c'est à dire un entier naturel $n_0$ tel que pour tout n $\ge n_0$, P(n) est VRAIE

Dans ce cas l'initalisation consiste à verifier que $P(n_0)$ est *VRAIE* et que l'hérédité en indiquant cepandant: pour $n \in \N$, tel que $n \ge n_0$

$n_0$ est un entier naturel

---

### 4) Principe de récurrence double

a) exemple: $(u_n): \{ u_0=1; u_1 =2, \text{pour tout} n \in \N, u_{n+2} = u_{n+1} + 2u_n$

1) Calculer $u_2$

<span color="green">Dans la relation de récurrence on remplace n=0</span>, $u_2 = u_n+2u_0 = 2+2*1 = 4$ 

<u>$u_2 = 4$</u>

2) Démontrer que: pour tout $n \in \N, u_n = 2^n$

On pose pour $n \in \N, P(N) : "u_n = 2^n"$

INITIALISATION: on montre que P(0) ET P(1) sont VRAIES

EN effet: $P(0) = 2⁰ = 1\ = u_0; et\; P(1) = 2 = 2¹ = u_1$

HéRéDITé : Soit $n \in \N$

HR: $P(n) et P(n+1)$ sont VRAIE
CCL: P(n+2) est VRAIE

Preuve:
On a $u_n = 2^n$; $u_{n+1} = 2^{n+1}$ par hypothèse de récurrence. En utilisant la relation de récurrence:

$u_{n+2} = u_{n+1} + 2u_n = 2^{n+1} + 2*2^n = 2^{n+1} +2^{n+1}$
donc $u_{n+2} = 2¹ * 2^{n+1} = 2^{n+2}$
Ainsi $P(n+2)$ est VRAIE

---

INITIALISATION: on montre que $P(n_0)$ ET $P(n_0+1)$ sont VRAIES

HéRéDITé : Soit $n \in \N$
Si: $P(n) et P(n+1)$
Alors: P(n+2) est VRAIE

## II) SUITES MAJORéES - MINORéES - BORENéES.
### 1) Definitiions

Soit $u_n$ une suite

#### Suite Majorée
On dit que la suite $u_n$ est majorées
s'il existe un nombre réel $M$, tel que: pout tout $n \in \N$, $u_n \leq M$
Le nombre $M$, ne doit pas dépendre de $n$
Ce nombre **$M$ est un majorant** de cette suite

#### Suite Minorée
On dit que la suite $u_n$ est minorée
s'il existe un nombre réel $m$, tel que: pout tout $n \in \N$, $m \leq u_n$
Le nombre $m$, ne doit pas dépendre de $n$
Ce nombre **$m$ est un minorant** de cette suite

#### Suites bornée
Une suite est bornée.
lorsque'elle est majorée et minotée

Autremement dit:
Si il exsite $m \in \R$ et $M \in \R$ tels que
	$\forall \in \N$, $m \leq u_n \leq M$


### 2) Propriétés:

étude sur une suite $u_n$ monotone
On rappele que une suite monotone est une suite croissante ou bien décroissante, 
Cas d'une suite croissante
$u_0$ $\leq$ $u_1$ $\leq$ $u_2$ $\leq$ ...... $\leq$ $u_n$ $\leq$ $u_{n+1}$ $\leq$ ....
On observe que $\forall n \in \N, u_0 \leq u_n$
Soit $u_n$ est minorée par $u_0$ 

Preuve: prouver l'observation en utilisonant le résonement par réccurrence
Soit $n \in \N, P(n): "u_0 \leq u_n"$  

INITIALISRATION: on a $u_0 \leq u_0$ donc P(0) est VRAIE:
HéRédité: SOit $n \in \N$
$u_0 \leq u_n \Rightarrow u_0 \leq u_{n+1}$ 

Preuve: 
on a par HR: $u_0 \leq u_n$
Sachant que u_n est croissante: $u_n \leq u_{n+1}$ on déduit que $u_0 \leq u_{n+1}$

<u>PROPRI2T2</u>
Une suite **croissante** est <u>minoré</u> par son 1er terme
Une suite **décroisant** est <u>majoré</u> par son 1er terme


$\left\{\begin{array}{rcr}u_0 = 6 \\\forall n \in \N, u_{n+1} = 0,2*u_n-3\\\end{array}\right.$

1) En utilisant le raisonement par récurrence, démontrez que:
$u_n$ est minorée par -3,75

2) a) étudier le sens de varations de $u_n$. en utilisant le raisonement par récueence
b) Cette suite est elle bornées




$$(u_n) = \{ u_0, \forall n \in \N, u_{n+1} = 0,2u_n -3$$


En utilisant le raisonnement par récurrence, étudier le sens de varation de $u_n$

- $u_1 - u_0 : u_1 = 0,2 *6 -3 = 1,2 -3 = 1,8$

puis $u_1-u_0 = -1,8-6 = -7,8$ 

soit $n \in \N$ $P(n): "u_{n+1} - u{n} < 0"$

INIT: $u_1 - u_0 < 0$ donc P(0) est VRAIE

H2E2DIT2: soit $n \in \N$

HR : $u_{n+1}-u_{n} < 0$
CCL: $u_{n+2}-u_{n+1} < 0$

Preuve:

D'apres la relation de récurrence:
$u_{n+2} = 0.2u_{n+1} -3$ 
et $u_{n+1} = 0.2u_{1} -3$ 

Puis: $u_{n+2} - u{n+1} = 0,2u_{n+1} - 3 - (0,2u_n-3)$
$\Leftrightarrow u_{n+2} - u{n+1} = 0,2u_{n+1} - 3 -0,2u_n +3$
$\Leftrightarrow u_{n+2} - u{n+1} = 0,2(u_{n+1} -u_n)$

D'apres HR $u{_n+1} - u_n < 0$
donc $0,2(u{_n+1} - u_n) < 0$
donc $u{_n+1} - u_n < 0$

Bilan: selon le principe de raisonnement par récurrence

$\forall n \in \N, u_{n+1} - u_n < 0$


Donc $u_n$ est stricement décroissancte
Montrere que $u_n$ est bornée

$u_n$ est strictement décroissante
donc $\forall n \in \N$, $u_n \leq u_0 = 6$

$u_n$ est minoée par -3.75

donc $\forall n \in \N$ $-3,75 \leq u_n \leq 6$


### 4) Suite non majorée; suite non minorée

#### a) Définition d'une suite non majorée

$u_n$ est majorée, s'il existe M, pour tout $n \in \N$: $u_n <= M$

----u0-----u2-----0---1-----u1----un------M-------------->

$u_n$ n'est pas majorée, s'il n'exsiste pas de nb $M \in \R, \forall n \in \N, u_n \leq M$

----M----------0---1---------un0-------------------->

si pour tout nombre $M \in \R$, il existe $n_0 \in \N, u_{n_0}>M$

Définiton d'une suite non minorée, 

#### b) Définition d'une suite non minorée:

$u_n$ est minorée s'il existe $m$, s'il existe $m \in \R$ , $\forall n \in \N, m \leq u_n$

----m----------0---1---------u1--u2----u0----un---->
$u_n$ n'est pas majorée, s'il n'exsiste pas de nb $m \in \R, \forall n \in \N, u_m \leq u_n$

--------------0---1---------un0-----m-------------->

si pour tout nombre $m \in \R$, il existe $n_0 \in \N, u_{n_0}<m$

#### c) une suite n'est pas bornée, lorque n n'est pas majoré  ou bien lorsqu'elle est pas minoré.
