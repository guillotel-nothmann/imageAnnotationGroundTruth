# imageAnnotationGroundTruth
  
 Amélioration du balisage généré automatiquement par TMG_ImageAnnotation.
  
## Table de l'ensemble des catégories de régions avec leurs équivalents en XML : 
- Notre fichier mets.xml utilise le format [PAGE XML](https://ocr-d.de/en/gt-guidelines/trans/trPage.html "lien vers OCR-D/Documentation of the PAGE XML Format") généré par OCR-D. Certaines zones ont évolué en fonction du contenu de ces sources spécifiques que sont les traités musicaux.  
- Les exemples en image s'affichent, soit quand vous cliquez sur le mot `exemple` ou dans les paragrahes après cette table décrivant toutes les classes des régions.


|       Classe       |            Page XML : Region class et @type ou @custom           | exemples en image  |
|:------------------:|:----------------------------------------------------------------:|:------------------:|
|      Paragraph     |         <pc:TextRegion id="region_id_0" type="paragraph">        |[Exemple&nbsp;1](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphp35.png?raw=true) [Exemple&nbsp;2](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphSur2pages.jpg?raw=true)|
|       Caption      |          <pc:TextRegion id="region_id_0" type="caption">         |[Exemple&nbsp;3](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionTable.png?raw=true) [Exemple&nbsp;4](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionStaffNotation.png?raw=true) [Exemple&nbsp;5](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptiontablatureNotation.png?raw=true) [Exemple&nbsp;6](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionImage.png?raw=true)|
|       Header       |          <pc:TextRegion id="region_id_0" type="header">          |[Exemple&nbsp;7](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/Header.png?raw=true)|
|       Heading      |          <pc:TextRegion id="region_id_0" type="heading">         |[Exemple&nbsp;8](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/HeadingParagraph.png?raw=true)|
|       Footer       |          <pc:TextRegion id="region_id_0" type="footer">          |[Exemple&nbsp;9](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/FooterParagraph.png?raw=true)|
|    Drop-capital    |       <pc:TextRegion id="region_id_0" type="drop-capital">       |[Exemple&nbsp;10](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/DropCapital2Lines.png?raw=true) [Exemple&nbsp;11](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/DropCapitalOrnement.png?raw=true)|
|     Marginalia     |        <pc:TextRegion id="region_id_0" type="marginalia">        |[Exemple&nbsp;12](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/MarginaliaParagraph.png?raw=true)|
|      Footnote      |         <pc:TextRegion id="region_id_0" type="footnote">         |                    |
|        Other       |           <pc:TextRegion id="region_id_0" type="other">          |[Exemple&nbsp;13](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/OtherManuscrit.png?raw=true) [Exemple&nbsp;14](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/OtherDateAuteur.png?raw=true)|
|        List        |          <pc:TextRegion id="region_id_0" type="other">         |[Exemple&nbsp;15](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/listp34.png?raw=true)|
|     Line group     | <pc:TextRegion id="region_id_0" custom="linegroup" type="other"> |[Exemple&nbsp;16](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/linegroupp50.png?raw=true)|
|        Table       |                 <pc:TableRegion id="region_id_0">                |[Exemple&nbsp;3](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionTable.png?raw=true)                    |
|       Graphic      |                <pc:GraphicRegion id="region_id_0">               |                    |
|        Image       |                 <pc:ImageRegion id="region_id_0">                |[Exemple&nbsp;6](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionImage.png?raw=true)                    |
|    Line drawing    |              <pc:LineDrawingRegion id="region_id_0">             |[Exemple&nbsp;17](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/linedrawingp11.png?raw=true)|
|      Separator     |               <pc:SeparatorRegion id="region_id_0">              |                    |
|   Staff notation   |     <pc:MusicRegion id="region_id_0" custom="staffNotation">     |[Exemple&nbsp;4](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionStaffNotation.png?raw=true) [Exemple&nbsp;18](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/StaffNotationEtTablatureP14.png?raw=true) [Exemple&nbsp;19](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/StattNotationLetteNotation.png?raw=true) [Exemple&nbsp;20](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/StattNotationPorteeLetteNotation.png?raw=true) [Exemple&nbsp;21](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaractereMusicauxParagraphP14.png?raw=true)|
| Tablature notation |   <pc:MusicRegion id="region_id_2" custom="tablatureNotation">   |[Exemple&nbsp;5](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptiontablatureNotation.png?raw=true)                    |




### Paragraph

Les paragraphes sont identifiés par leur indentation à l'exception des paragraphes continu sur deux pages. 

- Exemple 1:
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphp35.png?raw=true) 

- Exemple 2:  
Un paragraphe continu sur deux pages est identifié commes deux paragraphes distincts.

![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/paragraphSur2pages.jpg?raw=true)


### Caption

Les légendes des tables, de la notation sur portée, des tablatures ou des images sont signalées par la région caption.

- Exemple 3:
Caption pour une table.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionTable.png?raw=true)

- Exemple 4:
Caption pour une notation sur portée.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionStaffNotation.png?raw=true)

- Exemple 5:
Caption pour une tablature.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptiontablatureNotation.png?raw=true)

- Exemple 6:
Caption pour une image.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionImage.png?raw=true)  


### Header
- Exemple 7: la page de titre du traité de Burmeister. La région header est en violet.  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/Header.png?raw=true)  


### Heading
Les titres et sous-titres des chapiters sont représentés par la région heading.  
- Exemple 8: Le titre d'un chapitre suivi d'un paragraphe.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/HeadingParagraph.png?raw=true)  
   
   
### Footer
La région footer représente les pieds de page comprenant le début du texte de la page suivante et parfois un référencement pour la page consacrée aux corrections située en fin d'ouvrage.  
- Exemple 9: Un paragraphe suivi d'un footer.  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/FooterParagraph.png?raw=true)
   
   
### Drop-capital
Les lettres capitales sont identifiées dans une région spécifique quand elles s'étendent sur plusieurs lignes et se démarquent graphiquement.   
- Exemple 10: Lettre capitale sur plusieurs lignes.  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/DropCapital2Lines.png?raw=true)
   
- Exemple 11: Lettre capitale ornementée.  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/DropCapitalOrnement.png?raw=true)
   

### Marginalia
La région Marginalia représente les marges extérieures en caractères imprimés.   
- Exemple 12: Une marginalia extérieure au paragraphe.  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/MarginaliaParagraph.png?raw=true)
  

### Other
La région Other regroupe des annotations manuscrites, tampons ou des éléments mal placés de date ou d'auteur.   
- Exemple 13: Annotation manuscrite.  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/OtherManuscrit.png?raw=true)  
   
- Exemple 14: Elément date et auteur.   
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/OtherDateAuteur.png?raw=true)  
   

### List
Les listes numérotées ont une région spécifique.  
Exemple 15: Une liste après une région paragraphe.  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/listp34.png?raw=true)  

  
### Linegroup
- Les poèmes ont été identifiés dans la région linegroup.   
Exemple 16:  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/linegroupp50.png?raw=true)  

  
### Table
Les informations structurées en colonnes ou en lignes désignées comme région Table.
- Exemple 3: La région Caption puis Table. La région Caption est de la même couleur que la Table.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionTable.png?raw=true)   
   

### Image
La région Image comprend un dessin.   
- Exemple 6: La région Caption puis une Image.
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionImage.png?raw=true)   
   

### Line drawing
Les lignes séparent des parties et ont un motif particulier.  
- Exemple 17:     
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/linedrawingp11.png?raw=true)     
       
   
### staffNotation :
Les portées de musique sont signalées par la région staffNotation de couleur bleue comme celle des paragraphes. 
- Exemple 4:
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptionStaffNotation.png?raw=true)    
   
Tout texte, annotation par lettre, annotation analytique ou tablature se rattachant aux portées intègre la région staffNotation.    
- Exemple 18:  
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/StaffNotationEtTablatureP14.png?raw=true)   
   
     
Quand la notation par lettre n'est pas une tablature, elle est identifiée comme une région staffNotation.   
- Exemple 19 et 20:   
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/StattNotationLetteNotation.png?raw=true)    
   

[ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/StattNotationPorteeLetteNotation.png?raw=true)    
   
    
Les caractères musicaux dans le texte ne représentent pas une région particulière. Quand un caractère sans portée se trouvent isolé sur une ligne de texte, ils intègrent la région paragraphe qui sélectionne le texte.   
- Exemple 21:    
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaractereMusicauxParagraphP14.png?raw=true)  
  

#### tablatureNotation :
La notation par lettres est définie par la région tablatureNotation   
- Exemple 5: Une tablature précédée d'une région Caption.   
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/CaptiontablatureNotation.png?raw=true)  
   
   
## Superposition de région
Si une région est placée dans une région, il est possible de sélectionner séparemment les régions et ainsi de les superposer.
- Exemple 22 et 23 :
![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/TabledansParagraph.png?raw=true)  
   
[ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/StaffNotationdansTable.png?raw=true)
   
   
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
|             |    ``&#x1D110;``   |[Mus fugueEntA]|![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/fermatap56.png?r3aw=true)             |
|             |    ``&#x1D111;``   |[Mus fugueEntB]|![ImageAnnotationExample](https://github.com/guillotel-nothmann/imageAnnotationGroundTruth/blob/master/img/fermatabp56.png?r3aw=true)             |
|             |                    |              |             |
|             |                    |              |             |

## License
Ce projet est sous licence [CC BY-NC-SA](https://creativecommons.org/licenses/by-sa/4.0/deed.en "lien vers le résumé explicatif")