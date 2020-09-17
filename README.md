# imageAnnotationGroundTruth

 Amélioration du balisage généré automatiquement par TMG_ImageAnnotation.

## Table de l'ensemble des catégories de régions avec leurs équivalents en XML : 
- Notre fichier mets.xml utilise le format [PAGE XML](https://ocr-d.de/en/gt-guidelines/trans/trPage.html "lien vers OCR-D/Documentation of the PAGE XML Format") généré par OCR-D. Certaines zones ont évolué en fonction du contenu de ces sources spécifiques que sont les traités musicaux. 

|       Classe       |            Page XML : Region class et @type ou @custom :         | exemples en image  |
|:------------------:|:----------------------------------------------------------------:|:------------------:|
|      Paragraph     |         <pc:TextRegion id="region_id_0" type="paragraph">        |[Exemple&nbsp;1](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphp35.png?raw=true) [Exemple&nbsp;2](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphSur2pages.jpg?raw=true)|
|       Caption      |          <pc:TextRegion id="region_id_0" type="caption">         |[Exemple&nbsp;3](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionTable.png?raw=true) [Exemple&nbsp;4](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionStaffNotation.png?raw=true) [Exemple&nbsp;5](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptiontablatureNotation.png?raw=true) [Exemple&nbsp;6](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionImage.png?raw=true)|
|       Header       |          <pc:TextRegion id="region_id_0" type="header">          |                    |
|       Heading      |          <pc:TextRegion id="region_id_0" type="heading">         |                    |
|       Footer       |          <pc:TextRegion id="region_id_0" type="footer">          |                    |
| Drop-capital       |       <pc:TextRegion id="region_id_0" type="drop-capital">       |                    |
|     Marginalia     |        <pc:TextRegion id="region_id_0" type="marginalia">        |                    |
|      Footnote      |         <pc:TextRegion id="region_id_0" type="footnote">         |                    |
|        Other       |           <pc:TextRegion id="region_id_0" type="other">          |                    |
|        List        |          <pc:TextRegion id="region_id_0" type="caption">         |                    |
|     Line group     | <pc:TextRegion id="region_id_0" custom="linegroup" type="other"> |                    |
|   Staff notation   |     <pc:MusicRegion id="region_id_0" custom="staffNotation">     |[Exemple&nbsp;4](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionStaffNotation.png?raw=true)                    |
| Tablature notation |   <pc:MusicRegion id="region_id_2" custom="tablatureNotation">   |[Exemple&nbsp;5](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptiontablatureNotation.png?raw=true)                    |
|        Table       |                 <pc:TableRegion id="region_id_0">                |[Exemple&nbsp;3](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionTable.png?raw=true)                    |
|       Graphic      |                <pc:GraphicRegion id="region_id_0">               |                    |
|        Image       |                 <pc:ImageRegion id="region_id_0">                |[Exemple&nbsp;6](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionImage.png?raw=true)                    |
|    Line drawing    |              <pc:LineDrawingRegion id="region_id_0">             |                    |
|      Separator     |               <pc:SeparatorRegion id="region_id_0">              |                    |




### Paragraph

Les paragraphes sont identifiés par leur indentation à l'exception des paragraphes continu sur deux pages. 

- Exemple 1:
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphp35.png?raw=true) 

- Exemple 2:
Exception: un paragraphe continu sur deux pages a été identifié commes deux paragraphes distincts.

![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphSur2pages.jpg?raw=true)

### Caption

Les légendes des tables, de la notation sur portée, des tablatures ou des images sont signalées par la région caption.

- Exemple 3:
Caption pour une table.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionTable.png?raw=true)

- Exemple 4:
Caption pour une notation sur portée.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionStaffNotation.png?raw=true)

-Exemple 5:
Caption pour une tablature.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptiontablatureNotation.png?raw=true)

- Exemple 6:
Caption pour une image.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionImage.png?raw=true)


## Portées, caractères musicaux et notation par lettres
### staffNotation :
- Toutes les portées sont signalées par la région staffNotation. 
- Si un début de portée précède de la notation par lettres, la région est signalée par staffNotation. 
- Quand la notation par lettres n'est pas une tablature, elle est identifiée comme une région staffNotation. Exemple p. 14.
- Une tablature accompagnant une mélodie sur portée intègre la région staffNotation. Exemple p. 14.

### Linegroup
- Les poèmes ont été identifié dans la région linegroup. 
Exemple :
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/linegroupp50.png?raw=true)


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

## Restructuration du balisage automatique

- Supprimer les balisages inutiles.
- La possibilité de passer d'une région à une autre avec la flèche descendante du clavier permet de repérer de petites régions balisées en dessous d'une grande région. Après avoir identifié l'une de ces petites régions, supprimer la avec la touche backspace.


## Conseils méthologiques pour la relecture de la transcription

* Utilisation du zoon pour élargir la ou les zones à relire.
* Ouvrir la transcription avec ``alt gr+#``.
* Régler avec la souris le cadre de la région du texte à corriger afin de pouvoir superposer ce cadre au dessus de la région à corriger.
* Cliquer sur ``ok`` quand les corrections sont terminées.
* Sauvegarder en faisant ``alt+s`` pour windows.


## Les caractères

* L'ensemble des caractères uilisé est représenté par l'Unicode hexadécimal se référant à celui proposé par l'[OCR-D](https://ocr-d.de/en/gt-guidelines/trans/trFremdsprache.html "lien vers la page de l'OCR-D").
* Les caractères grecs sont précédés du préfixe [GR], par exemple : [GR γάμμα].
* Si un court exemple musical se trouve dans un paragraphe de texte, il est indiqué comme ceci : [Mus musical staff]

### Les caractères latins
- Certains caractères ne s'affichant pas, nous avons utilisé une tanscription pour les désigner.

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
|     𝆺𝅥      |  ``&#x1D1BC;``      | [Mus minimab]|![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/minimab.png?raw=true)             |
|     𝆺𝅥𝅮      |  ``&#x1D1BE;``      | [Mus seminimab]   |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/seminimab.png?raw=true)             |
|     ♮     |   ``&#x266E;``      |              |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/becarre.png?r3aw=true)             |
|     𝄞     |    ``&#x1D11E;``    | [Mus clef G] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/ClefG.jpg?raw=true) |
|     𝄢       |    ``&#x1D122;``   | [Mus clef F] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/ClefF.jpg?raw=true) |
|             |    ``&#x1D121;``   | [Mus clef C1] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/ClefC1.jpg?raw=true)|
|             |   ``&#x1D121;``    |[Mus clef C3] |![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/ClefC3.jpg?r3aw=true)             |
|     𝄐       |    ``&#x1D110;``   |[Mus fugueEntA]|![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/fermatap56.png?r3aw=true)             |
|     𝄑       |    ``&#x1D111;``   |[Mus fugueEntB]|![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/fermatabp56.png?r3aw=true)             |
|             |                    |              |             |
|             |                    |              |             |

## License
Ce projet est sous licence [CC BY-NC-SA](https://creativecommons.org/licenses/by-sa/4.0/deed.en "lien vers le résumé explicatif")