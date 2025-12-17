# EVA - Guide de Navigation Complet
## Index de tous les documents du projet

---

## 📚 STRUCTURE DU PROJET

### 🎬 SCÉNARIO ET HISTOIRE

| Fichier | Description | Pages | Utilisation |
|---------|-------------|-------|-------------|
| `README.md` | Vue d'ensemble du projet | 1 | Introduction générale |
| `screenplay/script.md` | Scénario complet (19 scènes, 5 actes) | 15 | Script dialogue et action |
| `screenplay/synopsis.md` | Synopsis étendu | 2 | Pitch et résumé |
| `screenplay/treatment.md` | Traitement détaillé par acte | 8 | Structure narrative |
| `SUMMARY.md` | Table des matières GitBook | 1 | Navigation |

---

### 🎭 PERSONNAGES

| Fichier | Description | Contenu |
|---------|-------------|---------|
| `characters/anabelle.md` | Profil Anabelle (mère) | Arc narratif, psychologie, relations |
| `characters/eva.md` | Profil Eva (fille, 8 ans) | Symbolisme, rôle narratif |
| `characters/secondary.md` | Personnages secondaires | Shawn, Beaulieu, Dubois, etc. |
| `production/ai-character-prompts.md` | **Prompts IA pour générer personnages** | Descriptions physiques complètes, expressions, costumes |

---

### 🤖 GÉNÉRATION IA VIDÉO

| Fichier | Description | Scènes Couvertes | Caractères |
|---------|-------------|------------------|-----------|
| `production/ai-video-prompts-detailed.md` | **Prompts ultra-détaillés Acte I** | Scènes 1-5 | 35k |
| `production/ai-prompts-acts-2-5.md` | **Prompts ultra-détaillés Actes II-V** | Scènes 6-19 | 32k |
| `production/video-prompts.md` | Prompts basiques (référence) | Scènes 1-4 | 15k |

**COMMENT UTILISER :**
1. Copier prompt de la scène désirée
2. Coller dans Sora / Runway / Pika
3. Ajuster paramètres techniques (durée, ratio, etc.)
4. Générer plusieurs variantes
5. Sélectionner meilleure version

---

### 🎵 GÉNÉRATION IA AUDIO

| Fichier | Description | Contenu |
|---------|-------------|---------|
| `production/ai-audio-prompts.md` | **Musique, SFX, Design Sonore** | 10 compositions musicales, 67 SFX, voix-off |
| `production/voiceover-script.md` | Script voix-off français/québécois | 15 lignes narration, prononciation |

**COMMENT UTILISER :**
1. **Musique** : Prompts pour Suno AI / Udio
2. **Voix-Off** : Utiliser ElevenLabs avec accent québécois
3. **SFX** : Télécharger/générer selon liste

---

### 🎬 PRODUCTION

| Fichier | Description | Usage |
|---------|-------------|-------|
| `production/shot-list.md` | Liste plans détaillée Scène 1 | 46 plans avec specs caméra |
| `production/locations.md` | Guide repérage lieux | Références visuelles pour IA |
| `production/notes.md` | Notes de production générales | Direction artistique |
| `PRODUCTION_GUIDE.md` | Guide production traditionnel | Référence workflow |

---

### 🔧 ASSEMBLAGE ET POST-PRODUCTION

| Fichier | Description | Usage Primaire |
|---------|-------------|----------------|
| `production/ai-assembly-guide.md` | **GUIDE ASSEMBLAGE COMPLET** | Combiner tous les clips IA |

**CONTENU :**
- Organisation fichiers
- Timeline DaVinci Resolve
- Color grading par acte
- Mix audio
- Export final

**FLOW :**
```
Génération IA → Organisation → Import DaVinci → Edit → Color → Sound → Export
```

---

## 🚀 WORKFLOW RECOMMANDÉ

### ÉTAPE 1 : Génération Vidéo (4-6 semaines)

**Priorité de génération :**

1. **Personnages d'abord** → `ai-character-prompts.md`
   - Générer character sheets (Anabelle, Eva, Shawn, Chat)
   - 6 angles par personnage principal

2. **Scènes critiques** → `ai-video-prompts-detailed.md` + `ai-prompts-acts-2-5.md`
   - Scène 4 : Le Tunnel (disparition)
   - Scène 13 : Découverte du corps
   - Scène 1 : Opening Montréal

3. **Scènes dialogue** → `screenplay/script.md`
   - Utiliser prompts personnages comme base
   - Ajouter dialogue du script

4. **Scènes transition** → Prompts simples
   - Plans d'établissement
   - Paysages, maison, village

**Outils :**
- Sora (OpenAI) - Meilleur réalisme
- Runway Gen-3 - Contrôle précis
- Pika Labs - Plans courts

---

### ÉTAPE 2 : Génération Audio (2-3 semaines)

**Ordre :**

1. **Musique** → `ai-audio-prompts.md` section Musique
   - Générer 10 compositions (Suno AI)
   - Variations et stems

2. **Voix-Off** → `voiceover-script.md` + `ai-audio-prompts.md`
   - ElevenLabs avec voix québécoise
   - 15 lignes narration

3. **SFX** → `ai-audio-prompts.md` section SFX
   - Télécharger bibliothèque (Freesound, etc.)
   - Générer sons spécifiques (chat, tunnel, etc.)

**Outils :**
- Suno AI / Udio - Musique
- ElevenLabs - Voix
- Freesound.org - SFX

---

### ÉTAPE 3 : Assemblage (8-10 semaines)

**Suivre** → `ai-assembly-guide.md`

**Phases :**
1. Organisation fichiers (3 jours)
2. Import DaVinci Resolve (1 jour)
3. Rough Cut (1 semaine)
4. Fine Cut (2 semaines)
5. Color Grading (1 semaine)
6. Sound Design (2 semaines)
7. Audio Mix (1 semaine)
8. Export Final (2 jours)

**Logiciel :**
- DaVinci Resolve 18 (Gratuit)

---

## 📊 STATISTIQUES DU PROJET

### Documents Créés
- **Total fichiers** : 18 fichiers markdown
- **Total caractères** : ~200,000 caractères
- **Pages équivalentes** : ~80 pages

### Prompts IA
- **Vidéo** : 45+ prompts ultra-détaillés
- **Audio** : 10 compositions + 67 SFX + 15 voix-off
- **Personnages** : 8 personnages complets
- **Total mots** : ~50,000 mots de prompts

### Durée Film
- **Cible** : 60 minutes exactement
- **Scènes** : 19 scènes principales
- **Plans** : ~150-200 plans estimés
- **Clips IA** : ~200-250 clips à générer

---

## 🎯 FICHIERS ESSENTIELS (Top 5)

Si vous ne lisez que 5 fichiers :

1. **`production/ai-video-prompts-detailed.md`** - Prompts Acte I
2. **`production/ai-prompts-acts-2-5.md`** - Prompts Actes II-V
3. **`production/ai-assembly-guide.md`** - Comment tout combiner
4. **`production/ai-character-prompts.md`** - Personnages consistants
5. **`screenplay/script.md`** - Le scénario complet

---

## ⚡ QUICKSTART

**Pour commencer maintenant :**

1. **Lire** : `README.md` (vue d'ensemble)
2. **Regarder** : `screenplay/script.md` (comprendre l'histoire)
3. **Générer** : Commencer par Scène 1 Plan 1 (vue aérienne Montréal)
   - Prompt dans `ai-video-prompts-detailed.md`
   - Utiliser Sora ou Runway
4. **Tester** : Un personnage (Anabelle)
   - Prompt dans `ai-character-prompts.md`
5. **Organiser** : Créer structure dossiers
   - Voir `ai-assembly-guide.md` Phase 2

**Durée test** : 1-2 jours pour valider le workflow

---

## 🆘 AIDE ET SUPPORT

### Questions Fréquentes

**Q : Par où commencer?**
A : Lire `README.md`, puis générer Scène 1 Plan 1 comme test

**Q : Quel outil IA utiliser?**
A : Sora (meilleur) ou Runway Gen-3 (alternative)

**Q : Combien de temps total?**
A : 3-4 mois (génération + assemblage)

**Q : Quel budget?**
A : Variable selon crédits IA (estimé 500-2000$ crédits total)

**Q : Besoin de compétences techniques?**
A : Montage vidéo basique + patience

---

## 📞 RESSOURCES

### Communautés
- r/StableDiffusion (génération IA)
- r/runwayml (Runway Gen-3)
- r/davinciresolve (montage)
- r/filmmakers (général)

### Tutoriels
- "DaVinci Resolve 18 Tutorial" (YouTube)
- "Runway ML Gen-3 Guide" (YouTube)
- "Color Grading for Beginners" (YouTube)

---

## 🔄 MISES À JOUR

### Version 1.0 (Décembre 2024)
- ✅ Scénario complet
- ✅ Prompts vidéo Actes I-V
- ✅ Prompts audio complets
- ✅ Prompts personnages
- ✅ Guide assemblage

### Version 1.1 (À venir)
- [ ] Storyboards visuels
- [ ] Templates DaVinci Resolve
- [ ] Scripts automation
- [ ] Tests résultats IA

---

## 📝 NOTES IMPORTANTES

**Copyright :** Tous les prompts et scripts sont originaux pour ce projet

**Utilisation :** Libre pour ce film, mentionner sources si réutilisation

**Crédits :** Film généré par IA - À mentionner dans générique

**Distribution :** Prévoir droits selon platforme (festivals, streaming, etc.)

---

**Navigation Complète - Projet EVA**  
*Tous les outils pour créer un film de 60 minutes avec IA*

**Contact :** Voir repository GitHub pour questions/issues
