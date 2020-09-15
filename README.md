# imageAnnotationGroundTruth

 Amélioration du balisage généré automatiquement par TMG_ImageAnnotation.

## Restructuration du balisage automatique

- Supprimer les balisages inutiles.
- La possibilité de passer d'une région à une autre avec la flèche descendante du clavier permet de repérer de petites régions balisées en dessous d'une grande région. Après avoir identifié l'une de ces petites régions, supprimer la avec la touche backspace.

## Paragraphe

Les paragraphes sont identifiés par leur indentation. 

![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphp35.png?raw=true) 

Il y a cependant quelques exceptions:
- Un paragraphe continu sur deux pages a été identifié commes deux paragraphes distincts.
- L'épigramme est identifié dans une seule région paragraph. Exemple page 5 de Burmeister.
- Les poèmes ont été identifié dans la région linegroup. 
Exemple :
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/linegroupp50.png?raw=true)

## Portées, caractères musicaux et notation par lettres
### staffNotation :
- Toutes les portées sont signalées par la région staffNotation. 
- Si un début de portée précède de la notation par lettres, la région est signalée par staffNotation. 
- Quand la notation par lettres n'est pas une tablature, elle est identifiée comme une région staffNotation. Exemple p. 14.
- Une tablature accompagnant une mélodie sur portée intègre la région staffNotation. Exemple p. 14.

### paragraph :
- Les caractères musicaux dans le texte ne représentent pas une région particulière. Quand un caractère sans portée se trouvent isolé sur une ligne de texte, ils intègrent la région paragraph qui sélectionne le texte.
Exemple page 13 de Burmeister

#### tablatureNotation :
- La notation par lettres est généralement considérée comme la région tablatureNotation.

## Encodade d'une région dans une autre région

Si des exemples musicaux sont insérés dans des tables, séléctionnez les exemples musicaux dans la région staffNotation, puis sélectionnez la table dans une région table insérant ainsi la région staffNotation dans table.
Exemple page 20 de Burmeister.

## Numérotation des régions

La numérotation se fait en fonction de la dernière région du balisage automatique. C'est-à-dire que si vous ajouter une région, elle prendra le numéro suivant de la dernière balise de la page. Il est donc préférable si on doit modifier la numérotation, de mettre à jour sa numérotation quand le réglage du balisage des régions est terminé.

## Zoom

- Le zoom permet de préciser le balisage des régions. Il est préférable de zoomer la région sur laquelle on veut travailler avant de la modifier et d'ajuster les balisages sans erreur.
- Eviter de zoomer en sélectionnant l'extérieur d'une marge. 

## Table de l'ensemble des catégories de régions avec leurs équivalents en XML : 
- Notre fichier mets.xml utilise le format [PAGE XML](https://ocr-d.de/en/gt-guidelines/trans/trPage.html "lien vers OCR-D/Documentation of the PAGE XML Format") généré par OCR-D. Certaines zones ont évolué en fonction du contenu de ces sources spécifiques que sont les traités musicaux. 

|       Classe       |            Page XML : Region class et @type ou @custom :         | exemples en image  |
|:------------------:|:----------------------------------------------------------------:|:------------------:|
|      Paragraph     |         <pc:TextRegion id="region_id_0" type="paragraph">        |                    |
|       Caption      |          <pc:TextRegion id="region_id_0" type="caption">         |                    |
|       Header       |          <pc:TextRegion id="region_id_0" type="header">          |                    |
|       Heading      |          <pc:TextRegion id="region_id_0" type="heading">         |                    |
|       Footer       |          <pc:TextRegion id="region_id_0" type="footer">          |                    |
| Drop-capital       |       <pc:TextRegion id="region_id_0" type="drop-capital">       |                    |
|     Marginalia     |        <pc:TextRegion id="region_id_0" type="marginalia">        |                    |
|      Footnote      |         <pc:TextRegion id="region_id_0" type="footnote">         |                    |
|        Other       |           <pc:TextRegion id="region_id_0" type="other">          |                    |
|        List        |          <pc:TextRegion id="region_id_0" type="caption">         |                    |
|     Line group     | <pc:TextRegion id="region_id_0" custom="linegroup" type="other"> |                    |
|   Staff notation   |     <pc:MusicRegion id="region_id_0" custom="staffNotation">     |                    |
| Tablature notation |   <pc:MusicRegion id="region_id_2" custom="tablatureNotation">   |                    |
|        Table       |                 <pc:TableRegion id="region_id_0">                |                    |
|       Graphic      |                <pc:GraphicRegion id="region_id_0">               |                    |
|        Image       |                 <pc:ImageRegion id="region_id_0">                |                    |
|    Line drawing    |              <pc:LineDrawingRegion id="region_id_0">             |                    |
|      Separator     |               <pc:SeparatorRegion id="region_id_0">              |                    |



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
- Certains caractères ne s'affiches pas. Nous avons utilisé une tanscription pour les désigner.
- Le ![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/qligated.png?raw=true) ne s'affiche pas dans le READme sur github mais s'affiche dans notre transcription.
- Le character ou l'Unicode hexadécimal se réfère à celui proposé par l'[OCR-D](https://ocr-d.de/en/gt-guidelines/trans/trFremdsprache.html "lien vers la page de l'OCR-D").

| Character | Unicode hexadecimal | Transcription|    image    |
|:---------:|:-------------------:|:------------:|:-----------:|
|         á |    ``&#x00E1;``     |              |             |
|         â |    ``&#x00E2;``     |              |             |
|         æ |    ``&#x00E6;``     |              |             |
|         Æ |    ``&#x00C6;``     |              |             |
|         č |    ``&#x010D;``     |              |             |
|         ê |    ``&#x00EA;``     |              |             |
|         & |    ``&#x0026;``     |              |             |
|         ì |    ``&#x00EC;``     |              |             |
|         í |    ``&#x00ED;``     |              |             |
|         m̃ |``&#x006D;&#x0303;`` |              |             |
|         ò |    ``&#x00F2;``     |              |             |
|         ó |    ``&#x00F3;``     |              |             |
|         ô |    ``&#x00F4;``     |              |             |
|         œ |    ``&#x0153;``     |              |             |
|         q́ |    ``&#x0301;``     |   [q+aigu]   | ![qaiguligated](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/qaigu.png?raw=true) |
|  q&#x037E;|    ``q&#x037E;``    |              |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/qligated.png?raw=true)|
|      	  q́;|``q&#x0301;&#x037E;``|[q&#x037E;+aigu]|![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/q_aigu_ligated.jpg?raw=true)|
|         ſ |    ``&#x017F;``     |              |             |
|         ß |    ``&#x00DF;``  	  |              |             |
|         ũ |    ``&#x0169;``     |              |             |
|         ù |    ``&#x00F9;``     |              |             |
|         ÿ |    ``&#x00FF;``     |              |             |
|         * |    ``&#x002A;``     |              |             |
|           |                     |              |             |


### Les caractères grecs
|   Character   | Unicode hexadecimal |
|:-------------:|:-------------------:|
|       Γ       |    ``&#x0393;``     |
|       Δ       |    ``&#x0394;``     |
|       Θ       |    ``&#x0398;``     |
|       Λ       |    ``&#x039B;``     |
|       Ξ       |    ``&#x039E;``     |
|       Π       |    ``&#x03A0;``     |
|       Σ       |    ``&#x03A3;``     |
|       Φ       |    ``&#x03A6;``     | 
|       Ψ       |    ``&#x03A8;``     |
|       Ω       |    ``&#x03A9;``     |
|       ά       |    ``&#x03AC;``     |
|       έ       |    ``&#x03AD;``     |
|       ή       |    ``&#x03AE;``     |  
|       ἰ       |    ``&#x03A9;``     |
|       α       |    ``&#x03B1;``     |
|       β       |    ``&#x03B2;``     |
|       γ       |    ``&#x03B3;``     |
|       δ       |    ``&#x03B4;``     |
|       ε       |    ``&#x03B5;``     |
|       ζ 	    |    ``&#x03B6;``     |
|       η       |    ``&#x03B7;``     |
|       θ       |    ``&#x03B8;``     |
|       ι       |    ``&#x03B9;``     |
|       λ       |    ``&#x03BB;``     |
|       μ       |    ``&#x03BC;``     |
|       ν       |    ``&#x03BD;``     |
|       ο       |    ``&#x03BF;``     |
|       π       |    ``&#x03C0;``     |
|       ρ       |    ``&#x03C1;``     |
|       ϛ       |    ``&#x03C2;``     |
|       σ       |    ``&#x03C3;``     |
|       τ       |    ``&#x03C4;``     |
|       υ       |    ``&#x03C5;``     |
|       φ       |    ``&#x03C6;``     |
|       ψ       |    ``&#x03C8;``     |
|       ω       |    ``&#x03C9;``     |
|       ϊ       |    ``&#x03CA;``     |
|       ύ       |    ``&#x03CD;``     |
|       ώ       |    ``&#x03CE;``     |
|       ϒ       |    ``&#x03D2;``     |
|       ϕ       |    ``&#x03D5;``     |
|       Ϥ       |    ``&#x03E4;``     |
|       ϰ       |    ``&#x03F0;``     |
|       ϱ       |    ``&#x03F1;``     | 
|       ϲ       |    ``&#x03F2;``     |
|       ἁ       |    ``&#x1F01;``     | 
|       ἄ       |    ``&#x1F04;``     |
|       ἔ       |    ``&#x1F14;``     |
|       ὡ       |    ``&#x1F61;``     |
|       ῖ       |    ``&#x1FD6;``     |
|       ῤ       |    ``&#x1FE4;``     |
|       ῦ       |    ``&#x1FE6;``     |
|       ῶ       |    ``&#x1FF6;``     |
|               |                     |


### Les caractères musicaux
- Le character ou l'Unicode hexadécimal se réfère à celui proposé par le site [babelstone](https://www.babelstone.co.uk/Unicode/babelmap.html "lien vers le site babelstone").

| Character | Unicode hexadecimal | Transcription|    image    |
|:---------:|:-------------------:|:------------:|:-----------:|
|     †     |    ``&#x2020;``     |              |             |
|     #     |    ``&#x0023;``     |              |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/diese.png?raw=true) |
|     𝆶     |    ``&#x1D1B6;``    | [Mus maxima] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/maxima.png?raw=true)|
|     𝆷     |    ``&#x1D1B7;``    | [Mus longa]  |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/longa.png?raw=true)|
|     𝆸     |    ``&#x1D1B8;``      | [Mus brevis] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/brevis.png?raw=true)|
|     𝆹      |   ``&#x1D1B9;``     |[Mus sebrevis]|![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/sebrevis.png?raw=true)|
|     𝅭      |  ``&#x1D16D;``      | [Mus aug dat] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/longadatp16.png?raw=true)             |
|     𝆹𝅥      |  ``&#x1D1BB;``      | [Mus minima] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/minima.png?raw=true)             |
|     𝆺𝅥      |  ``&#x1D1BC;``      |[Mus seminima]|![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/seminima.png?raw=true)             |
|     𝆺𝅥𝅮      |  ``&#x1D1BE;``      | [Mus fusa]   |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/fusa.png?raw=true)             |
|     ♮     |   ``&#x266E;``      |              |             |
|     𝄞     |    ``&#x1D11E;``    | [Mus clef G] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/ClefG.jpg?raw=true) |
|     𝄢       |    ``&#x1D122;``   | [Mus clef F] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/ClefF.jpg?raw=true) |
|     𝄡       |    ``&#x1D121;``   | [Mus clef C1] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/ClefC1.jpg?raw=true)|
|     𝄡       |   ``&#x1D121;``    |[Mus clef C3] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/ClefC3.jpg?r3aw=true)             |
|     g       |    ``&#x0067;``    |     [Mus g]  |             |
|     Ƒ       |    ``&#x0191;``    |              |             |
|     𝄐       |    ``&#x1D110;``   |[Mus fermata] |             |
|     𝄑       |    ``&#x1D111;``   |[Mus fermatab]|             |
|             |                    |              |             |
|             |                    |              |             |
