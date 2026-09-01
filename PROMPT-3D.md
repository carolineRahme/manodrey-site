# PROMPT — Manodrey, version « film 3D » professionnel

Prompt à coller tel quel dans Claude Code (ou tout agent de dev) pour reconstruire le site Manodrey en expérience cinématographique 3D temps réel.

---

## MISSION

Reconstruis le site de **Manodrey**, société de production audiovisuelle basée à Paris, sous la forme d'une **expérience 3D temps réel** qui se regarde comme un film. Le scroll ne fait pas défiler une page : il fait avancer un plan-séquence. Chaque section est un plan de cinéma, avec sa focale, sa lumière, son mouvement de caméra.

Référence de niveau : les sites primés Awwwards des studios de production (Dogstudio, Resn, Locomotive), et l'ouverture d'un long-métrage plus qu'une landing page. Zéro effet gratuit : chaque mouvement doit servir la narration.

Le site actuel est un `index.html` statique unique. La nouvelle version doit conserver **exactement le même contenu éditorial et la même charte**, mais changer entièrement de dimension visuelle.

## MARQUE ET CONTENU (à respecter au mot près)

- Nom : **Manodrey** — Société de production audiovisuelle. Cinéma, vidéo, télévision. Paris.
- Signature : **« Là où l'imaginaire prend vie »**
- Production phare 2026 : **La Salle**, série originale, humour et société, qui se déroule dans une salle de sport et raconte les petits faits de société du quotidien.
- Synopsis à afficher : « En France, environ 5 500 salles de sport accueillent chaque jour des milliers d'anonymes venus se dépenser, décompresser ou simplement tuer le temps. Plus de 2 millions de Français y sont abonnés, et 59 % d'entre eux y reviennent plusieurs fois par semaine, par habitude, par ambition ou par besoin de souffler. On y vient pour transpirer, oublier, recommencer, et, sans toujours s'en rendre compte, pour se rencontrer. Entre deux machines, sous la lumière crue des néons, des vies se croisent, se confient, s'accrochent et parfois se transforment pour de bon. » Chute : *voici leurs histoires*.
- Fondateur : **Christian Bahfir**, entrepreneur. Citation : « La discipline du ring m'a appris la patience. Le cinéma m'a appris à la transmettre. » Texte : Manodrey est né d'une double exigence, celle du sport de haut niveau et celle de l'art qui prend son temps. Une maison qui place l'intensité, la précision et la part d'imaginaire au cœur de chaque projet.
- Contact : **« Vous avez une histoire ? On en fera un film. »** — manodrey@orange.fr
- Bandeaux défilants : « Faites-nous rêver ✦ » / « Écrivons la suite ✦ »
- Footer : Productions (La Salle, Showreel), Maison (Fondateur, À propos, Contact), Suivre (Instagram, TikTok, YouTube), © 2026 Manodrey Productions.
- Langue : français, `lang="fr"`.

## DIRECTION ARTISTIQUE

Palette (inchangée) :
```
--night   #01030A   fond, noir bleuté profond
--surface #0B1430   /  --surface-2 #131D3F
--text    #ECEDF3   /  --text-2 #8C95B0  /  --text-3 #4A5275
--gold    #D4AF7A   /  --gold-light #FFE9C4  /  --gold-deep #A6824A
```
Typographies (inchangées, Google Fonts) : DM Serif Display (titres), Cormorant Garamond (textes littéraires), Inter (interface), Allura et Pinyon Script (accents manuscrits), Anton (impact).

Traitement image, non négociable :
- grain argentique 35 mm animé, subtil, sur toute la page ;
- vignettage doux et aberration chromatique très légère sur les bords ;
- flare anamorphique horizontal doré sur les sources lumineuses ;
- profondeur de champ réelle (bokeh) pilotée par la caméra, pas un flou CSS ;
- letterbox cinéma 2.39:1 qui s'ouvre et se referme aux moments clés ;
- aucune couleur hors palette, aucun blanc pur en aplat.

## STACK

- **Three.js** (WebGL2) en module ES, **GSAP + ScrollTrigger** pour la timeline, **Lenis** pour le scroll inertiel.
- Post-processing : EffectComposer avec bloom sélectif, depth of field, film grain, vignette, chromatic aberration. Budget maximum 3 passes actives simultanées.
- Pas de framework lourd imposé : Vite + JS vanilla suffit. Le site doit rester déployable en statique sur Vercel.
- Aucune dépendance CDN externe bloquante : tout bundlé, polices en `display=swap`.

## PLAN DE TOURNAGE (scroll = timeline)

Une seule scène 3D persistante, une seule caméra, sept plans enchaînés par le scroll. Jamais de coupe brutale, sauf si elle est écrite.

**Plan 1 — Ouverture.** Noir total. Le letterbox s'ouvre. Champ d'étoiles volumétrique en particules (reprise du starfield actuel, mais en 3D avec parallaxe réelle sur trois profondeurs). Le mot **MANODREY** se compose lettre par lettre en géométrie 3D dorée, comme un titre de générique, légèrement extrudé, éclairé en rasant. Sous-titre : « Là où l'imaginaire prend vie ✦ » puis « Société de production ✦ Paris ». La vidéo `assets/hero-bg.mp4` existante est utilisée en texture projetée sur un plan courbe en arrière-plan, très désaturée et assombrie.

**Plan 2 — Traversée.** Le scroll fait avancer la caméra à travers le champ d'étoiles. Les lettres du titre se dispersent en particules qui deviennent la poussière du plan suivant. Ralenti progressif.

**Plan 3 — La Salle.** Arrivée sur un espace 3D évoquant une salle de sport nocturne : volumes simples et abstraits (pas de modélisation réaliste), néons lumineux en émissive qui grésillent, faisceaux volumétriques dans la poussière. Titre **La Salle**, tags « Série originale · Humour · Société · 2026 ». Le pitch apparaît dans la lumière d'un néon.

**Plan 4 — Le synopsis.** Travelling latéral lent. Le texte du synopsis défile en calques à des profondeurs différentes, certains mots en avant-plan flous, d'autres nets au fond. Les chiffres (5 500, 2 millions, 59 %) s'incrustent en gros caractères dorés, en léger décalage de parallaxe. Fin du plan sur *voici leurs histoires* en Allura, seul dans le noir.

**Plan 5 — Le fondateur.** Coupe assumée, retour au calme. Portrait de Christian Bahfir traité comme un plan fixe : lumière unique latérale, fond noir, très peu de mouvement de caméra, respiration lente. La citation apparaît en Cormorant italique. Le contraste avec le plan 4 doit être frappant : ici, le site ralentit.

**Plan 6 — Bandeaux.** Les phrases « Faites-nous rêver ✦ » et « Écrivons la suite ✦ » défilent en 3D sur deux rubans opposés qui traversent l'écran en profondeur.

**Plan 7 — Contact.** La caméra recule jusqu'à révéler que toute la scène tenait dans un plan de projection. **« Vous avez une histoire ? On en fera un film. »** L'adresse manodrey@orange.fr est un lien `mailto:` avec un traitement lumineux au survol. Le letterbox se referme, le générique de fin fait office de footer.

## INTERACTIONS

- Curseur personnalisé : petit réticule de visée façon caméra, qui s'élargit sur les zones cliquables et affiche un libellé contextuel.
- Le logo Manodrey en header ramène toujours à l'accueil, plan 1 rejoué en douceur.
- Header transparent au départ, fond flouté et bordure dorée fine après 50 px de scroll.
- Survol des zones interactives : montée du bloom local, jamais de changement de couleur brutal.
- Micro-parallaxe à la souris sur chaque plan, amplitude maximale 15 px, désactivée au tactile.

## PERFORMANCE, EXIGENCE ABSOLUE

- **60 fps constants** sur un MacBook Air M1 en plein écran. C'est le critère d'acceptation principal.
- Une **seule boucle `requestAnimationFrame`** pour tout : Three.js, GSAP, parallaxe, grain. Aucun `setInterval`, aucun listener de scroll qui écrit dans le DOM.
- Uniquement des animations en `transform` et `opacity` côté DOM ; tout le reste vit dans le canvas.
- `pixelRatio` plafonné à 2, résolution du composer réduite à 0,75 sur les passes coûteuses.
- Détection de perte de fluidité : si la moyenne descend sous 45 fps sur 2 secondes, dégrader automatiquement (bloom off, DOF off, densité de particules divisée par deux) sans jamais couper l'expérience.
- Chargement : loader plein écran avec compteur, entrée dans le plan 1 seulement quand la scène est prête. Textures et vidéo en chargement différé.
- Mobile : version allégée, particules divisées par trois, post-processing réduit au grain et au vignettage, mais **la narration en sept plans reste identique**.

## ACCESSIBILITÉ ET SEO

- `prefers-reduced-motion` : servir une version statique élégante, plans figés sur leur plus belle image, contenu intégralement lisible et navigable.
- Tout le texte existe en HTML réel dans le DOM, jamais uniquement en texture 3D. Le canvas est `aria-hidden`.
- Navigation clavier complète, focus visible doré, contraste minimum AA sur tous les textes.
- Conserver et enrichir les métadonnées actuelles : title, description, Open Graph, Twitter Card, theme-color `#01030A`, plus JSON-LD `Organization` et `TVSeries` pour La Salle, sitemap.xml et robots.txt.

## LIVRABLE

- Le site fonctionnel, structure claire, code commenté en français.
- Aucune erreur ni avertissement dans la console.
- Un `README.md` expliquant comment lancer, modifier les textes et remplacer les médias.
- Ne rien inventer comme contenu : si un média manque, laisser un emplacement explicitement marqué à remplacer.
