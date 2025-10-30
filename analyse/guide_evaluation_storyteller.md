# Guide Méthodologique d'Évaluation du Storyteller

**Version :** 1.0  
**Date de création :** 30 octobre 2025  
**Objectif :** Référentiel permanent pour l'évaluation qualitative des benchmarks Storyteller

---

## Table des Matières

1. [Contexte et Objectifs](#contexte-et-objectifs)
2. [Grille de Notation Standardisée](#grille-de-notation-standardisée)
3. [Critères d'Évaluation Détaillés](#critères-dévaluation-détaillés)
4. [Méthodologie d'Analyse](#méthodologie-danalyse)
5. [Exemples de Niveaux de Qualité](#exemples-de-niveaux-de-qualité)
6. [Validation et Contrôle Qualité](#validation-et-contrôle-qualité)
7. [Reporting et Documentation](#reporting-et-documentation)

---

## Contexte et Objectifs

### Rôle du Storyteller dans l'Architecture

Le **Storyteller** est la première IA de l'architecture à double IA pour la génération de méditations guidées. Sa mission :

**Mission principale :** Créer un récit narratif cohérent de **5 scènes progressives** qui servira de base à une méditation guidée pour le sommeil.

**Responsabilités (Référence : [`architecture.md`](../architecture.md:144-151))** :
- ✅ Concevoir un **arc narratif** simple et clair
- ✅ Créer des **transitions fluides** entre scènes
- ✅ Utiliser un **vocabulaire sensoriel** simple (pas de termes techniques)
- ✅ Assurer la **cohérence spatiale** (progression logique des lieux)
- ✅ Maintenir une **atmosphère apaisante** (contexte relaxant)
- ✅ Respecter le thème et le lieu fournis

**Non-responsabilités :**
- ❌ Ancrage respiratoire (géré par Meditation Expert)
- ❌ Scan corporel (géré par Meditation Expert)
- ❌ Structure méditative en 5 parties (géré par Meditation Expert)

### Besoins Analytiques

#### 1. Comparaison Inter-Modèles

**Objectif :** Identifier le meilleur modèle d'IA pour le Storyteller en production.

**Questions clés :**
- Quel modèle produit les récits les plus cohérents ?
- Quels modèles maintiennent la meilleure atmosphère apaisante ?
- Quel modèle respecte le mieux les contraintes structurelles ?
- Quel est le rapport qualité/coût optimal ?

**Livrables attendus :**
- Classement des modèles par performance globale
- Identification du modèle recommandé pour production
- Modèles alternatifs viables pour A/B testing
- Modèles à éviter avec justifications

#### 2. Amélioration Continue des Prompts

**Objectif :** Identifier les faiblesses récurrentes pour optimiser le prompt Storyteller.

**Questions clés :**
- Quels sont les problèmes narratifs les plus fréquents ?
- Quelles règles du prompt ne sont pas respectées ?
- Quelles améliorations du prompt pourraient résoudre ces problèmes ?

**Livrables attendus :**
- Liste des problèmes récurrents avec exemples
- Recommandations concrètes d'amélioration du prompt
- Règles à renforcer ou à clarifier
- Exemples à ajouter dans le prompt

#### 3. Validation de Cohérence Architecture

**Objectif :** Vérifier que les sorties respectent les spécifications de l'architecture.

**Questions clés :**
- Le format JSON est-il respecté ?
- Les contraintes structurelles sont-elles respectées (5 scènes, ~300 mots) ?
- Les connexions (lieu/thème/son) sont-elles cohérentes ?

**Livrables attendus :**
- Taux de conformité par modèle
- Identification des champs JSON problématiques
- Validation de la cohérence avec architecture

#### 4. Monitoring de Qualité

**Objectif :** Établir des métriques de qualité reproductibles pour suivi dans le temps.

**Questions clés :**
- Quels sont les KPIs de qualité narrative ?
- Comment mesurer l'amélioration dans le temps ?
- Quels seuils de qualité minimale définir ?

**Livrables attendus :**
- KPIs définis et mesurables
- Benchmarks de référence
- Seuils de qualité minimale par critère

---

## Grille de Notation Standardisée

### Vue d'Ensemble

Chaque benchmark est évalué sur **5 critères principaux**, chacun noté sur **10 points**, pour un **total de 50 points**.

| Critère | Poids | Description | Référence Architecture |
|---------|-------|-------------|------------------------|
| **Arc Narratif** | 10 pts | Clarté et simplicité de la structure narrative | [`architecture.md:145`](../architecture.md:145) |
| **Cohérence Spatiale** | 10 pts | Progression logique et absence de sauts spatiaux | [`architecture.md:148`](../architecture.md:148) |
| **Transitions** | 10 pts | Fluidité des passages entre scènes | [`architecture.md:146`](../architecture.md:146) |
| **Progression Logique** | 10 pts | Respect de la structure en 5 scènes attendue | [`architecture.md:262-266`](../architecture.md:262-266) |
| **Connexions** | 10 pts | Qualité des 5 connexions (lieu/thème/exploration/retour/son) | Prompt Storyteller |

### Échelle de Notation Générale

| Note | Signification | Critère de décision |
|------|---------------|---------------------|
| **10/10** | Parfait | Aucune faiblesse identifiable, excellence sur tous les aspects |
| **9/10** | Excellent | Très haute qualité avec éventuellement 1-2 imperfections mineures |
| **8/10** | Très bon | Bonne qualité générale avec quelques points à améliorer |
| **7/10** | Bon | Qualité acceptable mais avec faiblesses notables |
| **6/10** | Passable | Problèmes significatifs mais récit utilisable |
| **5/10 ou moins** | Insuffisant | Problèmes majeurs, récit non utilisable en production |

### Notes Globales et Recommandations

| Note Globale | Interprétation | Recommandation |
|--------------|----------------|----------------|
| **45-50** | Excellence | Modèle recommandé pour production |
| **40-44** | Très bon | Modèle viable pour production ou A/B testing |
| **35-39** | Bon | Modèle acceptable avec réserves, amélioration possible |
| **30-34** | Passable | Non recommandé pour production, amélioration nécessaire |
| **<30** | Insuffisant | À éviter, problèmes structurels majeurs |

---

## Critères d'Évaluation Détaillés

### 1. Arc Narratif (/10)

**Définition :** Évalue la clarté et la simplicité de la structure narrative globale.

#### Barème Détaillé

| Note | Critères | Indicateurs |
|------|----------|-------------|
| **10** | Arc parfait | Structure claire : Ancrage → Exploration → Exploration profonde → Retour → Ancrage final. Progression évidente à la lecture. |
| **9** | Arc excellent | Structure respectée avec éventuellement 1 légère imprécision dans la progression. |
| **8** | Arc très bon | Structure globalement claire mais quelques étapes moins évidentes. |
| **7** | Arc bon | Structure identifiable mais transitions entre étapes floues. |
| **6** | Arc passable | Structure présente mais confuse, progression difficile à suivre. |
| **≤5** | Arc faible | Structure absente ou incompréhensible, pas de progression claire. |

#### Points d'Analyse Critiques

**À vérifier :**
1. ✅ Y a-t-il un point de départ clair (lieu de méditation) ?
2. ✅ La progression vers l'univers thématique est-elle évidente ?
3. ✅ Le point culminant (exploration profonde) est-il identifiable ?
4. ✅ Le retour est-il clairement marqué ?
5. ✅ Le bouclage final au lieu de méditation est-il présent ?

**Description de l'arc dans `arc_description` :**
- Doit résumer l'arc en 1 phrase claire
- Doit mentionner : point de départ → exploration → retour
- Ex. : "De la cabane vers la forêt proche, puis retour progressif" ✅
- Ex. : "Voyage dans l'univers" ❌ (trop vague)

#### Exemples

**10/10 - Arc parfait :**
```
"De la cabane chaleureuse vers la forêt proche, puis retour progressif"
Scène 1: Cabane (ancrage) → Scène 2: Forêt proche → Scène 3: Clairière éloignée 
→ Scène 4: Retour forêt → Scène 5: Cabane (ancrage final)
```

**6/10 - Arc passable :**
```
"Aventure Pokémon"
Scène 1: Chalet → Scène 2: Jardin → Scène 3: Lac (saut spatial !) 
→ Scène 4: Sentier forestier (lieu non vu à l'aller !) → Scène 5: Chalet
```

---

### 2. Cohérence Spatiale (/10)

**Définition :** Évalue la progression logique des lieux et l'absence de sauts spatiaux abrupts.

**Référence :** [`architecture.md:252-256`](../architecture.md:252-256) - "Cohérence spatiale stricte"

#### Barème Détaillé

| Note | Critères | Indicateurs |
|------|----------|-------------|
| **10** | Cohérence parfaite | Progression linéaire sans aucun saut. Retour symétrique par les mêmes lieux. Chaque lieu accessible depuis le précédent. |
| **9** | Excellente cohérence | Progression très claire avec 1 légère imprécision spatiale mineure (ex: description légèrement floue). |
| **8** | Très bonne cohérence | Progression globalement logique mais 1 transition spatiale un peu rapide. |
| **7** | Bonne cohérence | Lieux identifiables mais 1-2 transitions spatiales peu claires. |
| **6** | Cohérence passable | Au moins 1 saut spatial significatif OU retour non symétrique. |
| **≤5** | Cohérence faible | Multiples sauts spatiaux, confusion géographique majeure. |

#### Points d'Analyse Critiques

**Vérifications obligatoires :**

1. **Lieux précis et identifiables**
   - ✅ Chaque scène doit avoir un lieu clairement défini
   - ✅ Description du lieu suffisamment précise pour visualisation
   - ❌ Éviter lieux vagues comme "quelque part", "un endroit"

2. **Transitions géographiques logiques**
   - ✅ Scène N+1 accessible à pied depuis Scène N
   - ✅ Distance cohérente (immédiat → proche → éloigné progressivement)
   - ❌ Sauts instantanés entre lieux éloignés

3. **Retour symétrique OBLIGATOIRE**
   - ✅ Scène 4 doit passer par le lieu de Scène 2
   - ✅ Retour : Scène 3 → Scène 2 → Scène 1
   - ❌ Chemin de retour différent de l'aller

4. **Continuité visuelle forte**
   - ✅ Éléments visuels qui relient les scènes
   - ✅ Axe d'exploration établi (sentier, forêt, etc.)
   - ❌ Rupture visuelle complète entre scènes

**Test de cohérence spatiale :**

```
Question : Pourrait-on tracer le parcours sur une carte ?
- OUI = Cohérence présente
- NON = Problème de cohérence
```

#### Exemples

**10/10 - Cohérence parfaite (Claude Sonnet 4.5) :**
```
Scène 1: Chalet (intérieur, fenêtre)
Scène 2: Forêt de conifères PROCHE du chalet  [continuité immédiate]
Scène 3: Clairière cachée DANS la forêt  [progression logique]
Scène 4: Retour par forêt de conifères puis abords du chalet  [symétrie parfaite]
Scène 5: Chalet (intérieur, fenêtre)  [bouclage]

✅ Aucun saut spatial
✅ Retour symétrique exact
✅ Chaque lieu accessible depuis le précédent
```

**6/10 - Cohérence passable (Claude Haiku 4.5) :**
```
Scène 1: Chalet (fenêtre)
Scène 2: Jardin de pierres IMMÉDIAT du chalet
Scène 3: Lac cristallin AU CŒUR de la montagne  [❌ SAUT SPATIAL ABRUPT]
Scène 4: Sentier forestier  [❌ RETOUR NON SYMÉTRIQUE - pas de jardin]
Scène 5: Chalet

❌ Saut jardin → lac (comment ?)
❌ Retour différent de l'aller (sentier forestier ≠ jardin)
❌ "Sentier forestier" non établi lors de l'exploration
```

**Problèmes fréquents identifiés :**

| Problème | Manifestation | Impact Note |
|----------|---------------|-------------|
| Saut spatial abrupt | Lieu immédiat (jardin) → Lieu éloigné (lac montagne) sans préparation | -2 à -4 points |
| Retour non symétrique | Chemin retour différent de l'aller | -2 à -3 points |
| Sentier/chemin non établi | Transition mentionne un chemin non décrit précédemment | -1 à -2 points |
| Lieux incompatibles | Ex: Auvent du chalet → Sommet montagne directement | -3 à -4 points |

---

### 3. Transitions entre Scènes (/10)

**Définition :** Évalue la fluidité des passages entre scènes et la qualité des `transition_to_next`.

**Référence :** [`architecture.md:146`](../architecture.md:146) - "Créer des transitions fluides entre scènes"

#### Barème Détaillé

| Note | Critères | Indicateurs |
|------|----------|-------------|
| **10** | Transitions parfaites | Chaque transition est fluide, naturelle, et prépare bien la scène suivante. 2-3 phrases décrivant le passage. |
| **9** | Excellentes transitions | Transitions très fluides avec 1 légère imprécision (ex: trop brève mais claire). |
| **8** | Très bonnes transitions | La plupart des transitions sont fluides, 1-2 pourraient être plus détaillées. |
| **7** | Bonnes transitions | Transitions présentes mais certaines manquent de fluidité ou de détails. |
| **6** | Transitions passables | Au moins 1 transition problématique (abrupte, vague, ou chemin non établi). |
| **≤5** | Transitions faibles | Multiples transitions abruptes ou absentes. |

#### Points d'Analyse Critiques

**Structure de transition optimale (2-3 phrases) :**

1. **Élément d'attention** : Qu'est-ce qui attire vers la scène suivante ?
2. **Description du mouvement** : Comment s'effectue le passage ?
3. **Premier élément nouveau** : Qu'est-ce qui annonce la scène suivante ?

**Exemple de structure parfaite :**
```
"L'Évoli se lève doucement [1. élément d'attention] 
et commence à marcher vers un sentier moussu qui s'enfonce 
plus profondément dans la forêt [2. mouvement], 
t'invitant à le suivre [3. annonce]."
```

**Vérifications par transition :**

**Transition Scène 1→2 :**
- ✅ Doit établir le passage du lieu de méditation vers l'extérieur immédiat
- ✅ Peut utiliser un objet de connexion (livre, fenêtre, carte)
- ❌ Éviter : Saut direct sans préparation

**Transition Scène 2→3 :**
- ✅ CRITIQUE : Doit établir clairement le chemin/axe d'exploration
- ✅ Doit préparer l'arrivée au lieu éloigné
- ❌ Éviter : Apparition soudaine d'un nouveau lieu sans lien

**Transition Scène 3→4 :**
- ✅ Doit annoncer le retour
- ✅ Doit mentionner le même chemin qu'à l'aller
- ❌ Éviter : "Retour par un autre chemin"

**Transition Scène 4→5 :**
- ✅ Doit marquer le retour au lieu de méditation
- ✅ Doit introduire l'ambiance sonore
- ❌ Éviter : Arrivée brutale sans préparation

**Guides narratifs (technique avancée) :**

Utilisation de personnages, éléments ou objets pour guider les transitions :
- ✅ Personnages : Pokémon qui guident (Évoli, Gardevoir)
- ✅ Éléments naturels : Sentier, lumière, son, vent
- ✅ Objets : Carte, Poké Ball, livre

**Avantages :**
- Transitions plus naturelles
- Cohérence thématique renforcée
- Dimension émotionnelle ajoutée

#### Exemples

**10/10 - Transitions parfaites (Claude Sonnet 4.5) :**

```json
{
  "transition_to_next": "L'Évoli se lève doucement et commence à marcher 
  vers un sentier moussu qui s'enfonce plus profondément dans la forêt, 
  t'invitant à le suivre."
}
```
✅ 3 éléments présents
✅ Guide narratif (Évoli)
✅ Chemin établi (sentier moussu)

**6/10 - Transition problématique (Gemini Flash) :**

```json
{
  "transition_to_next": "invite à une exploration plus profonde, vers un 
  lieu d'eau, en suivant un petit sentier humide"
}
```
❌ Trop bref (1 seule phrase)
❌ Sentier apparaît soudainement
❌ Pas de guide ni d'élément d'attention

#### Techniques d'Évaluation

**Checklist par transition :**

- [ ] La transition fait 2-3 phrases ou équivalent ?
- [ ] Le passage géographique est-il décrit ?
- [ ] Y a-t-il un élément d'attention/motivation ?
- [ ] La transition prépare-t-elle la scène suivante ?
- [ ] Le chemin/axe est-il cohérent avec la scène précédente ?

**Score :**
- 5/5 cochés = 10/10
- 4/5 cochés = 8-9/10
- 3/5 cochés = 6-7/10
- <3/5 cochés = ≤5/10

---

### 4. Progression Logique (/10)

**Définition :** Évalue le respect de la structure attendue en 5 scènes avec rôles spécifiques.

**Référence :** [`architecture.md:262-266`](../architecture.md:262-266) - "Progression narrative"

#### Barème Détaillé

| Note | Critères | Indicateurs |
|------|----------|-------------|
| **10** | Progression parfaite | Les 5 scènes respectent parfaitement leur rôle attendu. |
| **9** | Excellente progression | 4 scènes parfaites, 1 scène avec légère imprécision. |
| **8** | Très bonne progression | 3-4 scènes respectent leur rôle, 1-2 avec imprécisions. |
| **7** | Bonne progression | Structure identifiable mais 2 scènes s'écartent du rôle attendu. |
| **6** | Progression passable | Au moins 1 scène ne remplit pas du tout son rôle (ex: scène 4 sans retour). |
| **≤5** | Progression faible | Structure non respectée, rôles des scènes confus. |

#### Structure Attendue

**Référence :** Prompt Storyteller, section "Progression narrative"

##### Scène 1 - Ancrage (15% du récit)

**Rôle :**
- ✅ Commencer par la découverte du lieu de méditation
- ✅ Établir une connexion entre le présent et le récit à venir
- ✅ Introduire quelques éléments de l'univers thématique
- ✅ Créer une transition douce vers l'univers thématique

**Vérifications :**
- [ ] Le lieu de méditation est clairement présent ?
- [ ] Un objet/élément de connexion au thème est-il introduit ?
- [ ] L'atmosphère apaisante est-elle établie ?
- [ ] La transition vers l'exploration est-elle amorcée ?

**Exemples de qualité :**

✅ **Excellent :**
```
"Tu es installé dans le chalet en bois, la chaleur t'enveloppe doucement. 
Par la fenêtre embuée, les montagnes se dessinent dans la brume. 
Sur l'appui, une petite Poké Ball ancienne attire ton regard. 
Elle brille légèrement, comme une invitation."
```
- Lieu présent (chalet)
- Objet de connexion (Poké Ball)
- Atmosphère (chaleur, douceur)
- Invitation à l'exploration

❌ **Faible :**
```
"Tu te retrouves au Crétacé supérieur, entouré de dinosaures."
```
- Pas de lieu de méditation
- Saut direct dans le thème
- Pas d'ancrage

##### Scène 2 - Exploration Immédiate (20% du récit)

**Rôle :**
- ✅ Explorer l'univers thématique dans les alentours IMMÉDIATS du lieu
- ✅ Immersion progressive dans le thème
- ✅ Détails sensoriels riches
- ✅ Créer une transition vers une exploration plus profonde
- ✅ **CRITIQUE** : Établir l'axe/chemin d'exploration pour la suite

**Vérifications :**
- [ ] Le lieu est-il proche/immédiat du lieu de méditation ?
- [ ] Le thème est-il présent (personnages, éléments) ?
- [ ] Au moins 3 sens sont-ils sollicités ?
- [ ] Un chemin/axe est-il établi pour aller plus loin ?

**Importance de l'axe d'exploration :**

L'axe d'exploration établi en Scène 2 doit être :
- Clairement mentionné (ex: "sentier", "forêt", "chemin")
- Réutilisé pour le retour en Scène 4
- Point de référence spatial constant

**Exemples :**

✅ **Excellent :**
```
"Tu avances doucement dans la forêt proche du chalet. La pluie tombe 
en rideau doux sur les conifères. Sous un grand sapin, un petit Évoli 
au pelage roux te regarde avec curiosité. Des gouttes brillent sur son nez. 
Tu entends le chant cristallin d'autres Pokémon cachés dans les branches."
```
- Proximité établie ("proche du chalet")
- Thème présent (Évoli, Pokémon)
- Sens : vue, ouïe, toucher (pluie)
- Axe : forêt de conifères

❌ **Faible :**
```
"Un jardin de pierres. Des Pokémon émergent entre les herbes."
```
- Pas de lien spatial avec Scène 1
- Peu de détails sensoriels
- Pas d'axe établi pour la suite

##### Scène 3 - Exploration Profonde (30% du récit - la plus longue)

**Rôle :**
- ✅ Explorer un lieu plus éloigné et plus immersif lié au thème
- ✅ Plongée plus profonde dans l'univers thématique
- ✅ Intensification des éléments sensoriels
- ✅ Point culminant du récit (moment fort)
- ✅ Préparer le retour au lieu de méditation

**Vérifications :**
- [ ] Le lieu est-il plus éloigné que Scène 2 ?
- [ ] Est-ce le moment le plus immersif/fort du récit ?
- [ ] Les éléments sensoriels sont-ils intensifiés ?
- [ ] Le retour est-il amorcé dans la transition ?

**Caractéristiques d'une bonne Scène 3 :**
- Lieu majestueux, secret, ou spécial
- Élément thématique fort (créature légendaire, lieu emblématique)
- Vocabulaire sensoriel riche
- Atmosphère contemplative maximale

**Exemples :**

✅ **Excellent :**
```
"Au cœur de la montagne, tu découvres un lac aux eaux cristallines. 
Là, une créature légendaire se tient immobile, ses ailes déployées 
irradient une lumière dorée apaisante. Son souffle crée des ondulations 
parfaites à la surface de l'eau. Tu t'agenouilles au bord du lac, 
respirant en harmonie avec elle. L'orage gronde maintenant au-dessus 
des pics. C'est un moment d'éternité paisible."
```
- Lieu éloigné et majestueux (cœur de la montagne, lac)
- Élément fort (créature légendaire)
- Sensorialité riche (visuel, auditif, tactile)
- Moment contemplatif ("éternité paisible")
- Préparation du son (orage)

##### Scène 4 - Retour (25% du récit)

**Rôle :**
- ✅ Retour progressif au lieu précédent (Scène 2)
- ✅ Puis retour progressif au lieu initial de méditation (Scène 1)
- ✅ Intensification du son de l'ambiance
- ✅ Clôture apaisante du récit

**Vérifications CRITIQUES :**
- [ ] Le retour passe-t-il par le lieu de Scène 2 ? **OBLIGATOIRE**
- [ ] Le chemin de retour est-il le même qu'à l'aller ?
- [ ] L'ambiance sonore s'intensifie-t-elle ?
- [ ] L'atmosphère reste-t-elle apaisante ?

**Test de symétrie du retour :**

```
Aller : Scène 1 (Chalet) → Scène 2 (Forêt) → Scène 3 (Lac)
Retour : Scène 3 (Lac) → Scène 2 (Forêt) → Scène 1 (Chalet)

✅ Symétrique = Cohérent
❌ Non symétrique = Problème majeur
```

**Exemples :**

✅ **Excellent (symétrie parfaite) :**
```
"Tu retraverses la forêt, accompagné par le petit Évoli. La pluie 
s'intensifie doucement, tambourinant plus fort sur les branches. 
Un éclair lointain illumine brièvement les sapins, suivi d'un grondement 
sourd qui roule entre les montagnes. L'orage est paisible, protecteur. 
Devant toi, les lumières chaudes du chalet apparaissent entre les arbres."
```
- Retour par la forêt (même lieu que Scène 2) ✅
- Intensification sonore (pluie, orage) ✅
- Retour vers chalet (Scène 1) ✅
- Atmosphère apaisante maintenue ✅

❌ **Problématique (retour non symétrique) :**
```
"Tu remontes le sentier forestier, la pluie intensifiant progressivement."
```
- "Sentier forestier" n'était PAS le lieu de Scène 2 (c'était un jardin) ❌
- Pas de mention du lieu de Scène 2 ❌
- Retour non symétrique ❌

##### Scène 5 - Ancrage Final (10% du récit)

**Rôle :**
- ✅ Renforcement du retour au lieu de méditation
- ✅ Dernières images apaisantes de l'aventure
- ✅ Remplacement naturel de la méditation par l'ambiance sonore

**Vérifications :**
- [ ] Le lieu de méditation est-il clairement présent ?
- [ ] Les images finales sont-elles apaisantes ?
- [ ] L'ambiance sonore est-elle introduite naturellement ?
- [ ] La transition vers le sommeil est-elle amorcée ?

**Techniques de bouclage :**
- Retour d'un objet de connexion (ex: Poké Ball qui s'éteint)
- Reprise d'éléments de Scène 1 (ex: fenêtre, chaleur)
- Introduction progressive du son qui remplace le récit

**Exemples :**

✅ **Excellent :**
```
"Te voilà de retour dans le chalet. Tu t'installes confortablement, 
enveloppé de chaleur. Par la fenêtre, la pluie ruisselle en filets réguliers. 
Les éclairs illuminent brièvement les sommets. Le tonnerre roule doucement, 
comme une voix lointaine qui berce. La petite Poké Ball brille une dernière 
fois, puis sa lumière s'éteint paisiblement. Il ne reste plus que toi, 
le chalet, et l'orage qui chante."
```
- Lieu de méditation présent (chalet, fenêtre) ✅
- Bouclage (Poké Ball s'éteint) ✅
- Ambiance sonore (pluie, orage) ✅
- Images apaisantes (chaleur, berceuse) ✅

#### Grille d'Évaluation par Scène

Pour chaque scène, attribuer une note de conformité :

| Scène | Rôle respecté | Note partielle |
|-------|---------------|----------------|
| Scène 1 | ✅ / ⚠️ / ❌ | /2 points |
| Scène 2 | ✅ / ⚠️ / ❌ | /2 points |
| Scène 3 | ✅ / ⚠️ / ❌ | /2 points |
| Scène 4 | ✅ / ⚠️ / ❌ | /2 points |
| Scène 5 | ✅ / ⚠️ / ❌ | /2 points |

**Conversion en note /10 :**
- 10/10 = Toutes scènes ✅
- 8/10 = 4 scènes ✅, 1 scène ⚠️
- 6/10 = 3 scènes ✅, 2 scènes ⚠️ OU 1 scène ❌
- ≤5/10 = 2+ scènes ❌

---

### 5. Connexions (/10)

**Définition :** Évalue la qualité des 5 connexions déclarées dans l'objet `connections` du JSON.

**Référence :** Format JSON Storyteller, champ `connections`

#### Les 5 Connexions Attendues

##### 1. `location_anchor`

**Rôle :** Expliquer comment le récit s'ancre dans le lieu de méditation.

**Critères de qualité :**
- ✅ Mentionne explicitement le lieu de méditation
- ✅ Explique comment le récit débute et se termine dans ce lieu
- ✅ Décrit la transition entre présent (méditation) et récit

**Exemples :**

✅ **Excellent :**
```json
"location_anchor": "Le récit débute dans le chalet en montagne où Léa et 
Vincent découvrent un objet qui les relie à l'univers Pokémon, créant une 
transition douce entre leur lieu de repos et l'aventure contemplative."
```

⚠️ **Passable :**
```json
"location_anchor": "Le récit débute et se termine dans le chalet"
```
(Trop bref, pas d'explication de la transition)

##### 2. `connection_to_theme`

**Rôle :** Expliquer comment le thème est intégré de façon apaisante.

**Critères de qualité :**
- ✅ Mentionne le thème explicitement
- ✅ Explique l'approche apaisante/contemplative (pas combative)
- ✅ Décrit comment les éléments thématiques sont utilisés

**Exemples :**

✅ **Excellent :**
```json
"connection_to_theme": "Le thème Pokémon s'intègre naturellement à travers 
la découverte paisible de créatures douces dans leur habitat montagneux, 
en harmonie avec la nature, loin de tout aspect combatif."
```

❌ **Faible :**
```json
"connection_to_theme": "Les Pokémon sont présents"
```
(Trop vague, pas d'explication de l'approche)

##### 3. `connection_to_exploration`

**Rôle :** Décrire la progression spatiale claire de l'exploration.

**Critères de qualité :**
- ✅ Liste la progression des lieux dans l'ordre
- ✅ Mentionne le point de départ et le point le plus éloigné
- ✅ Explique la logique de progression

**Exemples :**

✅ **Excellent :**
```json
"connection_to_exploration": "Depuis le chalet, le récit invite à explorer 
progressivement les alentours : d'abord la forêt proche sous la pluie, puis 
une clairière cachée avec un lac, avant de revenir par le même chemin."
```

⚠️ **Passable :**
```json
"connection_to_exploration": "Du chalet vers l'extérieur puis retour"
```
(Trop vague, manque de détails)

##### 4. `connection_to_comeback`

**Rôle :** Décrire le retour logique et symétrique.

**Critères de qualité CRITIQUES :**
- ✅ Mentionne explicitement le retour par les mêmes lieux
- ✅ Liste les lieux dans l'ordre inverse
- ✅ Cohérence avec le récit réel (vérifier dans les scènes !)

**Exemples :**

✅ **Excellent :**
```json
"connection_to_comeback": "Le retour se fait en sens inverse : de la 
clairière vers la forêt humide, puis vers le chalet où la pluie bat 
contre les fenêtres, créant une boucle spatiale cohérente et apaisante."
```

❌ **Incohérent :**
```json
"connection_to_comeback": "Le retour suit le même chemin : du lac au 
sentier forestier, puis au jardin"
```
(Si le récit réel ne montre PAS le retour au jardin → Incohérent !)

**Vérification obligatoire :**
Comparer `connection_to_comeback` avec le texte réel de Scène 4 :
- Si les lieux correspondent → ✅
- Si les lieux diffèrent → ❌ Incohérent

##### 5. `connection_to_sound`

**Rôle :** Expliquer comment le récit prépare l'ambiance sonore finale.

**Critères de qualité :**
- ✅ Mentionne l'ambiance sonore (ex: pluie et orage)
- ✅ Explique la progression/intensification du son
- ✅ Décrit comment le son remplace progressivement le récit

**Exemples :**

✅ **Excellent :**
```json
"connection_to_sound": "La pluie est présente dès la scène 2 dans la forêt, 
s'intensifie progressivement avec le tonnerre lointain au retour, pour 
devenir l'élément central à la fin où elle enveloppe totalement le chalet."
```

⚠️ **Passable :**
```json
"connection_to_sound": "L'orage arrive à la fin"
```
(Trop bref, pas de progression décrite)

#### Barème de Notation

| Note | Critères | Indicateurs |
|------|----------|-------------|
| **10** | 5 connexions parfaites | Toutes les connexions sont claires, détaillées, et cohérentes avec le récit |
| **9** | 4-5 connexions excellentes | 1 connexion avec légère imprécision (ex: un peu brève) |
| **8** | 3-4 connexions bonnes | 1-2 connexions avec imprécisions ou trop brèves |
| **7** | 3 connexions acceptables | 2 connexions avec faiblesses notables |
| **6** | 2-3 connexions acceptables | Au moins 1 connexion incohérente avec le récit réel |
| **≤5** | <2 connexions acceptables | Multiples connexions incohérentes ou absentes |

#### Grille d'Évaluation

Pour chaque connexion :

| Connexion | Qualité | Points |
|-----------|---------|--------|
| `location_anchor` | ✅ Excellent / ⚠️ Passable / ❌ Faible | /2 |
| `connection_to_theme` | ✅ Excellent / ⚠️ Passable / ❌ Faible | /2 |
| `connection_to_exploration` | ✅ Excellent / ⚠️ Passable / ❌ Faible | /2 |
| `connection_to_comeback` | ✅ Excellent / ⚠️ Passable / ❌ Faible | /2 |
| `connection_to_sound` | ✅ Excellent / ⚠️ Passable / ❌ Faible | /2 |

**Total /10**

---

## Méthodologie d'Analyse

### Processus Étape par Étape

#### Phase 1 : Préparation (5 min)

**1.1 Lecture de l'architecture**
- [ ] Relire les responsabilités du Storyteller ([`architecture.md:144-151`](../architecture.md:144-151))
- [ ] Relire les contraintes structurelles ([`architecture.md:244-248`](../architecture.md:244-248))
- [ ] Relire les règles de création ([`architecture.md:250-282`](../architecture.md:250-282))

**1.2 Lecture du prompt**
- [ ] Relire le prompt Storyteller complet
- [ ] Noter les contraintes spécifiques (5 scènes, ~300 mots, etc.)

**1.3 Préparation des fichiers**
- [ ] Ouvrir tous les fichiers benchmark à analyser
- [ ] Créer un document de notes pour l'analyse
- [ ] Préparer les grilles de notation

#### Phase 2 : Lecture Globale (10 min par modèle)

**2.1 Première lecture complète**
- [ ] Lire le JSON complet sans noter
- [ ] Se faire une impression générale de la qualité
- [ ] Identifier les forces et faiblesses évidentes

**2.2 Lecture du récit narratif**
- [ ] Lire les 5 `narrative_text` à la suite
- [ ] Évaluer la fluidité de lecture
- [ ] Noter si l'histoire est compréhensible et cohérente

**2.3 Examen des connexions**
- [ ] Lire les 5 connexions
- [ ] Noter si elles correspondent à l'impression du récit

#### Phase 3 : Analyse Détaillée (30-40 min par modèle)

**3.1 Analyse Arc Narratif**

Méthode :
1. Lire `arc_description`
2. Lister la progression des lieux : Scène 1 → 2 → 3 → 4 → 5
3. Vérifier si la structure Ancrage → Exploration → Profonde → Retour → Ancrage est respectée
4. Attribuer une note selon le barème

**Checklist :**
- [ ] Arc description clair et concis ?
- [ ] Progression visible à la lecture ?
- [ ] Structure en 5 étapes respectée ?
- [ ] Note attribuée et justifiée

**3.2 Analyse Cohérence Spatiale**

Méthode :
1. Créer un schéma spatial :
   ```
   Scène 1: [Lieu]
       ↓
   Scène 2: [Lieu - proximité ?]
       ↓
   Scène 3: [Lieu - progression logique ?]
       ↓
   Scène 4: [Lieu - retour par Scène 2 ?]
       ↓
   Scène 5: [Lieu - retour Scène 1 ?]
   ```

2. Vérifier chaque transition :
   - Scène N+1 accessible depuis Scène N ?
   - Distance cohérente ?
   - Sauts spatiaux ?

3. Vérifier la symétrie du retour :
   - Scène 4 passe-t-elle par Scène 2 ?
   - Chemin identique à l'aller ?

**Checklist :**
- [ ] Schéma spatial tracé
- [ ] Transitions vérifiées
- [ ] Symétrie du retour vérifiée
- [ ] Problèmes identifiés et documentés
- [ ] Note attribuée et justifiée

**3.3 Analyse Transitions**

Méthode :
1. Pour chaque `transition_to_next` :
   - Compter les phrases/éléments
   - Identifier : élément d'attention + mouvement + annonce
   - Vérifier cohérence avec scène suivante

2. Noter les guides narratifs utilisés
3. Identifier les transitions problématiques

**Checklist par transition :**
- [ ] Transition 1→2 : Longueur, qualité, cohérence
- [ ] Transition 2→3 : Longueur, qualité, établissement axe
- [ ] Transition 3→4 : Longueur, qualité, annonce retour
- [ ] Transition 4→5 : Longueur, qualité, préparation son
- [ ] Note globale attribuée et justifiée

**3.4 Analyse Progression Logique**

Méthode :
1. Pour chaque scène, vérifier le rôle attendu :
   - Scène 1 : Ancrage + connexion thème
   - Scène 2 : Exploration immédiate + axe établi
   - Scène 3 : Exploration profonde + point culminant
   - Scène 4 : Retour symétrique + intensification son
   - Scène 5 : Ancrage final + préparation son

2. Attribuer ✅ / ⚠️ / ❌ à chaque scène
3. Calculer note globale

**Checklist :**
- [ ] Scène 1 évaluée (✅/⚠️/❌)
- [ ] Scène 2 évaluée (✅/⚠️/❌)
- [ ] Scène 3 évaluée (✅/⚠️/❌)
- [ ] Scène 4 évaluée (✅/⚠️/❌)
- [ ] Scène 5 évaluée (✅/⚠️/❌)
- [ ] Note globale calculée et justifiée

**3.5 Analyse Connexions**

Méthode :
1. Pour chaque connexion :
   - Lire la déclaration
   - Vérifier cohérence avec le récit réel
   - Évaluer qualité (détail, clarté)

2. **IMPORTANT** : Pour `connection_to_comeback`, comparer avec Scène 4
3. Attribuer ✅ / ⚠️ / ❌ à chaque connexion

**Checklist :**
- [ ] `location_anchor` évalué (✅/⚠️/❌)
- [ ] `connection_to_theme` évalué (✅/⚠️/❌)
- [ ] `connection_to_exploration` évalué (✅/⚠️/❌)
- [ ] `connection_to_comeback` évalué et vérifié contre récit (✅/⚠️/❌)
- [ ] `connection_to_sound` évalué (✅/⚠️/❌)
- [ ] Note globale calculée et justifiée

#### Phase 4 : Synthèse (15 min par modèle)

**4.1 Calcul des notes**
- [ ] Arc Narratif : ___ /10
- [ ] Cohérence Spatiale : ___ /10
- [ ] Transitions : ___ /10
- [ ] Progression Logique : ___ /10
- [ ] Connexions : ___ /10
- [ ] **Total : ___ /50**

**4.2 Identification Points Forts**
Lister 3-5 points forts majeurs avec exemples concrets

**4.3 Identification Points Faibles**
Lister 3-5 points faibles majeurs avec exemples concrets

**4.4 Recommandation**
Selon la note globale :
- 45-50 : Recommandé pour production
- 40-44 : Viable pour production/A/B
- 35-39 : Acceptable avec réserves
- 30-34 : Non recommandé
- <30 : À éviter

#### Phase 5 : Analyse Comparative (20 min)

**5.1 Classement**
Classer les modèles du meilleur au moins bon

**5.2 Analyse par critère**
Pour chaque critère, classer les modèles et identifier l'écart

**5.3 Problèmes récurrents**
Identifier les problèmes présents dans plusieurs modèles

**5.4 Innovations remarquables**
Identifier les techniques/approches réussies

#### Phase 6 : Recommandations (15 min)

**6.1 Sélection modèle**
- Modèle recommandé principal
- Modèle alternatif viable
- Modèles à éviter

**6.2 Amélioration prompt**
- Problèmes à résoudre
- Règles à renforcer
- Exemples à ajouter

**6.3 Validation automatique**
- Checks à implémenter
- Seuils de qualité à définir

### Temps Total Estimé

- 1 modèle : ~60-70 min
- 4 modèles : ~4-5 heures (avec pauses)
- Analyse comparative + recommandations : +1 heure

**Total pour analyse complète : 5-6 heures**

---

## Exemples de Niveaux de Qualité

### Excellence (9-10/10)

#### Arc Narratif Excellent

**Claude Sonnet 4.5 :**
```json
{
  "arc_description": "Depuis le chalet, une exploration contemplative 
  mène à travers la forêt pluvieuse jusqu'à une clairière secrète habitée 
  de Pokémon paisibles, avant un retour progressif bercé par l'orage."
}
```

**Pourquoi c'est excellent :**
- ✅ Progression claire : chalet → forêt → clairière → retour
- ✅ Mention du thème (Pokémon paisibles)
- ✅ Atmosphère établie (contemplative, bercé)
- ✅ Retour explicitement mentionné

#### Cohérence Spatiale Excellente

**Progression linéaire parfaite :**
```
Scène 1: Chalet (intérieur, fenêtre)
    ↓ "forêts environnantes du chalet"
Scène 2: Forêt de conifères proche du chalet
    ↓ "sentier moussu plus profondément dans la forêt"
Scène 3: Clairière cachée dans la forêt
    ↓ "reprend le chemin de la forêt"
Scène 4: Forêt de conifères puis abords du chalet
    ↓ "lumières du chalet apparaissent"
Scène 5: Chalet (intérieur, fenêtre)
```

**Pourquoi c'est excellent :**
- ✅ Aucun saut spatial
- ✅ Progression logique et continue
- ✅ Retour symétrique exact (forêt → chalet)
- ✅ Chaque lieu accessible depuis le précédent

#### Transition Excellente

**Exemple (Claude Sonnet 4.5, Scène 2→3) :**
```json
{
  "transition_to_next": "L'Évoli se lève doucement et commence à marcher 
  vers un sentier moussu qui s'enfonce plus profondément dans la forêt, 
  t'invitant à le suivre."
}
```

**Pourquoi c'est excellent :**
- ✅ 3 éléments présents :
  1. Élément d'attention : Évoli se lève
  2. Mouvement : marcher vers sentier
  3. Annonce : s'enfonce dans forêt
- ✅ Guide narratif (Évoli)
- ✅ Établissement du chemin (sentier moussu)
- ✅ Invitation douce (t'invitant)

### Bon (7-8/10)

#### Arc Narratif Bon

**Exemple :**
```json
{
  "arc_description": "Un voyage imaginaire depuis le chalet vers un lac 
  alpin où dorment des Pokémon, avant un retour paisible sous une pluie 
  apaisante."
}
```

**Pourquoi c'est bon mais pas excellent :**
- ✅ Progression présente
- ✅ Retour mentionné
- ⚠️ Manque détails sur les étapes intermédiaires
- ⚠️ "Voyage" un peu vague

#### Cohérence Spatiale Bonne

**Progression avec légère imprécision :**
```
Scène 1: Chalet (carte mystérieuse)
    ↓ "Le regard vers la fenêtre"
Scène 2: Sentier de montagne menant au lac
    ↓ "Le chemin se resserre vers les rives"
Scène 3: Bord du lac + grotte cachée
    ↓ "Retraçant les pas vers le sentier"
Scène 4: Sentier puis abords du chalet
    ↓
Scène 5: Chalet (intérieur)
```

**Pourquoi c'est bon mais pas excellent :**
- ✅ Progression globalement logique
- ✅ Retour symétrique
- ⚠️ "Grotte cachée" apparaît un peu brusquement
- ⚠️ Transition scène 2→3 pourrait être plus détaillée

### Passable (6/10)

#### Cohérence Spatiale Passable

**Progression avec saut spatial :**
```
Scène 1: Chalet (fenêtre)
    ↓ "Tu franchis le seuil"
Scène 2: Jardin de pierres immédiat
    ↓ "Guidé par les Pokémon, tu suis un sentier"
Scène 3: Lac cristallin au cœur de la montagne  [❌ SAUT ABRUPT]
    ↓ "Tu retournes"
Scène 4: Sentier forestier  [❌ DIFFÉRENT DU JARDIN]
    ↓
Scène 5: Chalet
```

**Pourquoi c'est passable :**
- ⚠️ Jardin (scène 2) → Lac montagne (scène 3) : saut spatial
- ❌ Retour par "sentier forestier" ≠ "jardin de pierres"
- ❌ Incohérence du chemin

#### Transition Passable

**Exemple :**
```json
{
  "transition_to_next": "invite à une exploration plus profonde, vers un 
  lieu d'eau, en suivant un petit sentier humide"
}
```

**Pourquoi c'est passable :**
- ⚠️ Trop bref (1 seule phrase)
- ❌ Sentier apparaît soudainement
- ⚠️ Pas de guide ni d'élément d'attention clair

### Insuffisant (≤5/10)

#### Cohérence Spatiale Insuffisante

**Multiples sauts spatiaux :**
```
Scène 1: Bibliothèque
    ↓
Scène 2: Forêt préhistorique  [❌ SAUT]
    ↓
Scène 3: Clairière avec dinosaures  [Logique mais...]
    ↓
Scène 4: Plage  [❌ SAUT INCOMPRÉHENSIBLE]
    ↓
Scène 5: Bibliothèque
```

**Pourquoi c'est insuffisant :**
- ❌ Bibliothèque → Forêt : saut total
- ❌ Clairière → Plage : incohérent
- ❌ Pas de progression logique
- ❌ Retour non symétrique

---

## Validation et Contrôle Qualité

### Validation Technique (Format JSON)

#### Checklist Format

**Champs obligatoires (⭐) :**
- [ ] `version`
- [ ] `original_context.user_name`
- [ ] `original_context.sleep_duration`
- [ ] `storyteller_output.connections` (5 sous-champs)
- [ ] `storyteller_output.theme` (complet)
- [ ] `storyteller_output.location` (complet)
- [ ] `storyteller_output.ambiance_sound` (complet)
- [ ] `storyteller_output.narrative.arc_description`
- [ ] `storyteller_output.narrative.total_scenes`
- [ ] `storyteller_output.narrative.scenes` (array de 5)

**Pour chaque scène (⭐) :**
- [ ] `scene_number`
- [ ] `title`
- [ ] `location`
- [ ] `atmosphere`
- [ ] `sensory_elements` (au moins visual et auditory)
- [ ] `narrative_text`
- [ ] `meditation_hints`
- [ ] `transition_to_next`

### Validation Contraintes Structurelles

**Référence :** [`architecture.md:244-248`](../architecture.md:244-248)

| Contrainte | Valeur Attendue | Tolérance | Validation |
|------------|-----------------|-----------|------------|
| Nombre de scènes | 5 | Aucune | Exact = ✅ |
| Longueur totale | ~300 mots | ±30 mots | 270-330 = ✅ |
| Longueur par scène | 30-70 mots | ±10 mots | 20-80 = ✅ |
| Arc narratif | Début→Exploration→Retour | - | Subjectif |
| Format sortie | JSON | - | Valid JSON = ✅ |

#### Script de Validation Automatique

```javascript
function validateStorytellerOutput(output) {
  const errors = [];
  const warnings = [];
  
  // 1. Nombre de scènes
  const sceneCount = output.storyteller_output.narrative.scenes.length;
  if (sceneCount !== 5) {
    errors.push(`Nombre de scènes incorrect : ${sceneCount} (attendu: 5)`);
  }
  
  // 2. Longueur totale
  const totalWords = output.storyteller_output.narrative.scenes
    .reduce((sum, scene) => sum + scene.narrative_text.split(/\s+/).length, 0);
  if (totalWords < 270 || totalWords > 330) {
    warnings.push(`Longueur totale : ${totalWords} mots (recommandé: 270-330)`);
  }
  
  // 3. Longueur par scène
  output.storyteller_output.narrative.scenes.forEach((scene, idx) => {
    const words = scene.narrative_text.split(/\s+/).length;
    if (words < 20 || words > 80) {
      warnings.push(`Scène ${idx + 1}: ${words} mots (recommandé: 30-70)`);
    }
  });
  
  // 4. Champs obligatoires par scène
  output.storyteller_output.narrative.scenes.forEach((scene, idx) => {
    const required = ['scene_number', 'location', 'narrative_text', 
                     'transition_to_next', 'sensory_elements'];
    required.forEach(field => {
      if (!scene[field]) {
        errors.push(`Scène ${idx + 1}: champ "${field}" manquant`);
      }
    });
    
    if (scene.sensory_elements && 
        (!scene.sensory_elements.visual || !scene.sensory_elements.auditory)) {
      errors.push(`Scène ${idx + 1}: manque visual ou auditory`);
    }
  });
  
  // 5. Connexions
  const connections = output.storyteller_output.connections;
  const requiredConnections = ['location_anchor', 'connection_to_theme', 
    'connection_to_exploration', 'connection_to_comeback', 'connection_to_sound'];
  requiredConnections.forEach(conn => {
    if (!connections[conn]) {
      errors.push(`Connexion "${conn}" manquante`);
    }
  });
  
  return {
    valid: errors.length === 0,
    errors,
    warnings,
    metrics: {
      sceneCount,
      totalWords,
      averageWordsPerScene: Math.round(totalWords / sceneCount)
    }
  };
}
```

### Validation Qualité Narrative

#### Checklist Rapide

**Questions de validation :**

1. **Cohérence spatiale**
   - [ ] Peut-on tracer le parcours sur une carte ?
   - [ ] Le retour passe-t-il par les mêmes lieux que l'aller ?

2. **Atmosphère apaisante**
   - [ ] Y a-t-il des éléments de danger ou de tension ?
   - [ ] Le vocabulaire est-il simple et sensoriel ?

3. **Transitions**
   - [ ] Chaque transition fait-elle au moins 2 phrases ?
   - [ ] Le passage entre lieux est-il décrit ?

4. **Progression logique**
   - [ ] Scène 1 = Ancrage dans lieu de méditation ?
   - [ ] Scène 3 = Point culminant/moment fort ?
   - [ ] Scène 4 = Retour symétrique ?
   - [ ] Scène 5 = Retour au lieu + préparation son ?

5. **Connexions**
   - [ ] `connection_to_comeback` correspond-elle au récit réel ?

**Seuils de qualité minimale :**

Pour être utilisable en production :
- Note globale ≥ 40/50
- Cohérence spatiale ≥ 8/10
- Aucun problème critique (retour non symétrique, danger, etc.)

---

## Reporting et Documentation

### Structure du Rapport d'Analyse

#### 1. En-tête

```markdown
# Analyse Benchmark Storyteller : [Nom du Modèle]

**Date :** [Date]
**Analyseur :** [Nom]
**Modèle analysé :** [Nom + version]
**Prompt utilisé :** [Référence au prompt]
**Thème/Lieu testé :** [Thème] / [Lieu]
```

#### 2. Résumé Exécutif

```markdown
## Résumé Exécutif

**Note globale :** XX/50

**Recommandation :** [Recommandé / Viable / Acceptable / Non recommandé / À éviter]

**Forces principales :**
- [Force 1]
- [Force 2]

**Faiblesses principales :**
- [Faiblesse 1]
- [Faiblesse 2]
```

#### 3. Grille de Notation

```markdown
## Grille de Notation

| Critère | Note | Justification |
|---------|------|---------------|
| Arc Narratif | X/10 | [1-2 phrases] |
| Cohérence Spatiale | X/10 | [1-2 phrases] |
| Transitions | X/10 | [1-2 phrases] |
| Progression Logique | X/10 | [1-2 phrases] |
| Connexions | X/10 | [1-2 phrases] |
| **TOTAL** | **XX/50** | |
```

#### 4. Analyse Détaillée par Critère

Pour chaque critère, structure :

```markdown
### [Nom du Critère] : X/10

[Analyse détaillée avec exemples concrets du JSON]

**Points forts :**
- [Point 1 avec exemple]

**Points faibles :**
- [Point 1 avec exemple]
```

#### 5. Points Forts Globaux

```markdown
## Points Forts

1. **[Titre du point fort]**
   - Description
   - Exemple concret du JSON
   - Impact positif

[Répéter pour 3-5 points forts]
```

#### 6. Points Faibles Globaux

```markdown
## Points Faibles

1. **[Titre du point faible]**
   - Description du problème
   - Exemple concret du JSON
   - Impact négatif
   - [Optionnel] Suggestion d'amélioration

[Répéter pour 3-5 points faibles]
```

#### 7. Conclusion et Recommandation

```markdown
## Conclusion

[Paragraphe de synthèse]

**Recommandation finale :** [Recommandé / Viable / etc.]

**Utilisation suggérée :**
- [Production / A/B testing / Éviter / etc.]
- [Contexte d'utilisation optimal si applicable]

**Améliorations nécessaires :**
- [Si non recommandé, liste des améliorations requises]
```

### Format Comparatif Multi-Modèles

```markdown
# Analyse Comparative Benchmarks Storyteller

**Date :** [Date]
**Modèles analysés :** [Liste]
**Prompt utilisé :** [Référence]

## Classement Final

| Rang | Modèle | Note | Recommandation |
|------|--------|------|----------------|
| 1 | [Modèle] | XX/50 | [Recommandé] |
| 2 | [Modèle] | XX/50 | [Viable] |
| ... | ... | ... | ... |

## Analyse par Critère

### Cohérence Spatiale (Critère le plus discriminant)

[Analyse comparative...]

[Répéter pour chaque critère]

## Problèmes Récurrents

[Liste et analyse des problèmes présents dans plusieurs modèles]

## Innovations Remarquables

[Liste et analyse des techniques réussies]

## Recommandations

### Pour la sélection du modèle
[Modèle principal + alternatives]

### Pour l'amélioration des prompts
[Liste des améliorations à apporter]

### Pour la validation automatique
[Checks à implémenter]
```

### Fichiers de Sortie

**Structure recommandée :**

```
/analyse
  /benchmarks
    /[date]-[modele].md          # Analyse individuelle
    /[date]-comparison.md        # Analyse comparative
  /guides
    guide_evaluation_storyteller.md  # Ce guide
```

**Nommage des fichiers :**
- Format date : `YYYY-MM-DD`
- Format modèle : `provider-model-version`
- Ex: `2025-10-30-anthropic-claude-sonnet-4.5.md`

---

## Annexes

### Glossaire

**Arc narratif :** Structure globale du récit (début → milieu → fin).

**Cohérence spatiale :** Progression logique et continue des lieux sans sauts abrupts.

**Retour symétrique :** Le chemin de retour passe par les mêmes lieux que l'aller, dans l'ordre inverse.

**Axe d'exploration :** Élément spatial constant qui guide l'exploration (ex: forêt, sentier).

**Guide narratif :** Personnage, objet ou élément utilisé pour fluidifier les transitions.

**Saut spatial :** Passage abrupt entre deux lieux éloignés sans transition appropriée.

**Objet de connexion :** Élément tangible reliant le lieu de méditation au thème (ex: livre, carte, Poké Ball).

### Références

- **Architecture :** [`architecture.md`](../architecture.md)
- **Prompt Storyteller :** [`prompt_storyteller.md`](../prompt_storyteller.md)
- **Exemple d'analyse :** [`analyse/benchmark_storyteller_qualite_narrative.md`](benchmark_storyteller_qualite_narrative.md)

### Changelog du Guide

| Version | Date | Changements |
|---------|------|-------------|
| 1.0 | 2025-10-30 | Création initiale du guide méthodologique |

---

**Fin du Guide Méthodologique d'Évaluation du Storyteller**
