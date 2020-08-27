# imageAnnotationGroundTruth

 Amélioration du balisage généré automatiquement par TMG_ImageAnnotation.

## Restructuration du balisage automatique

- Supprimer les balisages inutiles.
- La possibilité de passer d'une région à une autre avec la flèche descendante du clavier permet de repérer de petites régions balisées en dessous d'une grande région. Après l'avoir identifié, on peut la supprimer avec la touche backspace.


## Paragraphe

Chaque paragraphe est identifié par son indentation.

## Portées et caractères musicaux

Toutes les portées sont signalées par la région Staffnotation. La notation par lettres est également signalée par Staffnotation. Les caractères musicaux dans le texte ne représentent pas une région particulière. S'ils se trouvent dans un paragraphe, ils intègrent cette région.
Exemple page 13 de Burmeister 

## Encodade de certaines zones dans des zones

Si des exemples musicaux sont insérés dans des tables, séléctionnez les exemples musicaux dans la région staffNotation, puis sélectionnez la table dans région table insérant ainsi staffNotation dans table.
Exemple page 20 de Burmeister.

## Numérotation des régions

La numérotation se fait en fonction de la dernière région du balisage automatique. C'est-à-dire que si vous ajouter une région, elle prendra le numéro suivant de la dernière balise de la page. Il est donc préférable si on doit modifier la numérotation, de mettre à jour sa numérotation quand le réglage du balisage des régions est terminé.

## Zoom

- Le zoom permet de préciser le balisage des régions. Il est préférable de zoomer la région sur laquelle on veut travailler avant de la modifier et d'ajuster les balisages sans erreur.
- Eviter de zoomer en sélectionnant l'extérieur d'une marge. 

## Table de l'ensemble des catégories de régions avec leurs équivalents en XML : 

|       Classe       |            Page XML : Region class et @type ou @custom :            |
|:------------------:|:----------------------------------------------------------------:|
|      Paragraph     |         <pc:TextRegion id="region_id_0" type="paragraph">        |
|       Caption      |          <pc:TextRegion id="region_id_0" type="caption">         |
|       Header       |          <pc:TextRegion id="region_id_0" type="header">          |
|       Heading      |          <pc:TextRegion id="region_id_0" type="heading">         |
|       Footer       |          <pc:TextRegion id="region_id_0" type="footer">          |
| Drop-capital       |       <pc:TextRegion id="region_id_0" type="drop-capital">       |
|     Marginalia     |        <pc:TextRegion id="region_id_0" type="marginalia">        |
|      Footnote      |         <pc:TextRegion id="region_id_0" type="footnote">         |
|        Other       |           <pc:TextRegion id="region_id_0" type="other">          |
|        List        |          <pc:TextRegion id="region_id_0" type="caption">         |
|     Line group     | <pc:TextRegion id="region_id_0" custom="linegroup" type="other"> |
|   Staff notation   |     <pc:MusicRegion id="region_id_0" custom="staffNotation">     |
| Tablature notation |   <pc:MusicRegion id="region_id_2" custom="tablatureNotation">   |
|        Table       |                 <pc:TableRegion id="region_id_0">                |
|       Graphic      |                <pc:GraphicRegion id="region_id_0">               |
|        Image       |                 <pc:ImageRegion id="region_id_0">                |
|    Line drawing    |              <pc:LineDrawingRegion id="region_id_0">             |
|      Separator     |               <pc:SeparatorRegion id="region_id_0">              |



## Conseils méthologiques pour la relecture de la transcription

* Utilisation du zoon pour élargir la ou les zones à relire.
* Ouvrir la transcription avec "alt gr+#".
* Régler avec la souris le cadre de la région du texte à corriger afin de pouvoir superposer ce cadre au dessus de la région à corriger.
* Cliquer sur "ok" quand les corrections sont terminées.
* Sauvegarder en faisant "alt+s" pour windows.


## Préfixes spécifiques pour certains caractères 

* Le q́ latin est noté [q+aigu]
* Les caractères grecs sont précédés de [GR], exemple : [GR γάμμα]
* Les caractères musicaux sont précédés [Mus ]
* Si un court exemple musical se trouve dans un paragraphe de texte, il est indiqué comme ceci : [Mus musical staff]

## Liste des symboles
### Les caractères latins

| Caractère  Unicode| Hex Unicode | Transcription|    image    |
|:-----------------:|:-----------:|:------------:|:-----------:|
|         â         |             |              |             |
|         &         |             |              |             |
|         ſ         |             |              |             |
|         Æ         |             |              |             |
|         ũ         |             |              |             |
|         ù         |             |              |             |
|         q́         |             |              |             |
|         ß         |        	  |              |             |
|         æ         |             |              |             |
|         œ         |             |              |             |
|         ò         |             |              |             |
|         ô         |             |              |             |
|         ê         |             |              |             |
|         ÿ         |             |              |             |
|         *         |             |              |             |
|         m̃         |             |              |             |
|         ì         |             |              |             |
|         í         |             |              |             |
|         á         |             |              |             |
|         č         |             |              |             |
|         ó         |             |              |             |
|                  |  U+E8BF     |              |             |
|                   |             |[q+aigu]      |             |
|                   |             |[+aigu]      |![qaiguligated](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/tree/master/img/q_aigu_ligated.jpg)|
|                   |             |              |             |
|                   |             |              |             |


### Les caractères grecs
| Caractère Unicode | Hex Unicode | Transcription|    image    |
|:-----------------:|:-----------:|:------------:|:-----------:|
|         Ω         |             |              |             |
|         Π         |             |              |             |
|         ώ         |             |              |             |
|         ψ         |             |              |             |
|         g         |             |              |             |
|         έ         |             |              |             |
|         ω         |             |              |             |
|         ϛ         |             |              |             |
|         ρ         |             |              |             |
|         δ         |             |              |             |
|         ι         |             |              |             |
|         ά         |             |              |             |
|         ο         |             |              |             |
|         ϰ         |  U+03F0     |              |             |
|         μ         |             |              |             |
|         υ         |             |              |             |
|         ϊ         |             |              |             |
|         ι         |             |              |             |
|         σ         |             |              |             |
|         α         |             |              |             |
|         γ         |             |              |             |
|         δ         |             |              |             |
|         ε         |             |              |             |
|         ζ	        |             |              |             |
|         β         |             |              |             |
|         λ         |             |              |             |
|         ἁ         |             |              |             |
|         π         |             |              |             |
|         ῶ         |             |              |             |
|         ν         |             |              |             |
|         λ         |             |              |             |
|         ή         |             |              |             |
|         ύ         |             |              |             |
|         ϱ         |             |              |             |
|         τ         |             |              |             |
|         ῤ         |             |              |             |
|         φ         |             |              |             |
|         ῦ         |             |              |             |
|         π         |             |              |             |
|         ῖ         |             |              |             |
|         ἄ         |             |              |             |
|         Ϥ         |             |              |             |
|         ὡ         |             |              |             |
|         ϒ         |             |              |             |
|         Γ         |             |              |             |
|         ἡ         |             |              |             |
|         ἰ         |             |              |             |
|         η         |             |              |             |
|         Σ         |             |              |             |
|         Γ         |             |              |             |
|         Ψ         |             |              |             |
|         Λ         |             |              |             |
|         Φ         |             |              |             |
|         Δ         |             |              |             |
|         Ξ         |             |              |             |
|         Θ         |             |              |             |
|         ἔ         |             |              |             |
|         ϲ         |             |              |             |
|                   |             |              |             |
|                   |             |              |             |


### Les caractères musicaux
| Caractère Unicode | Hex Unicode | Transcription|    image    |
|:-----------------:|:-----------:|:------------:|:-----------:|
|          †        |             |              |             |
|          ♪        |             |              |             |
|          𝅗𝅥         |             |              |             |
|          𝅆         |             |              |             |
|          #        |             |              |             |
|          𝆶        |   U+1D1B6   | [Mus maxima] |             |
|          𝆷        |  U+1D1B7    | [Mus longa]  |             |
|          𝆸        |  U+1D1B8    | [Mus brevis] |             |
|          𝆹        |  U+1D1B9    |[Mus sebrevis]|             |
|          𝅭         |  U+1D16D    |[Mus aug dat] |             |
|          𝆹𝅥        |  U+1D1BB    | [Mus minima] |             |
|          𝆺𝅥        |  U+1D1BC    |[Mus seminima]|             |
|          𝆺𝅥𝅮        |  U+1D1BE    | [Mus fusa]   |             |
|          ♮        |   U+266E    |              |             |
|          𝄞        |  U + 1D11E  | [Mus clef G] |             |
|                   |  U+1D122    | [Mus clef F] |             |
|                   |             |[Mus clef C1] |             |
|                   |             |[Mus clef C3] |             |
|         g         |  U+0067     |     [Mus g]  |             |
|         Ƒ         |  U+0191     |              |             |
|         𝄐         |  U+1D110    |[Mus fermata] |             |
|         𝄑         |  U+1D111    |[Mus fermatab]|             |
|                   |             |              |             |
|                   |             |              |             |