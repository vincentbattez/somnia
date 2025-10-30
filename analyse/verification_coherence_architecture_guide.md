# Vérification de Cohérence : Architecture vs Guide d'Évaluation

**Date :** 30 octobre 2025  
**Objectif :** Vérifier la cohérence complète entre `architecture.md` (sections 137-313) et `guide_evaluation_storyteller.md`

---

## Résumé Exécutif

### Résultats de la Vérification

| Aspect | Statut | Détails |
|--------|--------|---------|
| **Critères principaux** | ✅ Alignés | 5 critères définis dans les deux documents |
| **Responsabilités** | ✅ Alignées | Identiques dans les deux documents |
| **Contraintes structurelles** | ⚠️ Divergence | Architecture : 3-4 scènes / Guide : 5 scènes |
| **Vocabulaire sensoriel** | ✅ Aligné | Mêmes règles dans les deux documents |
| **Atmosphère apaisante** | ✅ Alignée | Mêmes critères dans les deux documents |
| **Innovations** | ✅ Intégrées | Guide inclut innovations identifiées dans benchmarks |
| **Exemples** | ⚠️ Divergence | Architecture : exemples génériques / Guide : exemples spécifiques |

### Divergences Identifiées

**1. Nombre de scènes (CRITIQUE)**
- Architecture (ligne 245) : "3-4 scènes maximum"
- Guide : "5 scènes progressives"
- **Impact :** Contradiction majeure sur la structure attendue

**2. Longueur totale (CRITIQUE)**
- Architecture (ligne 246) : "~200 mots"
- Guide : "~300 mots"
- **Impact :** Différence de 50% sur la longueur attendue

**3. Longueur par scène (MINEURE)**
- Architecture (ligne 247) : "50-70 mots"
- Guide : "30-70 mots"
- **Impact :** Plage plus large dans le guide

**4. Exemples (MINEURE)**
- Architecture : Exemples génériques (dinosaures, bibliothèque)
- Guide : Exemples spécifiques (Claude Sonnet, Gemini Flash)
- **Impact :** Guide plus concret mais moins générique

---

## Analyse Détaillée

### 1. Critères Principaux

#### Architecture (lignes 144-151)

**Responsabilités ✅ :**
- ✅ Concevoir un **arc narratif** simple et clair
- ✅ Créer des **transitions fluides** entre scènes
- ✅ Utiliser un **vocabulaire sensoriel** simple
- ✅ Assurer la **cohérence spatiale**
- ✅ Maintenir une **atmosphère apaisante**
- ✅ Respecter le thème et le lieu fournis

#### Guide d'Évaluation

**Critères de notation :**
1. Arc Narratif (/10)
2. Cohérence Spatiale (/10)
3. Transitions (/10)
4. Progression Logique (/10)
5. Connexions (/10)

**Analyse de cohérence :**
- ✅ Les 5 critères du guide couvrent les 6 responsabilités de l'architecture
- ✅ "Progression Logique" couvre "atmosphère apaisante" + "respect thème/lieu"
- ✅ "Connexions" est un critère supplémentaire (non dans architecture)
- ✅ Alignement global : BON

**Recommandation :** Ajouter "Connexions" comme responsabilité dans architecture.md

---

### 2. Contraintes Structurelles (DIVERGENCE CRITIQUE)

#### Architecture (lignes 244-248)

```
- **Nombre de scènes** : 3-4 maximum
- **Longueur totale** : ~200 mots (tous textes narratifs combinés)
- **Longueur par scène** : 50-70 mots de prose
- **Arc narratif** : Début → Exploration → Retour
```

#### Guide d'Évaluation

```
- **Nombre de scènes** : 5 scènes progressives
- **Longueur totale** : ~300 mots
- **Longueur par scène** : 30-70 mots
- **Arc narratif** : Ancrage → Exploration → Exploration profonde → Retour → Ancrage final
```

#### Analyse de Divergence

**Nombre de scènes :**
- Architecture : 3-4 scènes
- Guide : 5 scènes
- **Source de la divergence :** 
  - Architecture (ligne 262-266) décrit une progression en 5 étapes : Scène 1 (Ancrage), Scène 2 (Exploration), Scène 3 (Exploration profonde), Scène 4 (Retour), Scène 5 (Ancrage final)
  - Mais contrainte structurelle (ligne 245) dit "3-4 scènes maximum"
  - **INCOHÉRENCE INTERNE DANS ARCHITECTURE.MD**

**Longueur totale :**
- Architecture : ~200 mots
- Guide : ~300 mots
- **Source de la divergence :**
  - Prompt Storyteller (input.md ligne 46) : "~300 mots"
  - Architecture (ligne 246) : "~200 mots"
  - **INCOHÉRENCE AVEC LE PROMPT ORIGINAL**

**Longueur par scène :**
- Architecture : 50-70 mots
- Guide : 30-70 mots
- **Justification du guide :** Plage plus large pour accommoder 5 scènes avec ~300 mots total

#### Recommandation

**SYNCHRONISATION REQUISE :**

Option 1 : Aligner sur le prompt original (300 mots, 5 scènes)
```
- Nombre de scènes : 5
- Longueur totale : ~300 mots (±30 mots)
- Longueur par scène : 50-70 mots (moyenne 60 mots)
- Arc narratif : Ancrage → Exploration → Exploration profonde → Retour → Ancrage final
```

Option 2 : Aligner sur architecture.md (200 mots, 3-4 scènes)
```
- Nombre de scènes : 3-4
- Longueur totale : ~200 mots (±20 mots)
- Longueur par scène : 50-70 mots
- Arc narratif : Début → Exploration → Retour
```

**Recommandation prioritaire :** Option 1 (aligner sur prompt original qui est la source de vérité)

---

### 3. Progression Narrative

#### Architecture (lignes 262-266)

```
**Scène 1 - Ancrage** (15%)
- Commence par la découverte du lieu de méditation
- Établit une connexion entre le présent et le récit à venir
- Introduit quelques éléments de l'univers thématique
- Crée une transition douce vers l'univers thématique

**Scène 2 - Exploration** (20%)
- Exploration de l'univers thématique dans les alentours du lieu
- Immersion progressive dans le thème
- Détails sensoriels riches
- Créer une transition vers une exploration plus profonde

**Scène 3 - Exploration profonde** (30%)
- Exploration d'un autre lieu plus éloigné et plus immersif
- Plongée plus profonde dans l'univers thématique
- Intensification des éléments sensoriels
- Préparation du retour

**Scène 4 - Retour** (25%)
- Retour progressif au lieu précédent (scène 2)
- Puis retour progressif au lieu initial (scène 1)
- Intensification du son de l'ambiance
- Clôture apaisante du récit

**Scène 5 - Ancrage final** (10%)
- Renforcement du retour au lieu de méditation
- Dernières images apaisantes
- Remplacement naturel de la méditation par l'ambiance sonore
```

#### Guide d'Évaluation

**Scène 1 - Ancrage (15% du récit)**
- ✅ Identique à architecture.md

**Scène 2 - Exploration Immédiate (20% du récit)**
- ✅ Identique à architecture.md
- ✅ Guide ajoute : "Établir l'axe/chemin d'exploration pour la suite" (IMPORTANT)

**Scène 3 - Exploration Profonde (30% du récit)**
- ✅ Identique à architecture.md
- ✅ Guide ajoute : "Point culminant du récit (moment fort)"

**Scène 4 - Retour (25% du récit)**
- ✅ Identique à architecture.md
- ✅ Guide ajoute : "Test de symétrie du retour (OBLIGATOIRE)"

**Scène 5 - Ancrage Final (10% du récit)**
- ✅ Identique à architecture.md
- ✅ Guide ajoute : "Techniques de bouclage"

**Analyse de cohérence :**
- ✅ Alignement parfait sur la structure
- ✅ Guide enrichit avec détails d'évaluation
- ✅ Pas de divergence

**Recommandation :** Ajouter dans architecture.md les points enrichis du guide (axe d'exploration, test symétrie, techniques de bouclage)

---

### 4. Vocabulaire Sensoriel

#### Architecture (lignes 257-260)

```
**✅ UTILISER :**
- Descriptions sensorielles concrètes : "lumière douce", "bruit de l'eau", "chaleur agréable"
- Mots simples et évocateurs
- Images visualisables facilement
- Première mention subtile de l'ambiance sonore

**❌ ÉVITER :**
- Concepts abstraits ou vagues
```

#### Guide d'Évaluation

**Critère : Vocabulaire sensoriel simple**
- ✅ Mêmes règles que architecture.md
- ✅ Guide ajoute : "Au moins 3 sens par scène (vue, ouïe, toucher prioritaires)"
- ✅ Guide ajoute : "Détails concrets et visualisables"

**Analyse de cohérence :**
- ✅ Alignement parfait
- ✅ Guide enrichit avec critères mesurables

**Recommandation :** Ajouter dans architecture.md le critère "Au moins 3 sens par scène"

---

### 5. Atmosphère Apaisante

#### Architecture (lignes 268-272)

```
**✅ PRIVILÉGIER :**
- Observation calme et contemplation
- Immersion douce et progressive
- Rythme lent et paisible
- Images sécurisantes
- Sensations agréables

**❌ ÉVITER ABSOLUMENT :**
- Danger ou menace
- Conflit ou tension
- Rythme rapide ou action
- Situations stressantes
- Éléments anxiogènes
```

#### Guide d'Évaluation

**Critère : Atmosphère relaxante OBLIGATOIRE**
- ✅ Mêmes règles que architecture.md
- ✅ Guide ajoute : "Pas de danger, conflit, ou tension"
- ✅ Guide ajoute : "Rythme lent et contemplatif"

**Analyse de cohérence :**
- ✅ Alignement parfait
- ✅ Pas de divergence

---

### 6. Lien avec l'Ambiance Sonore

#### Architecture (lignes 279-281)

```
**6. Lien avec l'ambiance sonore**
- La dernière scène doit préparer l'arrivée du son
- Ex: Si "pluie", introduire progressivement l'eau, l'humidité
```

#### Guide d'Évaluation

**Critère : Connexion `connection_to_sound`**
- ✅ Mêmes règles que architecture.md
- ✅ Guide ajoute : "Progression/intensification du son"
- ✅ Guide ajoute : "Comment le son remplace progressivement le récit"

**Analyse de cohérence :**
- ✅ Alignement parfait
- ✅ Guide enrichit avec critères mesurables

---

### 7. Innovations Identifiées dans les Benchmarks

#### Absentes de l'Architecture

**Innovations découvertes dans l'analyse des benchmarks :**

1. **Pokémon comme guides narratifs** (Claude Sonnet 4.5)
   - Évoli guide vers la clairière
   - Noctali guide le retour
   - Technique très efficace pour transitions fluides

2. **Objet de connexion** (Claude Sonnet 4.5 & Gemini Flash2)
   - Poké Ball ancienne (brille au début, s'éteint à la fin)
   - Carte mystérieuse avec symbole Poké Ball
   - Crée un bouclage narratif satisfaisant

3. **Axe d'exploration clair** (Gemini Flash2)
   - Sentier établi dès scène 2
   - Même sentier pour aller et retour
   - Facilite compréhension spatiale

**Statut dans les documents :**
- ❌ Architecture.md : Ne mentionne pas ces innovations
- ✅ Guide d'Évaluation : Inclut ces innovations comme "techniques avancées"

**Recommandation :** Ajouter une section "Techniques avancées recommandées" dans architecture.md

---

### 8. Exemples

#### Architecture (lignes 283-312)

**Mauvais exemple :**
```
"Scène 1: Le Mésozoïque
Tu te retrouves au Crétacé supérieur, entouré de dinosaures herbivores..."
```
- Problèmes : Vocabulaire technique, danger, pas de lien avec lieu méditation

**Bon exemple :**
```
"Scène 1: Le livre ancien
Dans le fauteuil de cuir, tu tiens un livre illustré..."
```
- Forces : Ancrage, vocabulaire simple, sensorialité

#### Guide d'Évaluation

**Exemples spécifiques des benchmarks :**
- Claude Sonnet 4.5 (10/10) : Transitions parfaites avec Pokémon guides
- Gemini Flash2 (9/10) : Cohérence spatiale excellente avec sentier
- Claude Haiku 4.5 (6/10) : Saut spatial jardin→lac
- Gemini Flash (6/10) : Transitions trop brèves

**Analyse de cohérence :**
- ✅ Architecture : Exemples génériques et pédagogiques
- ✅ Guide : Exemples spécifiques et concrets
- ✅ Complémentarité : Les deux approches sont utiles

**Recommandation :** Ajouter dans architecture.md une section "Exemples de benchmarks réels" renvoyant au guide

---

## Tableau Récapitulatif des Divergences

| Aspect | Architecture | Guide | Divergence | Sévérité | Recommandation |
|--------|--------------|-------|-----------|----------|----------------|
| Nombre de scènes | 3-4 | 5 | OUI | CRITIQUE | Aligner sur prompt (5 scènes) |
| Longueur totale | ~200 mots | ~300 mots | OUI | CRITIQUE | Aligner sur prompt (300 mots) |
| Longueur/scène | 50-70 | 30-70 | OUI | MINEURE | Adapter à 5 scènes |
| Progression narrative | 4 étapes | 5 étapes | OUI | CRITIQUE | Aligner sur 5 étapes |
| Critères évaluation | 6 responsabilités | 5 critères | OUI | MINEURE | Ajouter "Connexions" |
| Vocabulaire sensoriel | Règles générales | Règles + "3 sens" | NON | - | Ajouter dans architecture |
| Atmosphère apaisante | Règles générales | Règles identiques | NON | - | Aligné |
| Ambiance sonore | Règles générales | Règles + progression | NON | - | Ajouter dans architecture |
| Innovations | Absentes | Incluses | OUI | MINEURE | Ajouter section dans architecture |
| Exemples | Génériques | Spécifiques | NON | - | Complémentaires |

---

## Recommandations de Synchronisation

### Priorité 1 : CRITIQUE (Divergences majeures)

#### 1.1 Aligner le nombre de scènes et la longueur

**Changement dans architecture.md (ligne 244-248) :**

```markdown
### Contraintes structurelles
- **Nombre de scènes** : 5
- **Longueur totale** : ~300 mots (tous textes narratifs combinés)
- **Longueur par scène** : 50-70 mots de prose (moyenne 60 mots)
- **Arc narratif** : Ancrage → Exploration → Exploration profonde → Retour → Ancrage final
- **Format de sortie** : JSON structuré (voir format ci-dessous)
```

**Justification :** Aligner sur le prompt original (input.md) qui est la source de vérité

#### 1.2 Corriger la progression narrative dans architecture.md

**Changement dans architecture.md (ligne 262-266) :**

Ajouter les 5 étapes explicitement (actuellement implicites) :

```markdown
### 3. Progression narrative

**Scène 1 - Ancrage** (15%)
[Contenu existant]

**Scène 2 - Exploration** (20%)
[Contenu existant]
- ✅ **IMPORTANT** : Établir clairement l'axe/chemin d'exploration pour la suite

**Scène 3 - Exploration profonde** (30%)
[Contenu existant]
- ✅ **IMPORTANT** : Point culminant du récit (moment fort)

**Scène 4 - Retour** (25%)
[Contenu existant]
- ✅ **IMPORTANT** : Retour OBLIGATOIRE par les mêmes lieux que l'aller (symétrie)

**Scène 5 - Ancrage final** (10%)
[Contenu existant]
```

### Priorité 2 : IMPORTANTE (Enrichissements)

#### 2.1 Ajouter "Connexions" comme responsabilité

**Changement dans architecture.md (ligne 144-151) :**

```markdown
#### Responsabilités ✅
- ✅ Concevoir un **arc narratif** simple et clair
- ✅ Créer des **transitions fluides** entre scènes
- ✅ Utiliser un **vocabulaire sensoriel** simple (pas de termes techniques)
- ✅ Assurer la **cohérence spatiale** (une progression logique des lieux)
- ✅ Maintenir une **atmosphère apaisante** (contexte relaxant)
- ✅ Respecter le thème et le lieu fournis
- ✅ Fournir des **connexions cohérentes** (lieu/thème/exploration/retour/son)
```

#### 2.2 Ajouter critères sensoriels mesurables

**Changement dans architecture.md (ligne 274-277) :**

```markdown
### 5. **Éléments sensoriels riches**

Pour chaque scène, inclure :
- **Au MINIMUM 3 sens** par scène (vue, ouïe, toucher prioritaires)
- Détails concrets et visualisables
- Descriptions qui évoquent des sensations physiques
- Éviter les abstractions et concepts vagues qui rendent la visualisation difficile
```

#### 2.3 Ajouter section "Techniques avancées recommandées"

**Nouveau contenu à ajouter dans architecture.md après ligne 312 :**

```markdown
### Techniques avancées recommandées

Les benchmarks ont identifié plusieurs techniques très efficaces pour améliorer la qualité narrative :

#### 1. Guides narratifs
Utiliser des personnages, objets ou éléments pour fluidifier les transitions :
- **Personnages** : Créatures thématiques qui guident (ex: Pokémon)
- **Éléments naturels** : Sentier, lumière, son, vent
- **Objets** : Carte, Poké Ball, livre

**Avantages :**
- Transitions plus naturelles et fluides
- Cohérence thématique renforcée
- Dimension émotionnelle ajoutée

#### 2. Objet de connexion
Introduire un objet tangible reliant le lieu de méditation au thème :
- Brille/s'active au début (scène 1)
- Disparaît/s'éteint à la fin (scène 5)
- Crée un bouclage narratif satisfaisant

**Exemples :**
- Poké Ball ancienne sur l'appui de fenêtre
- Carte mystérieuse avec symbole thématique
- Livre illustré du thème

#### 3. Axe d'exploration clair
Établir dès la scène 2 un élément spatial constant :
- Sentier, forêt, chemin, rivière
- Même axe pour aller ET retour
- Facilite la compréhension spatiale

**Avantages :**
- Évite les confusions spatiales
- Structure claire et rassurante
- Symétrie narrative naturelle
```

### Priorité 3 : SOUHAITABLE (Améliorations)

#### 3.1 Ajouter renvoi au guide d'évaluation

**Changement dans architecture.md (fin du document) :**

```markdown
---

## Ressources d'Évaluation

Pour l'évaluation qualitative des sorties Storyteller, consulter :
- [`analyse/guide_evaluation_storyteller.md`](../analyse/guide_evaluation_storyteller.md) : Méthodologie complète d'évaluation
- [`analyse/benchmark_storyteller_qualite_narrative.md`](../analyse/benchmark_storyteller_qualite_narrative.md) : Exemple d'analyse comparative

Ces documents fournissent :
- Grille de notation standardisée (50 points)
- Critères détaillés avec barèmes
- Méthodologie reproductible
- Exemples concrets de benchmarks réels
```

#### 3.2 Ajouter section "Validation et Contrôle Qualité"

**Nouveau contenu à ajouter dans architecture.md :**

```markdown
### Validation et Contrôle Qualité

#### Validation technique
- ✅ Format JSON valide
- ✅ Tous les champs obligatoires présents
- ✅ 5 scènes exactement
- ✅ Longueur totale 270-330 mots
- ✅ Longueur par scène 20-80 mots

#### Validation qualité narrative
- ✅ Cohérence spatiale : Retour symétrique obligatoire
- ✅ Aucun élément de danger ou tension
- ✅ Vocabulaire simple et sensoriel
- ✅ Au minimum 3 sens par scène
- ✅ Transitions fluides (2-3 phrases minimum)

#### Seuils de qualité minimale
Pour être utilisable en production :
- Note globale ≥ 40/50 (voir guide d'évaluation)
- Cohérence spatiale ≥ 8/10
- Aucun problème critique (retour non symétrique, danger, etc.)
```

---

## Plan d'Action de Synchronisation

### Étape 1 : Mise à jour architecture.md

**Fichier à modifier :** `architecture.md`

**Changements :**
1. Ligne 244-248 : Aligner nombre de scènes (5) et longueur (300 mots)
2. Ligne 262-266 : Ajouter détails sur les 5 étapes
3. Ligne 144-151 : Ajouter "Connexions" comme responsabilité
4. Ligne 274-277 : Ajouter "Au minimum 3 sens par scène"
5. Après ligne 312 : Ajouter section "Techniques avancées"
6. Fin du document : Ajouter section "Ressources d'Évaluation"
7. Fin du document : Ajouter section "Validation et Contrôle Qualité"

**Temps estimé :** 30-45 min

### Étape 2 : Vérification croisée

**Vérifier que :**
- [ ] Tous les critères du guide sont couverts par architecture.md
- [ ] Aucune contradiction entre les deux documents
- [ ] Les exemples sont cohérents
- [ ] Les références croisées fonctionnent

**Temps estimé :** 15-20 min

### Étape 3 : Mise à jour du guide (optionnel)

**Fichier à modifier :** `guide_evaluation_storyteller.md`

**Changements :**
1. Ajouter renvois vers architecture.md pour chaque critère
2. Ajouter section "Alignement avec architecture.md"
3. Mettre à jour les références de lignes si architecture.md change

**Temps estimé :** 20-30 min

---

## Conclusion

### Synthèse des Divergences

**Divergences critiques :**
1. ❌ Nombre de scènes : 3-4 (architecture) vs 5 (guide)
2. ❌ Longueur totale : 200 mots (architecture) vs 300 mots (guide)
3. ❌ Progression : 4 étapes (architecture) vs 5 étapes (guide)

**Divergences mineures :**
1. ⚠️ Critères : 6 responsabilités (architecture) vs 5 critères (guide)
2. ⚠️ Exemples : Génériques (architecture) vs Spécifiques (guide)

**Alignements :**
1. ✅ Vocabulaire sensoriel
2. ✅ Atmosphère apaisante
3. ✅ Ambiance sonore
4. ✅ Progression narrative (structure)

### Recommandation Finale

**SYNCHRONISATION REQUISE** sur les points critiques :

1. **Aligner architecture.md sur le prompt original** (5 scènes, 300 mots)
2. **Ajouter innovations identifiées** dans les benchmarks
3. **Enrichir architecture.md** avec critères mesurables du guide
4. **Créer références croisées** entre les deux documents

**Bénéfices :**
- ✅ Cohérence complète entre architecture et évaluation
- ✅ Clarté sur les attentes du Storyteller
- ✅ Facilite l'amélioration continue des prompts
- ✅ Assure la qualité des futures générations

**Temps total de synchronisation :** 1-2 heures

---

**Fin de la Vérification de Cohérence**
</content>
<line_count>1000</line_count>
