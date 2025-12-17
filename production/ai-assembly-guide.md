# EVA - Guide d'Assemblage IA
## Comment combiner tous les clips vidéo et audio générés par IA

---

## 📋 VUE D'ENSEMBLE

Ce guide explique comment prendre tous les éléments générés par IA (vidéo, audio, voix-off) et les assembler en un film cohérent de 60 minutes.

**Flux de travail** : Génération → Organisation → Assemblage → Post-Production → Export Final

---

## 🎬 PHASE 1 : GÉNÉRATION DES CLIPS

### 1.1 Génération Vidéo (Sora/Runway/Pika)

**Ordre de génération recommandé :**

#### PRIORITÉ 1 : Scènes Critiques (Générer en premier)
```
✅ Scène 4 - Le Tunnel (Disparition d'Eva)
   - Plan 4.1 : POV tempête (15s)
   - Plan 4.2 : Arrivée au tunnel (25s)
   - Plan 4.3 : Dans le tunnel (30s)
   - Plan 4.4 : Chasse-neige (15s)
   - Plan 4.5 : Lit vide (12s)
   Total : 97 secondes / 5 clips

✅ Scène 13 - Découverte du corps
   - Plan 13.1 : Printemps (10s)
   - Plan 13.2 : Approche (15s)
   - Plan 13.3 : La découverte (8s)
   Total : 33 secondes / 3 clips

✅ Scène 1 - Montréal Opening
   - Plans 1-46 (voir shot-list.md)
   Total : ~12 minutes / 46 clips
```

#### PRIORITÉ 2 : Personnages (Générer character sheets)
```
✅ Anabelle - 6 angles (front, profile, 3/4, etc.)
✅ Eva - 6 angles
✅ Shawn - 4 angles
✅ Chat noir - 8 variations (différents éclairages)
✅ Personnages secondaires - 2-3 angles chacun
```

#### PRIORITÉ 3 : Scènes Moyennes/Faciles
```
✅ Dialogues intérieurs (moins de mouvement)
✅ Plans d'établissement (paysages, maison)
✅ Plans de transition
```

**OUTIL DE TRACKING :**

Créer un spreadsheet (Google Sheets/Excel) :

| # Scène | # Plan | Description | Durée | Prompt | Status | Fichier Output | Notes |
|---------|--------|-------------|-------|--------|--------|----------------|-------|
| 1 | 1 | Vue aérienne MTL | 15s | prompt-001.txt | ✅ Généré | scene01_plan01_v3.mp4 | Version 3 OK |
| 1 | 2 | Fenêtre appart | 3s | prompt-002.txt | ⏳ En cours | - | - |
| 4 | 3 | Dans tunnel POV | 30s | prompt-004-3.txt | ❌ À faire | - | - |

---

### 1.2 Génération Audio

**Musique (Suno/Udio)**
```
□ Track 01 - Thème principal EVA (3min)
□ Track 02 - Thème Chat Noir (2min)
□ Track 03-10 - Thèmes par acte (voir ai-audio-prompts.md)
□ Variations et stems séparés
```

**Voix-Off (ElevenLabs)**
```
□ V01 - "Avant je voyageais..." (8s)
□ V02 - "Peut-être qu'en quittant..." (5s)
□ V03-15 - Autres voix-off (voir production/voiceover-script.md)
□ Générer 3 variations par ligne (sélectionner meilleure)
```

**SFX (Freesound/Custom)**
```
□ Télécharger/générer 67 effets sonores (voir liste ai-audio-prompts.md)
□ Organiser par catégorie (environnement, objets, corps, etc.)
□ Enregistrements custom si nécessaire (chat réel, tunnel réel, etc.)
```

---

## 📁 PHASE 2 : ORGANISATION DES FICHIERS

### 2.1 Structure de Dossiers

```
EVA-FILM/
│
├── 01-VIDEO-RAW/           # Tous les clips vidéo générés par IA
│   ├── ACTE-01/
│   │   ├── scene01/
│   │   │   ├── plan001_v1.mp4
│   │   │   ├── plan001_v2.mp4
│   │   │   └── plan001_FINAL.mp4  ← Version sélectionnée
│   │   ├── scene02/
│   │   └── ...
│   ├── ACTE-02/
│   ├── ACTE-03/
│   ├── ACTE-04/
│   └── ACTE-05/
│
├── 02-AUDIO-RAW/
│   ├── MUSIC/
│   │   ├── track01_theme-eva.wav
│   │   ├── track02_theme-chat.wav
│   │   └── ...
│   ├── VOICEOVER/
│   │   ├── V01_avant-je-voyageais.wav
│   │   └── ...
│   ├── SFX/
│   │   ├── ENV/              # Environnement
│   │   ├── OBJ/              # Objets
│   │   ├── BODY/             # Sons corporels
│   │   └── SPECIAL/          # Tunnel, chat, etc.
│   └── AMBIANCE/
│
├── 03-ASSETS/
│   ├── GRAPHICS/             # Titres, crédits
│   ├── SUBTITLES/            # .srt files
│   └── REFERENCES/           # Images de référence
│
├── 04-PROJECT/               # Fichiers de projet DaVinci/Premiere
│   └── EVA_MASTER.drp
│
├── 05-EXPORT/                # Rendus finaux
│   ├── EVA_60min_MASTER.mov
│   ├── EVA_60min_STREAMING.mp4
│   └── EVA_60min_DCP/
│
└── DOCS/
    ├── timeline-notes.txt
    ├── color-grading-notes.txt
    └── mix-notes.txt
```

### 2.2 Nomenclature des Fichiers

**Vidéo :**
```
Format : S[scène]_P[plan]_[description]_v[version].mp4
Exemple : S04_P03_tunnel-POV_v2.mp4
         S13_P03_decouverte_FINAL.mp4
```

**Audio :**
```
Format : [type]_[numéro]_[description].wav
Exemple : MUS_01_theme-eva.wav
         VO_03_quitter-montreal.wav
         SFX_23_snowplow-pass.wav
```

---

## 🎞️ PHASE 3 : ASSEMBLAGE VIDÉO

### 3.1 Logiciel Recommandé

**Option 1 : DaVinci Resolve (Gratuit/Pro)**
- ✅ Gratuit (version complète)
- ✅ Montage + Color + Audio intégrés
- ✅ Timeline magnétique
- ✅ Export professionnel

**Option 2 : Adobe Premiere Pro**
- ✅ Industrie standard
- ❌ Abonnement payant
- ✅ Intégration After Effects

**Option 3 : Final Cut Pro (Mac)**
- ✅ Magnetic timeline
- ❌ Mac seulement
- ✅ Optimisé M1/M2

**RECOMMANDATION : DaVinci Resolve** (gratuit + puissant)

---

### 3.2 Configuration Projet DaVinci Resolve

**Nouveau Projet :**
```
Nom : EVA_60min
Timeline Resolution : 3840x1644 (2.35:1 custom)
   ou 4096x1716 (DCI 2.39:1)
Frame Rate : 24 fps
Color Space : Rec.709 (ou DCI-P3 si capacité)
Audio : 48kHz, 24-bit
```

**Custom Timeline Resolution (2.35:1) :**
1. File > Project Settings > Timeline Resolution
2. Custom : Width 3840, Height 1634
3. Appliquer à tous les nouveaux timelines

---

### 3.3 Import et Organisation

**Bins (Dossiers dans DaVinci) :**
```
Media Pool:
├── 01_RAW_VIDEO_ACTE1
├── 02_RAW_VIDEO_ACTE2
├── 03_RAW_VIDEO_ACTE3
├── 04_RAW_VIDEO_ACTE4
├── 05_RAW_VIDEO_ACTE5
├── AUDIO_MUSIC
├── AUDIO_VO
├── AUDIO_SFX
├── GRAPHICS
└── SELECTS (clips finaux sélectionnés)
```

**Import :**
1. File > Import Media
2. Sélectionner tous les dossiers vidéo
3. Importer audio séparément
4. Créer bin "SELECTS" pour versions finales

---

### 3.4 Assemblage Timeline - Workflow Étape par Étape

#### ÉTAPE 1 : Rough Cut (Premier Montage)

**Créer Timeline Master :**
```
Nom : EVA_MASTER_EDIT
Durée cible : 60 minutes
```

**Placer les clips dans l'ordre du scénario :**

```
TIMELINE (simplifié) :

V1 [Vidéo principale]
V2 [Transitions/Overlays]
---
A1 [Dialogue/VO L]
A2 [Dialogue/VO R]
A3 [Music Stéréo L]
A4 [Music Stéréo R]
A5 [SFX/Ambiance L]
A6 [SFX/Ambiance R]
```

**Méthode :**
1. **Acte I** : Placer Scene 1 Plan 1, 2, 3... dans l'ordre
2. Ajouter markers (M) pour début de chaque scène
3. Pas de timing précis encore, juste ordre
4. Laisser gaps (espaces) entre scènes si besoin

**Durée attendue Rough Cut :** 70-75 minutes (sera coupé à 60)

---

#### ÉTAPE 2 : Fine Cut (Montage Fin)

**Ajustements timing :**
- Couper débuts/fins de clips (enlever artefacts IA)
- Ajuster durée de chaque plan selon rythme désiré
- Créer rythme : Acte I lent, Acte II accélère, Acte III chaotique, etc.

**Transitions :**
- Majoritairement : **Cut** (coupe nette)
- Occasionnellement : **Fondu au noir** (2 secondes) entre actes
- Rare : **Fondu enchaîné** (0.5s) pour flashbacks/hallucinations
- **Pas d'effets fancy** (pas de wipes, stars, etc. - réalisme)

**Raccords :**
- Match on action (si possible)
- Continuité visuelle (direction du regard, mouvement)
- Utiliser raccords audio pour lisser transitions vidéo

**Durée cible Fine Cut :** 62-63 minutes (buffer)

---

#### ÉTAPE 3 : Intégration Audio Dialogue/VO

**Synchronisation Voix-Off :**
```
1. Placer clip VO sur piste A1/A2
2. Aligner avec vidéo correspondante
3. Ajuster timing exact (commence où?)
4. Fade in/out (0.2s crossfade)
5. Vérifier intelligibilité
```

**Exemple : Voix-Off Scène 1**
```
Timeline Position : 00:00:10:00 (10 secondes après début)
Clip : V01_avant-je-voyageais.wav
Durée : 8 secondes
Volume : -12dB (en dessous musique)
Fade : In 0.5s, Out 0.5s
```

---

#### ÉTAPE 4 : Sound Design Préliminaire

**Layer 1 : Ambiances (Tracks A5-A6)**
- Ambiance constante sous chaque scène (vent, intérieur maison, etc.)
- Volume bas (-25dB)
- Fondu entre scènes (3 secondes overlap)

**Layer 2 : SFX Spécifiques (Tracks A7-A8)**
- Sons d'objets, actions, etc.
- Placés exactement sur action visuelle
- Ajustement frame par frame si nécessaire

**Layer 3 : Musique (Tracks A3-A4)**
- Placer thèmes musicaux
- Volume variable selon scène
- Silence total dans certaines scènes (respecter intention)

**Astuce :** Utiliser couleurs pour différencier types audio
- Rouge : VO
- Bleu : Musique
- Vert : SFX
- Jaune : Ambiance

---

## 🎨 PHASE 4 : POST-PRODUCTION VIDÉO

### 4.1 Color Grading (DaVinci Color Page)

**Philosophie Couleur EVA :**
- Désaturation générale (ton mélancolique)
- Tons froids dominants (bleus, gris)
- Progression : Acte I moins désaturé → Acte V presque noir&blanc

**LUT de Base (Point de départ) :**
```
LUT : None (partir de Rec.709)
ou télécharger : "Bleach Bypass" LUT (look désaturé)
```

**Corrections par Acte :**

**ACTE I - Montréal**
```
Lift (Ombres) : Légèrement bleuté
Gamma (Tons moyens) : Désaturation -20%
Gain (Hautes lumières) : Légèrement doré (sunset)
Saturation Globale : -15%
Température : Refroidir -10 Kelvin
Contraste : +5 (pas excessif)
```

**ACTE II-III - Village/Descente**
```
Lift : Bleu plus prononcé
Gamma : Désaturation -40%
Saturation Globale : -30%
Température : -20 Kelvin (très froid)
Contraste : +10
Vignette : Subtile (assombrir bords)
```

**ACTE IV-V - Post-Découverte**
```
Lift : Crusher les noirs (noir profond)
Gamma : Désaturation -60%
Saturation Globale : -50% (presque monochrome)
Température : -30 Kelvin
Contraste : +15
Grain : Ajouter grain film (subtil)
```

**Scènes Spécifiques :**

**Tunnel (Scène 4) :**
```
Primaries : Extrême désaturation (-80%)
Exposition : Underexpose -0.5 stops
Courbes : Crush blacks, préserver détails ombres
Grain : Grain fort (effet ISO élevé)
```

**Hallucinations (Scène 10) :**
```
Distorsion chromatique : Ajouter via FX
Shift teintes : Vert/Magenta léger
Flou : Gaussian Blur à 5% (dreamlike)
```

**Chat Noir (Toutes scènes) :**
```
Power Window : Isoler le chat
Yeux : Augmenter luminosité/saturation (glow effect)
Pelage : S'assurer noir profond mais détails visibles
```

**ASTUCE :** Créer "Still" (snapshot) pour chaque look, appliquer aux scènes similaires

---

### 4.2 VFX et Corrections

**Corrections nécessaires (IA génère parfois erreurs) :**

**Problèmes communs clips IA :**
1. **Morphing/warping** : Recadrer pour cacher
2. **Mains bizarres** : Recadrer ou flouter léger
3. **Inconsistances arrière-plan** : Masking et remplacement
4. **Artefacts** : Stabilisation, noise reduction

**Outils DaVinci (Fusion Page) :**
- Planar Tracker : Suivre objet, masquer
- Roto Brush : Isoler personnage
- Clean Plate : Remplacer arrière-plan
- Denoise : Réduire artefacts

**VFX Spécifiques :**

**Yeux du Chat (glow) :**
```
1. Fusion > Add Glow node
2. Masquer yeux du chat (ellipse mask x2)
3. Glow Gain : 1.5
4. Glow Size : 10
5. Color : Vert-jaune (#CCFF00)
6. Blend : Screen
```

**Flashbacks/Hallucinations (effet dreamlike) :**
```
1. Duplicate clip sur V2
2. Gaussian Blur : 15
3. Blend Mode : Soft Light
4. Opacity : 30%
5. Color Shift : +5 Magenta
```

---

## 🔊 PHASE 5 : POST-PRODUCTION AUDIO

### 5.1 Mix Audio (DaVinci Fairlight Page)

**Bus Structure :**
```
Master Out
├── Dialogue Bus (A1-A2)
├── Music Bus (A3-A4)
├── SFX Bus (A5-A8)
└── Ambiance Bus (A9-A10)
```

**Niveaux Cibles (LUFS) :**
- Dialogue/VO : -16 LUFS (le plus fort)
- Musique : -20 to -24 LUFS (sous dialogue)
- SFX : -18 LUFS (présent mais pas écrasant)
- Ambiance : -28 LUFS (sous tout)

**EQ par Bus :**

**Dialogue Bus :**
```
HPF : 80Hz (enlever rumble)
Boost : 2-3kHz (+3dB) (intelligibilité)
De-esser : 6-8kHz (réduire sibilance)
Compressor : Ratio 3:1, Threshold -18dB
```

**Music Bus :**
```
HPF : 40Hz
LPF : 15kHz (laisser place dialogue hautes fréq.)
Compressor : Ratio 2:1, Threshold -16dB (subtil)
```

**SFX Bus :**
```
EQ selon contexte
Pas de compression générale (préserver dynamics)
```

---

### 5.2 Sound Design Avancé

**Scène Critique : LE TUNNEL (Scène 4)**

**Timeline Audio Détaillée (30 secondes) :**

```
TEMPS  | A1-A2 [VO/Dialog] | A3-A4 [Music] | A5-A6 [ENV] | A7-A8 [SFX] | A9-A10 [Design]
-------|-------------------|---------------|-------------|-------------|------------------
0:00   | Breathing (child) | Drone 40Hz    | Wind storm  | Footsteps   | Heartbeat (60bpm)
0:05   | "Petit chat..."   | String swell  | Wind +snow  | Coat drag   | Tinnitus (fade in)
0:10   | Breathing faster  | Crescendo     | Wind heavy  | Water drip  | Heartbeat (70bpm)
0:15   | Whimper          | Peak         | Wind muted  | Scraping    | Heartbeat (80bpm)
0:20   | [Tunnel reverb]   | Sustained     | Echo space  | Rumble far  | Heartbeat louder
0:25   | "Maman!"         | Cut to low    | Compression | Plow close  | Heart (90bpm)
0:30   | [Scream cut]     | SILENCE       | Muffled     | Crush snow  | Heart slow/stop
```

**Automation (Keyframes) :**
- Volume : Créer courbe d'intensité
- Pan : Chat moving L→R
- Reverb : Dry (extérieur) → Wet 100% (tunnel)
- Filter : LPF automation (neige recouvre = sons étouffés)

---

### 5.3 Moments de Silence

**CRUCIAL : Respecter les silences du design sonore**

**Scènes avec silence total (0.0 dB) :**
1. **Scène 13.3** (Découverte corps) : 2 secondes silence après cri
2. **Scène 17** (Accouchement) : Silence quand bébé purrs
3. **Transitions entre actes** : 1 seconde silence noir

**Technique :**
```
Créer clip de "Room Tone" (silence pas totalement mort)
Volume : -infinity dB → Silence parfait
Ou utiliser vrai silence (aucun clip)
```

---

## 🎬 PHASE 6 : MASTERING ET EXPORT

### 6.1 Mastering Audio Final

**Sur Master Bus :**
```
1. EQ : Légère courbe (enlever mud 200-400Hz)
2. Multiband Compressor : Contrôle graves, médiums, aigus
3. Limiter : Ceiling -1dBTP (true peak)
4. Loudness Meter : Viser -23 LUFS intégré (standard)
```

**Vérifications :**
- ✅ Pas de clipping (red lights)
- ✅ Dialogue toujours intelligible
- ✅ Pas de sauts de volume entre scènes
- ✅ Test sur multiples systèmes (laptop, phone, TV, theatre)

---

### 6.2 Export Final

**MASTER FILE (Archive Qualité Max) :**
```
Format : QuickTime (MOV)
Codec : ProRes 422 HQ
Résolution : 3840x1634 (2.35:1) ou 4096x1716 (DCI)
Frame Rate : 24 fps
Scan : Progressive
Audio : PCM 24-bit, 48kHz, Stéréo
Color Space : Rec.709 (ou P3)
Taille fichier : ~40-60 GB
```

**STREAMING (Netflix/Amazon/YouTube) :**
```
Format : MP4
Codec : H.264 (ou H.265 si dispo)
Résolution : 3840x1634 (2.35:1)
Frame Rate : 24 fps
Bitrate : 15-25 Mbps (VBR)
Audio : AAC 320 kbps, 48kHz, Stéréo
Color : Rec.709
Taille fichier : ~3-5 GB
```

**DCP (Cinéma Numérique) :**
```
Logiciel : DCP-o-matic (gratuit) ou Clipster (pro)
Format : DCI 2K ou 4K
Frame Rate : 24 fps
Color : XYZ
Audio : 5.1 ou 7.1 (si mixé)
Encryption : Selon diffuseur
```

**SOUS-TITRES :**
```
Format : .srt (SubRip)
Langue : Français + Anglais
Timecode : Exact avec dialogue
Export : Fichier séparé + burned-in version
```

---

## ✅ CHECKLIST FINALE

### AVANT EXPORT :
- [ ] Tous les clips en place (aucun gap)
- [ ] Durée totale : 60 minutes ±30 secondes
- [ ] Audio sync parfait (pas de décalage)
- [ ] Color grading appliqué à tout
- [ ] Corrections VFX terminées
- [ ] Mix audio équilibré
- [ ] Loudness à -23 LUFS
- [ ] Pas de clipping audio/vidéo
- [ ] Crédits début/fin ajoutés
- [ ] Logo production si nécessaire

### TEST VIEWING :
- [ ] Regarder film complet sans interruption
- [ ] Vérifier continuité visuelle
- [ ] Vérifier continuité audio
- [ ] Tester sur différents écrans
- [ ] Tester avec/sans sous-titres
- [ ] Demander feedback à viewers beta

### EXPORTS :
- [ ] Master ProRes (archive)
- [ ] MP4 Streaming (distribution)
- [ ] DCP (si projection cinéma)
- [ ] Sous-titres (.srt)
- [ ] Affiche/poster (marketing)
- [ ] Teaser 60s (promotion)

---

## 🚀 OPTIMISATIONS ET ASTUCES

### Performance DaVinci Resolve

**Si lag/ralentissement :**
```
1. Générer Optimized Media (Proxy à 1/2 résolution)
2. Playback > Timeline Proxy Mode > Half Resolution
3. Désactiver effets temps réel pendant edit
4. Rendre cache audio (pour SFX lourds)
5. Fermer applications inutiles
6. Augmenter RAM cache (Preferences)
```

**Raccourcis Clavier Utiles :**
```
I / O : Mark In / Out
B : Razor Tool (couper)
T : Trim Edit Mode
M : Add Marker
Cmd+D : Duration (changer durée clip)
Cmd+Z : Undo (important!)
Space : Play/Pause
J K L : Rewind / Pause / Forward
```

---

### Workflow Parallèle (Équipe)

Si plusieurs personnes travaillent :

**Diviser par Acte :**
```
Personne A : Acte I + II (Montage)
Personne B : Acte III + IV (Montage)
Personne C : Acte V + Color Grading
Personne D : Audio Mix complet
```

**Utiliser DaVinci Collaboration :**
- Project Server (gratuit jusqu'à 2 users)
- Cloud sync (Google Drive pour assets)
- Lock bins (éviter conflits)

---

## 📊 TIMELINE PRODUCTION ESTIMÉE

**Avec équipe de 2-3 personnes :**

| Phase | Durée | Notes |
|-------|-------|-------|
| Génération IA (tous clips) | 4-6 semaines | Parallèle, iterations |
| Organisation fichiers | 3 jours | Crucial, ne pas rush |
| Rough Cut | 1 semaine | Assemblage basique |
| Fine Cut | 2 semaines | Timing précis, transitions |
| Color Grading | 1 semaine | Plan par plan |
| Sound Design | 2 semaines | Layer par layer |
| Audio Mix | 1 semaine | Balance finale |
| VFX/Corrections | 1 semaine | Selon problèmes IA |
| Review & Adjustments | 1 semaine | Tests, feedback |
| Master & Export | 2-3 jours | Exports multiples |
| **TOTAL** | **~10-12 semaines** | Post-génération IA |

---

## 🎓 RESSOURCES ET FORMATION

### Tutoriels Recommandés :

**DaVinci Resolve :**
- "DaVinci Resolve 18 - Full Tutorial for Beginners" (YouTube)
- Casey Faris channel (gratuit, excellent)
- Blackmagic Design Training (officiel)

**Color Grading :**
- "Cinematic Color Grading in DaVinci Resolve"
- Waqas Qazi channel

**Audio Mix :**
- "Film Sound Design Tutorial"
- "Fairlight Audio Crash Course"

### Communautés :

- **r/davinciresolve** (Reddit)
- **r/filmmaking** (Reddit)
- **Blackmagic Forum** (officiel)
- **Discord servers** pour AI film makers

---

## 📝 NOTES FINALES

**Points Critiques :**

1. **Backup Obsessionnel** : 3-2-1 rule (3 copies, 2 médias, 1 offsite)
2. **Version Control** : Sauvegarder versions projet régulièrement
3. **Patience** : Ne pas rusher, qualité > vitesse
4. **Test Audio** : Headphones ET speakers
5. **Breaks** : Repos yeux/oreilles régulièrement

**Le secret d'un bon assemblage :** **ORGANISATION** dès le début. Temps investi en organisation = gain massif en post.

---

**Guide Assemblage Complet - Prêt pour Production Film EVA**

*Combiner avec tous les autres guides (video-prompts, audio-prompts, character-prompts) pour workflow complet*
