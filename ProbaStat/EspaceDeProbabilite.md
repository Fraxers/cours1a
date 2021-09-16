# ESPACE DE PROBABILITÉ

Dans la modelisation d'un experience aléatoire, la première étape consiste à établir la liste des résultats possibles. L'ensemble de ces résultats est noté $\Omega$.

$\Omega$ univers, ensemble des réalisations. Un élément de $\Omega$ est noté $\omega$.
- Exemple :
  - Jeu de pile ou face : $\Omega = \{F, P\}$
  - Jeu de dé : $\Omega = \{1,2,3,4,5,6\}$

---

## I/ Tribu et Événement

- Un événement est un sous ensemble de $\Omega$
- La tribu associée à $\Omega$ sera définie par une famille d'événements (càd des sous ensembles de $\Omega$) vérifiants un certains nombre de propriétés.

On note $F$ la tribu associée à $\Omega$, les propriétés que doit vérifier $F$ sont :
- $\Omega \in F , \varnothing \in F$
- $A \in F \implies A^\complement \in F$
- Si $(Ai)\underset{i \in \N}{}$ sont des événements de $F$ alors $\underset{i \in \N}{\cup}A \in F$ et $\underset{i \in \N}{\cap}Ai \in F$

Exemples : 
- $\{ \varnothing, \Omega \}$ est une tribu
- Si $A \subset \Omega$ alors $\{ A, A^\complement, \varnothing, \Omega \}$ est une tribu

---

## II/ Probabilité

**Définition :**
- Une probabilité définie sur le couple $(\Omega, F)$ [espace mesurable] est une application de F dans [0, 1] vérifiant les conditions suivantes :
  - $\mathbb{P}(\Omega)=1$
  - Si $(Ai)_{i \in I}$ est une famille finie ou dénombrable d'événements (càd d'éléments de F) deux à deux disjoints $\mathbb{P}(\underset{i \in I}{\cup}Ai) = \displaystyle\sum_{i \in I} \mathbb{P}(Ai)$

- Propriété de $\sigma$-additivité si I est dénombrable.
- Propriété d'additivité si I est fini.
- $(\Omega, F, \mathbb{P})$ = Espace de probabilité
- On dit qu'un événement $A \in F$ est certain si $\mathbb{P}(A) = 1$
- On dit qu'un événement $A \in F$ est negligeable si $\mathbb{P}(A) = 0$
- Une propriété P dependante des éléments de $\Omega$ sera dite vraie presque-surement si $\{\omega \in \Omega : P(\omega) \text{ est vrai}\}$ contient un événement certain.

    $\Omega \rightarrow \{0,1\}~~~~~~~~~~P(\omega) = 0$, $P$ est fausse 
    
    $\omega \rightarrow P(\omega)~~~~~~~~~~~P(\omega) = 1$, $P$ est vraie

**Définition :**
- Soit $(Ai)_{i \in I}$ une famille de sous ensemble de $\Omega$. One dit que $(Ai)_{i \in I}$ est une partition de $A \subset \Omega$ si :

    $A = \underset{i \in I}{\cup}Ai$

    $Ai \cap Aj = \varnothing \text{ pour } i\not=j$

**Exemple de probabilité**

- Lorsque $\Omega$ est fini $\lbrack \Omega = \lbrace \omega_1, \omega_2, ..., \omega_n\rbrace\rbrack$ on considère habituellement pour $F$ l'ensemble des parties de $\Omega$ noté $P(\Omega)$.

- Une probabilité $\mathbb{P}$ sur ce type d'ensemble est définie par les valeurs $\mathbb{P}(\{\omega_i\})=p_i$ ou $(p_1, p_2, ..., p_n)$ sont des réels positifs vérifiants $\displaystyle\sum_{i=1}^n p_i = 1$. Dans ce cas, $\mathbb{P}(A)=\displaystyle\sum_{i=\omega_i \in A}p_i$
- Un exemple de probabilité sur $\Omega = \{\omega_1, \omega_2,...,\omega_n\}$ est la probabilité uniforme. Comme précédemment, on a $\mathbb{P}(\{\omega_i\})=p_i$. Alors dans ce cas, $p_1 = p_i,~ \forall i \in \{1,n\}$

$$\large{\displaystyle\sum_{i=1}^n p_i =1 \implies n*p_1 = 1 \implies p_1 = {1\over n} \implies \forall i \in\{1,n\}, ~p_i={1\over n}}$$

$$\large{\boxed{n = card(\Omega), ~~~p_i={1\over card(\Omega)}, ~~~\mathbb{P}(A)={card(A)\over card(\Omega)}}}$$

**Propositions :**
- Soit $(\Omega, F, \mathbb{P})$ un espace de probabilité :

  1. $\mathbb{P}(\varnothing) = 0$
  2. Si $A \in F,~~~ \mathbb{P}(A^\complement) = 1-\mathbb{P}(A)$
  3. Si $A \subset B$ alors $\mathbb{P}(A) \le \mathbb{P}(B)$
  4. Si $A \text{ et } B$ sont deux événement alors, $\large{\boxed{\mathbb{P}(A \cup B)=\mathbb{P}(A)+\mathbb{P}(B)-\mathbb{P}(A\cap B)}}$

**Propositions :** 
- Formule des probabilité totale :
  - Soit $(\Omega, F, \mathbb{P})$ un espace de probabilité et $(A_i)_{i\in I}$
 une famille finie et dénombrable formant une partition de $(\Omega)$. On a que :
    - $\large{\mathbb{P} = \sum_{i\in I} \mathbb{P}(B\cap A_i) \text{pour tout} B \in F}$

**Preuve :** 
- Par hypothèse $(B\cap A_i)_{i\in I}$ est une proposition de $B$. En effet, $\forall i \not ={j}, \\ (B\cap A_i) \cap (B\cap Ai) = \varnothing$ et $\underset{i \in I}{\cup}(B \cap A_i) = B \cap (\underset{\cup}{i \in I}A_i) = B \cap \Omega = B$

$$\large{\boxed{\mathbb{P}(B)=\mathbb{P}(\underset{i\in I}{\cup}(B\cap A_i)) = \underset{{i\in I}}{\sum} \mathbb{P}(B\cap A_i)}}$$

**Propositions :**
1) Si $(A_i)_{i\in N}$ est une famille croissante d'événements $(A_i \subset A_{i+1})$, alors $\lim\limits_{i\to x} \mathbb{P}(A_i) = \mathbb{P}(\underset{i \in N}\cup A_i)$

2) Si $(A_i)_{i\in N}$ est une famille décroissante d'événéménts $(A_i \subset A_{i+1})$, alors $\lim\limits_{i\to x} \mathbb{P}(A_i) = \mathbb{P}(\underset{i \in N}\cap A_i)$

3) Si $(C_i)_{i\in I}$ est une famille finie ou dénombrable d'événements alors $\mathbb{P}(\underset{i \in I}\cup C_i) \le \displaystyle\sum_{i\in I} \mathbb{P}(C_i)$
---
## III/ Indépendence d'événements

**Définition :**
1) Deux événements A et B sont indépendants si $\mathbb{P}(A\cap B) = \mathbb{P}(A)*\mathbb{P}(B)$
2) Une famille finie d'événements $(A_i)_{i\in I}$ est indépendante si $\forall J \subset I, ~~\mathbb{P}(\underset{j\in J}{\cap}A_j) = \underset{j\in J}{\Pi}\mathbb{P}(C_i)$ 
3) Une famille quelconque d'événements $(A_i)_{i\in I}$ est indépendante si pour toute sous famille finie $(A_j)_{j\in J}$ où $J \subset I$ et $J$ fini, est indépendante.
   - $A_1, A_2, A_3$ indépendante :
     - $\begin{cases}
        \mathbb{P}(A_1 \cap A_2) = \mathbb{P}(A_1) * \mathbb{P}(A_2) \\
        \mathbb{P}(A_1 \cap A_3) = \mathbb{P}(A_1) * \mathbb{P}(A_3) \\
        \mathbb{P}(A_3 \cap A_2) = \mathbb{P}(A_3) * \mathbb{P}(A_2) \\
        \end{cases}~~$
        et $~~\large{\mathbb{P}(A_1 \cap A_2 \cap A_3)}=\mathbb{P}(A_1) \cap \mathbb{P}(A_2) \cap \mathbb{P}(A_3)$

---


## IV/ Probabilité conditionnelle

**Définition :** Soit $(\Omega, F, P)$ un espace de probabilité. La probabilité conditionnelle de l'événement $A$ sachant l'événement $B$ est notée $\mathbb{P}(A|B)$ et est définie par

$\large{\mathbb{P}(A|B)= \begin{cases}
   \Large\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}&\text{si } \mathbb{P}(B) > 0 \\
   \mathbb{P}(A) &\text{sinon}
\end{cases}}$

**Exemple :**
- $\Omega = \{ (F,F), (F,G), (G,F), (G,G)\}$
- $\Omega ' = \{ (F,F), (F,G), (G,G)\}$

Modèle avec $\Omega$ :
  - $\mathbb{P}(\{F,F\}) = \large{1\over 4}$
  - $\mathbb{P}(\{F,G\}) = \large{1\over 4}$
  - $\mathbb{P}(\{G,F\}) = \large{1\over 4}$
  - $\mathbb{P}(\{G,G\}) = \large{1\over 4}$

**Donc probabilité uniforme**

On note :
  - $A$ = Un enfant G
  - $B$ = Un enfant F

Alors :
  - $\mathbb{P}(A|B) = \Large\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(B)}$
  - $A\cap B = \{(G,F), (F,G)\}$, Donc $\mathbb{P}(A\cap B) = \Large{2\over 4}$
  - Ainsi : $\mathbb{P}(A|B) = \Large{2 \over card(\Omega)} * \Large{card(\Omega)\over 3} = \Large{2 \over 3}$


### **Lien entre indépendance et probabilité conditionnelle**

**Proposition :**
Soit $(\Omega, \mathbb{F}, \mathbb{P})$ un espace de probabilité. A et B deux événements [A et B sont indépendants] <=> $\mathbb{P}(A|B) = \mathbb{P}(A)$ <=> $\mathbb{P}(B|A) = \mathbb{P}(B)$

**Formule de Bayes**:

On considère deux événements A et B. On suppose que $\mathbb{P}(B) > 0$

Alors $\boxed{\mathbb{P}(A|B)=\frac{\mathbb{P}(B|A)*\mathbb{P}(A)}{\mathbb{P}(B)}}$

**Formule de probabilités totale**:

On considère $(A_i)_{i\in I}$ une famille finie ou dénombrable d'événements formant un partition de $\Omega$. On suppose que $\mathbb{P}(A_i)>0$ pour tout $i\in I$