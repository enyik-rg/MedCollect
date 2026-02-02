# MedCollect
## MedCollect egészségügyi álhírkorpusz  

A korpuszt az *MTA-SZTE-DE Elméleti Nyelvészeti és Informatikai Kutatócsoport* készítette.  

A korpusz gyűjtése és annotálása az *MTA Tudomány a Magyar Nyelvért Nemzeti Program Álhírek, áltudományos nézetek nyelvészeti azonosítása* c. alprogramja támogatásával készült.


## A könyvtár tartalma

* **MedCollect_all_txt.zip** - A MedCollect korpusz szövegei .txt formátumban
* **file_description.tsv** - A MedCollect korpusz fájljainak alapvető tulajdonságai 
* **allAnnotatedWord_felszolitas.xlsx** - A felszólító alakkal kifejezett direktívák annotált jegyei
* **allAnnotatedWord_indirekt.xlsx** - A felszólító alakkal nélküli direktívák annotált jegyei
* **allAnnotatedWord_tegezes.xlsx** - A társas deixis annotált jegyei

### MedCollect_all_txt.zip
A MedCollect összes egészségügyi hírének szövege .txt formátumban. 
A zip file-ban az álhírek és a valódi hírek szövege külön mappában van:   
* allTxt/fn/ - álhírek  
* allTxt/tn/ - valódi hírek

### file_description.tsv  
A MedCollect korpusz szövegfájljainak a jellemzői .tsv fájlban. Az oszlopok értelmezése: 
* **id** - A szöveg/file azonosítója
* **title** - A szöveg címe
* **url** - A szöveg eredeti elérhetősége
* **date** - A szöveg létrehozásának dátuma
* **s_num** - A szöveg mondatainak a száma (e-magyar elemzés szerint)
* **w_num** - A szöveg szavainak a száma (e-magyar elemzés szerint)
* **c_num** - A szöveg karaktereinek a száma (tokenelválasztó karakter nélkül)
* **MedCollect** - a szöveg álhírbesorolása:
  * *fn*: álhír
  * *ctrl*: valódi hír
* **annotated** - manuálisan annotált-e: *True/False*

### allAnnotatedWord_felszolitas.xlsx  
A MedCollect korpuszban felszólító alakkal kifejezett direktívaként elemzett nyelvi elemek listája, az annotált jegyekkel együtt.  
Az Excel file sorai az egyes annotált nyelvi elem adatait mutatják.  
Az oszlopok értelmezése: 
* **id** - Az annotált elem azonosítója {fájl}*s*{mondat}*w*{szó} formában, pl. *fn001s14w26*.
* **MC** - A tartalmazó szöveg álhírbesorolása: 
  * *fn*: álhír
  * *ctrl*: valódi hír
* **form** - Az annotált elem szóalakja.
* **directive** - Az annotált elem funkciója. Lehetséges értékei:
  * *1nodirectiva*
  * *2saját hangú*
  * *3közvetített*
  * *4meta*
  * *5ambiguous*
  * *6szövegszervező*
  * *7interakciós*
* **source** - A direktíva forrása. Lehetséges értékei:
  * _
  * *1speaker*
  * *2speaker*+
* **target** - A direktíva címzettje. Lehetséges értékei:
  * _
  * *1listener*
  * *2listener*+
  * *3inclusive*
* **sentence** - Az annotált elemet tartalmazó mondat.

### allAnnotatedWord_indirekt.xlsx  
A MedCollect korpuszban nem felszólító alakkal kifejezett direktívaként elemzett nyelvi elemek listája, az annotált jegyekkel együtt.  
Az Excel file sorai az egyes annotált nyelvi elem adatait mutatják.  
Az oszlopok értelmezése: 
* **id** - Az annotált elem azonosítója {fájl}*s*{mondat}*w*{szó} formában, pl. *fn001s14w26*. A szavak számozása 2-vel kezdődik a mondatok elé beillesztett *XXX* szó miatt.
* **MC** - A tartalmazó szöveg álhírbesorolása: 
  * *fn*: álhír
  * *ctrl*: valódi hír
* **form** - Az annotált elem szóalakja. Abban az esetben, amikor a direktívaként való olvasatot kiváltó nyelvi elem nem azonosítható, de a mondat direktívaként értelmezhető, a mondat első szavaként beillesztett *XXX* szó kapta az annotációt - ez a *form* oszlopban is *XXX*-ként jelenik meg.
* **action** - Ha a végrehajtandó cselekvést nem az annotált nyelvi elem fejezi ki, hanem egy másik nyelvi elem, ez a másik nyelvi elem van itt (pl. az *El kell menned* mondatban a *menned*). Az _ érték ennek hiányát mutatja.
* **directive** - Az annotált elem funkciója. Lehetséges értékei:
  * *1nodirectiva*
  * *2saját hangú*
  * *3közvetített*
  * *4meta*
  * *5ambiguous*
  * *6szövegszervező*
  * *7interakciós*
* **source** - A direktíva forrása. Lehetséges értékei:
  * _
  * *1speaker*
  * *2speaker*+
* **target** - A direktíva címzettje. Lehetséges értékei:
  * _
  * *1listener*
  * *2listener*+
  * *3inclusive*
* **sentence** - Az annotált elemet tartalmazó mondat. A mondat nem tartalmazza a mondatkezdő *XXX* szót.

### allAnnotatedWord_tegezes.xlsx
A MedCollect korpuszban a társas deixist kifejező nyelvi elemek listája, az annotált jegyekkel együtt.  
Az Excel file sorai az egyes annotált nyelvi elem adatait mutatják.  
Az oszlopok értelmezése: 
* **id** - Az annotált elem azonosítója {fájl}*s*{mondat}*w*{szó} formában, pl. *fn001s14w26*.
* **MC** - A tartalmazó szöveg álhírbesorolása: 
  * *fn*: álhír
  * *ctrl*: valódi hír
* **form** - Az annotált elem szóalakja.
* **word** - a szószintű tegező/magázó kifejezések funkciója. Lehetséges értékei:
  * _ - nem szószintű elem esetén
  * *1Tegezés*
  * *2Magázás*
  * *3metaTegezés*
  * *4metaMagázás*
  * *5hipoTegezés*
  * *7Idiomatikus*
  * *8megszólítás*
* **text** - a szövegszintű tegezés/magázás értékelése. (A szöveg végéhez adott egyszavas *XXXXX* mondaton jelölve.) Lehetséges értékei:
  * _ - nem szövegszintű elem esetén
  * 0 - nem volt a szövegben tegező/magázó alak
  * *1TEGEZÉS* - csak tegező alak volt a szövegben
  * *2MAGÁZÁS*+ - csak magázó alak volt a szövegben
  * *3KEVERT* - tegező és magázó alak egyaránt előfordult a szövegben
* **meta** - a szövegszintű metaTegezés/metaMagázás értékelése. (A szöveg végéhez adott egyszavas *XXXXX* mondaton jelölve.) Lehetséges értékei:
  * _ - nem szövegszintű elem esetén
  * 0 - nem volt a szövegben metaTegező/metaMagázó alak
  * *1KOHERENS* - a szövegben koherens volt a metaTegező/metaMagázó alakok használata
  * *2INKOHERENS* - a szövegben nem volt  a metaTegező/metaMagázó alakok használata
* **sentence** - Az annotált elemet tartalmazó mondat.
