# PROMPT — Vidéo d'intro Manodrey

Générique d'ouverture de 22 secondes, à passer en hero du site et en intro de tous les contenus Manodrey.
Format principal 16:9 (2.39:1 après letterbox), variante 9:16 pour Instagram et TikTok.

Méthode : 6 plans générés séparément (5 s chacun), montés et raccourcis au montage. Le logotype MANODREY n'est **jamais** généré par le modèle vidéo, il est incrusté en post-production : les modèles écrivent mal le texte.

---

## PROMPT MAÎTRE (contexte à répéter dans chaque plan)

```
Cinematic 35mm film opening title sequence for a French film production company.
Deep blue-black night palette (#01030A), pure gold highlights (#D4AF7A), no other colors.
Anamorphic lens, 2.39:1, shallow depth of field, heavy bokeh, horizontal gold lens flares,
visible 35mm film grain, soft vignette, high contrast chiaroscuro lighting, dust in the air.
Slow deliberate camera movement. Prestige cinema mood, patient, elegant, no dialogue, no text.
```

Négatif commun :
```
text, letters, words, subtitles, watermark, logo, captions, CGI look, cartoon, oversaturated,
teal and orange grading, fast cuts, shaky camera, lens dirt overlay, people looking at camera, deformed hands
```

---

## PLAN 1 — Naissance de la lumière (0 s à 3 s)

```
Total darkness. A single thin beam of warm gold light slowly cuts through the black,
revealing thousands of dust particles drifting in the air. The camera pushes forward
extremely slowly into the beam. Nothing else is visible. Absolute silence and stillness.
[PROMPT MAÎTRE]
```
Caméra : dolly avant très lent, focale 85 mm.

## PLAN 2 — Traversée d'étoiles (3 s à 6 s)

```
The dust particles become stars. Camera flies slowly forward through a dense volumetric
starfield, white and pale gold points of light passing on three depth layers with real parallax.
Deep blue-black space, distant nebula barely visible, no planets.
[PROMPT MAÎTRE]
```
Caméra : travelling avant continu, focale large 24 mm, léger roulis.

## PLAN 3 — La salle, la nuit (6 s à 10 s)

```
Interior of an empty gym at night, seen from far away. Rows of weight machines as dark
geometric silhouettes. One fluorescent neon tube flickers and buzzes overhead, casting a
harsh cold light into thick dusty air with visible volumetric light beams. Nobody in frame.
Slow lateral tracking shot past the machines.
[PROMPT MAÎTRE]
```
Caméra : travelling latéral gauche vers droite, focale 40 mm.

## PLAN 4 — La discipline (10 s à 14 s)

```
Extreme close-up, low key lighting: hands slowly wrapping boxing tape around knuckles,
then a drop of sweat falling in slow motion onto a rubber floor, then chalk dust rising
in a single shaft of light. Anonymous, no face visible. Intimate, patient, almost sacred.
[PROMPT MAÎTRE]
```
Caméra : macro fixe, très léger flottement, focale 100 mm macro.

## PLAN 5 — Les vies qui se croisent (14 s à 18 s)

```
Slow motion, backlit silhouettes of several anonymous people crossing paths in the haze of
a gym, walking in opposite directions, faces hidden by the backlight, gold rim light on their
shoulders. Shallow focus, foreground bodies blurred, one distant silhouette sharp.
[PROMPT MAÎTRE]
```
Caméra : fixe, longue focale 135 mm, compression des plans.

## PLAN 6 — Le logo (18 s à 22 s)

```
All the dust and light particles from the room rise and converge slowly toward the center
of the frame, forming a dense glowing cloud of gold particles suspended in total darkness,
then settling into stillness. Empty centered composition, room left for a title.
[PROMPT MAÎTRE]
```
Caméra : recul lent, focale 50 mm. **Le mot MANODREY et la signature « Là où l'imaginaire prend vie » sont incrustés au montage** en DM Serif Display doré #D4AF7A, apparition lettre par lettre sur 1,2 s, puis fermeture du letterbox en fondu au noir.

---

## SON

- Nappe grave et tenue, montée progressive du plan 1 au plan 5.
- Sons concrets discrets et espacés : le grésillement du néon (plan 3), le bruit sec du tape qui se déroule et une respiration (plan 4).
- Silence total pendant 0,4 s juste avant l'apparition du logo, puis une seule note dorée résonante avec longue réverbération.
- Aucune voix off, aucune musique rythmée.

## RÉGLAGES DE GÉNÉRATION

- Modèle conseillé : Veo 3.1 ou Kling 2.5 en image-to-video, à partir d'images fixes générées d'abord pour figer la direction artistique (cohérence bien meilleure qu'en text-to-video direct).
- 5 s par plan, 24 fps, 16:9, puis recadrage 2.39:1 par letterbox au montage.
- Générer 2 à 3 variantes par plan et ne garder que la plus stable, surtout pour les plans 4 et 5 (mains et visages).
- Étalonnage final commun : désaturation légère, noirs bleutés, hautes lumières poussées vers l'or, grain 35 mm ajouté au montage pour uniformiser.

## VARIANTE 9:16

Mêmes plans, deux ajustements : cadrer les plans 3 et 5 en vertical serré (une seule machine, une seule silhouette), et raccourcir à 15 s en coupant le plan 2 et en réduisant chaque plan à 2,5 s. Le logo reste 3 s pleines.

## MONTAGE

Enchaînements en fondu de 12 images entre tous les plans, sauf entre le plan 5 et le plan 6 : coupe franche sur le silence. Durée finale 22 s.
