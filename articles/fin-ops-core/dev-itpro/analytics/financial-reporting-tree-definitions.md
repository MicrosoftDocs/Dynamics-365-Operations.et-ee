---
title: Aruandluspuu definitsioonid finantsaruannetes
description: See artikkel kirjeldab aruandluspuu definitsioone. Aruandluspuu definitsioon on aruande komponent, mis määratleb organisatsiooni struktuuri.
author: jinniew
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 97ecd7996ed2d8fb12c1038aa296450d3481e6fd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345782"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Aruandluspuu definitsioonid finantsaruannetes

[!include [banner](../includes/banner.md)]

See artikkel käsitleb aruandluspuu definitsioone. Aruandluspuu definitsioon on aruande komponent (koosteüksus), mis aitab määratleda teie organisatsiooni struktuuri ja hierarhiat.

Finantsaruandlus toetab paindlikku aruandlust nii, et ettevõtte struktuuri muutumisel oleks lihtne muudatusi teha. Aruanded koostatakse mitmesugustest komponentidest (koosteüksustest). Üks neist koosteüksustest on aruandluspuu definitsioon. Aruandluspuu definitsioon aitab määratleda teie organisatsiooni struktuuri ja hierarhia. See on dimensioonidevaheline hierarhiastruktuur, mis põhineb finantsandmete dimensiooniseostel. See annab teavet aruandlusüksuse tasandil ja kõigi puu üksuste koondtasandil. Aruandluspuu definitsioone saab kombineerida veerudefinitsioonide ja aruande definitsioonidega koosteüksuste grupi loomiseks, mida saavad kasutada mitu ettevõtet. Aruandlusüksust kasutatakse organisatsiooniskeemi iga välja puhul. Aruandlusüksus võib olla üksik finantsandmete osakond või kõrgematasemelisem kokkuvõttev üksus, mis ühendab teavet muudest aruandlusüksustest. Aruandluspuud sisaldava aruande definitsiooni puhul luuakse aruanne iga aruandlusüksuse ja kokkuvõtte taseme puhul. Kõik need aruanded kasutavad aruande definitsioonis määratud rea ja veeru definitsioone, v.a juhul, kui aruande definitsioon näeb ette aruandluspuu kasutamise readefinitsioonist. Rea ja veeru definitsioonid on finantsaruannete kujunduse ja toimivuse olulised komponendid. Aruandluspuud võimendavad komponente ja toetavad paindlikku aruandlust ettevõtte struktuuri muutumisel. Aruandluspuul mittepõhinevad finantsaruanded kasutavad ainult osasid finantsaruandluse võimalusi. Saate kasutada mitut aruandluspuu definitsiooni koos sama rea ja veeru definitsioonidega, et vaadata oma ettevõtte andmeid eri viisil.

## <a name="reporting-tree-best-practices"></a>Aruandluspuu head tavad
Enne aruandluspuu loomist arvestage järgmisi häid tavasid.

- Esmalt määrake, milliseid aruandluse dimensioone teie juriidiline isik või ettevõte vajab.
- Arvestage sellega, kuidas olete struktuuri seadistanud, ja seejärel koostage oma ettevõtte organisatsiooniskeem. Organisatsiooniskeem aitab teil visualiseerida, kuidas aruandlusüksusi ühte või mitmesse aruandluspuusse rühmitada.
- Alustage madalaimast olemasolevast üksikasjatasemest, näiteks finantsandmetes määratletud osakondadest ja projektidest. Lisage üksikasjatasemele nii palju välju, kui vaja, et kuvada kõrgema taseme jaotused või regioonid. Iga väli tähistab võimalikku aruandlusüksust mis tahes teie loodud aruandluspuus.
- Peate arvestama ka puude loomise parimat moodust. Saate aruandluspuu loomiseks kasutada automaatset koostamisprotsessi või luua aruandluspuu käsitsi. Enne puude kujundamist on oluline mõista mõlemat meetodit.
- Aruandlusüksuste lisamiseks aruandluspuu definitsiooni saate kasutada teie finantsandmetes määratletud aruandlusüksusi.

## <a name="create-multiple-reporting-trees"></a> Mitme aruandluspuu loomine
Oma organisatsiooni andmete eri viisil vaatamiseks saate luua piiramatul arvul aruandluspuid. Iga aruandluspuu saab sisaldada mis tahes kombinatsiooni osakondadest ja kokkuvõtvatest üksustest. Aruande definitsioon võib sisaldada korraga linki ainult ühele aruandluspuule. Aruandlusüksuste struktuuri ümberkorraldamisel saate luua erinevaid aruandluspuid. Seejärel saate kasutada iga aruandluspuu jaoks samu rea- ja veerudefinitsioone. Sel viisil saate kiiresti luua erinevaid finantsaruande paigutusi. Mitme aruandluspuu loomisel saate iga kuu printida finantsaruannete seeria, mis analüüsib ja esitab teie ettevõtte toiminguid mitmesugusel viisil. Lisateavet leiate aruandlusüksuse struktuuride näidetest selle artikli lõpus.

## <a name="create-a-reporting-tree-definition"></a> Aruandluspuu definitsiooni loomine
Aruandluspuu definitsioon sisaldab järgmises tabelis kirjeldatud veerge.

| Aruandluspuu veerg | Kirjeldus |
|-----------------------|-------------|
| Ettevõte               | Aruandlusüksuse ettevõtte nimi. Väärtus **\@ANY**, mis määratakse üldjuhul vaid kokkuvõtvale tasemele, võimaldab kõigil ettevõtetel aruandluspuud kasutada. Kõikidele tütarharudele on määratud ettevõte. |
| Ühiku nimi             | Kood, mis määratleb selle aruandlusüksuse graafilises aruandluspuus. Veenduge, et looksite kordumatu kodeerimissüsteemi, mis on järjepidev ja mida kasutajatel on lihtne mõista. |
| Üksuse kirjeldus      | Aruandlusüksuse pealkiri kuvatakse aruande päises ja jaluses suvandi **UnitDesc** koodina sisestamisel aruande definitsiooni vahekaardil **Päised ja jalused**. Pealkiri kuvatakse aruande rea kirjelduses, kui sisestate suvandi **UnitDesc** readefinitsiooni lahtrisse **Kirjeldus**. |
| Dimensioonid            | Aruandlusüksus, mis tõmbab teavet otse finantsandmetest. See määrab konto ja seotud segmentide loogilise paigutuse ja pikkused. Igal aruandlusüksuse real peab olema selles veerus dimensioon. Saate panna dimensiooni ka kokkuvõtva üksuse reale (nt kulud, mis on selle üksusega otseselt seotud). Kokkuvõtva üksuse reale dimensiooni sisestamisel ei tohiks emaüksustes kasutatavaid kontosid kasutada tütarüksustes. Vastasel korral võidakse summasid dubleerida. |
| Readefinitsioonid       | Aruandlusüksuse readefinitsiooni nimi. Iga aruandluspuu üksuse puhul kasutatakse sama readefinitsiooni. Aruande loomisel kasutatakse iga aruandlusüksuse puhul seda readefinitsiooni. Readefinitsioon võib sisaldada mitut finantsdimensioonide linki. Kui readefinitsioon on aruandluspuus määratud, valige aruande definitsiooni vahekaardil **Aruanne** märkeruut **Kasuta aruandluspuu readefinitsiooni**. |
| Finantsdimensioonide link| Aruandlusüksuse jaoks kasutatav finantsdimensioonide link. Finantsdimensioonide lingid määratakse readefinitsiooni puhul, tuvastamaks finantsdimensioonid, millele siduda. |
| Lehe suvandid          | See veerg juhib, kas aruandlusüksuse andmed keelatakse aruande vaatamisel või printimisel. |
| Ümberarvestuse %              | Emaüksusele eraldatava aruandlusüksuse protsent. Sellesse veergu sisestatud protsent rakendub readefinitsiooni igale reale enne rea väärtuse lisamist emaaruandesse. Näiteks kui tütarüksus tuleb jagada võrdselt kahe osakonna vahel, korrutatakse igal real olevaid summasid 50 protsendiga enne selle väärtuse aruandesse lisamist. Ühel aruandlusüksusel ei saa olla kahte emaüksust. Aruandlusüksuse summade eraldamiseks kahele emaüksusele looge teine sama dimensiooniga aruandlusüksus täiendava 50 protsendi koondamiseks. Sisestage kümnendkohtadeta täisprotsendid. Näiteks **25** tähistab 25 protsendi eraldamist emaüksusele. Kui lisate koma (**.25**), eraldatakse emaettevõttele 0,25%. Alla 1 protsendi suuruse protsendi kasutamiseks kasutage aruande definitsiooni valikut **Luba ümberarvestus &lt;1%**. See suvand asub vahekaardil **Lisasuvandid** dialoogiboksis **Aruande sätted**. Pääsete selle dialoogiboksi juurde nupuga **Muud** aruande definitsiooni vahekaardil **Sätted**. |
| Üksuse turvalisus         | Piirangud selle kohta, millised kasutajad ja grupid pääsevad aruandlusüksuse teabe juurde. |
| Lisatekst       | Aruandel olev tekst. |

Aruandluspuu definitsiooni loomiseks tehke järgmist.

1. Avage aruande kujundaja.
2. Klõpsake **Fail** &gt; **Uus** &gt; **Aruandluspuu definitsioon**.
3. Klõpsake **Redigeeri** &gt; **Sisesta aruandlusüksused dimensioonidest**.
4. Märkige dialoogiboksis **Sisesta aruandlusüksused dimensioonidest** märkeruut iga aruandluspuusse kaasatava dimensiooni puhul. Dialoogiboks **Sisesta aruandlusüksused dimensioonidest** sisaldab järgmisi jaotisi.

    | Lõik                          | Kirjeldus |
    |----------------------------------|-------------|
    | Dimensiooni segmentimise aruandlus | Kasutage segmentide arvu ja pikkuse muutmiseks nuppe **Eralda segmendid** ja **Kombineeri segmendid**.<blockquote>[!NOTE] Saate kombineerida ainult eraldatud segmente. Kasutage mitme dimensiooni kombineerimiseks dimensiooniväärtustes metamärke.</blockquote> |
    | Kaasa/märgi asukoht       | Selles jaotises on loetletud finantsandmetes määratletud dimensioonid ja kuvatud märkide arv kõige pikemas igale dimensioonile määratud väärtuses. Selle dimensiooni lisamiseks aruandluspuu hierarhiasse märkige dimensioonil see ruut. |
    | Segmendi hierarhia ja vahemikud     | See jaotis kuvab dimensioonide hierarhia. Dimensioonide aruandluse järjekorra muutmiseks saate dimensioone loendis liigutada. Väljadel **Alates dimensioonist** ja **Kuni dimensioonini** saate määrata iga dimensiooni väärtuste vahemiku. Kui te vahemikku ei määra, lisatakse aruandluspuule kõik dimensiooniväärtused.<blockquote>[!NOTE] Kui kasutate mitut dimensiooni, kuvatakse tulemuste hulgas ainult dimensioonide kombinatsioonid, millesse on sisestusi tehtud.</blockquote> |

    Illustratsiooni jaoks, mis näitab näidet dialoogiboksist **Sisesta aruandlusüksused dimensioonidest** , vaadake „Näide aruandlusüksuste sisestamise kohta dimensioonide dialoogiboksist”.

5. Lisasegmentide loomiseks (näiteks ühe segmendi jaotamiseks kaheks lühemaks segmendiks) klõpsake õiget asukohta väljal **Märgi asukoht** ja seejärel klõpsake käsku **Tükelda segmendid**.
6. Kahe segmendi mestimiseks ühte segmenti klõpsake segmentide liitmiseks ühte segmendivälja ja seejärel klõpsake käsku **Ühenda segmendid**.
7. Hierarhia määratleb, kuidas dimensioonid üksteisele ja iga dimensiooni vahemiku puhul aruande esitavad. Dimensioonide hierarhia muutmiseks valige alal **Segmendi hierarhia ja vahemikud** teisaldatav dimensioon ja seejärel klõpsake käsku **Liigu üles** või **Liigu alla**.
8. Uude aruandluspuusse lisatavate dimensiooniväärtuse vahemiku määramiseks järgige alas **Segmendi hierarhia ja vahemikud** järgmisi etappe.

    1. Sisestage selle dimensiooni väljale **Alates dimensioonist** vahemiku esimene väärtus.
    2. Sisestage väljale **Kuni dimensioonini** vahemiku viimane väärtus.

9. Korrake alal **Segmendi hierarhia ja vahemikud** iga dimensiooni puhul toiminguid 7–8.
10. Kui olete lõpetanud selle määratlemise, kuidas aruandlusüksused uude aruandluspuusse tuua tuleks, klõpsake nuppu **OK**.
11. Aruandluspuu salvestamiseks klõpsake valikuid **Fail** &gt; **Salvesta**. Sisestage aruandluspuu kordumatu nimi ja kirjeldus ja seejärel klõpsake nuppu **OK**.

### <a name="open-an-existing-reporting-tree-definition"></a>Olemasoleva aruandluspuu definitsiooni avamine

1. Klõpsake aruande kujundajas navigeerimispaanil suvandit **Aruandluspuu definitsioonid**.
2. Topeltklõpsake aruandluspuu loendis nime selle avamiseks.
3. Mis tahes aruandluspuuga seostatud koosteüksuse vaatamiseks paremklõpsake aruandluspuu definitsiooni ja seejärel valige **Seosed**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Aruandluspuu andmete koondamine

Aruandluspuu kasutamisel saate koondada summad aruandluse alamüksusest aruandluse ülemüksuse tasemel. Seda nimetatakse andmete koondamiseks. Summade koondamiseks aruandluspuu emaüksustele kasutatakse järgmisi reegleid.

- Aruandluspuul peavad tütarüksused sisaldama dimensioone, kui pole tegemist üksiktaseme puuga. Emaüksuste puhul pole aruandluspuul üldjuhul dimensioone.

    > [!NOTE]
    > Dimensioonide määramine nii tütar- kui ka emaüksustele võib põhjustada aruandes andmete dubleerimist.

- Aruandluspuus dimensioone sisaldavad aruandlusüksused vastavad dimensioonidele, mida kasutatakse rea ja veeru definitsioonides. Dimensioonikombinatsioon määrab selle üksuse puhul tagastatavad summad. Näiteks selle artikli edaspidises näites 2 annavad read 6 ja 7 väärtused ainult osakondadele 00 ja 01.
- Aruandluspuul dimensioone mittesisaldavate aruandluse emaüksuste summad määratakse tütarüksuse aruandes ja summa koondatakse määratud emaüksusesse. Näiteks kui ülendüksusel (vt Contoso USA-d andmete koondamise näites 2) on kaks alamüksust (022 ja 023) ja see ei sisalda dimensioone, luuakse aruanne iga alam- ja ülemüksuse kohta. Emaüksuse kogusumma on kahe tütarüksuse summa.

### <a name="manage-reporting-units"></a>Aruandlusüksuste haldamine

Iga aruandluspuu definitsioon kuvatakse kordumatus vaates. Ema/tütre hierarhia kuvamiseks on graafiline vaade ja töölehe vaade, milles kuvatakse iga aruandlusüksuse konkreetne teave. Graafiline vaade ja töölehe vaade on ühendatud. Aruandlusüksuse valimisel ühes vaates valitakse see ka teises vaates. Saate luua dimensioonidevahelisi hierarhiaid finantsandmete dimensiooniseoste põhjal. Aruandluspuu definitsiooni loomisel saate kasutada samu readefinitsioone mitu korda, olenemata sellest, kas koostate osakondade kasumiaruande või konsolideeritud kasumi koondaruande. Teie organisatsiooni tulemuste mitmesuguste vaadete pakkumiseks saab readefinitsioonis määratletud dimensioone kombineerida aruandluspuu dimensioonidega.

### <a name="reporting-unit-structure"></a> Aruandlusüksuse struktuur

Finantsaruandluses kasutatakse järgmist tüüpi aruandlusüksusi.

- Üksikasjade üksus tõmbab teavet otse finantsandmetest.
- Kokkuvõtte üksus koondab madalama taseme üksuste andmed.

Aruandluse emaüksus on kokkuvõtte üksus, mis koondab üksikasjade üksuse kokkuvõtteandmed. Kokkuvõttev üksus võib olla nii üksikasjade üksus kui ka kokkuvõttev üksus. Seega võib kokkuvõttev üksus tuua andmeid madalama taseme üksusest või finantsandmetest. Emaüksus võib olla kõrgema taseme emaüksuse tütarüksus. Aruandluse tütarüksus võib olla üksikasjade üksus, mis tõmbab andmeid otse finantsandmetest. Aruandluse tütarüksus võib olla ka kesktaseme kokkuvõtteüksus. Teisisõnu võib see olla madalama taseme üksuse emaüksus ja samuti kõrgema taseme kokkuvõtva üksuse tütarüksus. Kõige tavalisema aruandlusüksuste stsenaariumi korral on emaüksustel veerus **Dimensioonid** tühi lahter ja tütarüksustel lingid kindlatele või metamärgiga dimensioonikombinatsioonidele.

### <a name="organize-reporting-units"></a> Aruandlusüksuste korraldamine

Saate aruandluspuu definitsiooni organisatsioonistruktuuri ümber korraldada, liigutades graafilises vaates aruandlusüksusi. Saate viia aruandlusüksusi ka aruandluspuu kõrgemale tasemele või madalamale tasemele.

1. Avage aruande kujundajas muudetav aruandluspuu.
2. Valige aruandluspuu definitsiooni graafilises vaates aruandlusüksus.
3. Lohistage üksus uude asukohta. Teine võimalus on teha üksusel paremklõps ja valida siis **Edenda aruandlusüksust** või **Alanda aruandlusüksust**.
4. Klõpsake muudatuste salvestamiseks valikuid **Fail** &gt; **Salvesta**.

### <a name="add-text-about-a-reporting-unit"></a> Teksti lisamine aruandlusüksuse kohta

Lisateksti kirje on staatiline kuni 255 märgi pikkune tekstistring, mis lisab aruandluspuu definitsiooni teavet. Näiteks võib lisatekst olla ettevõtte lühikirjeldus. Saate luua kuni kümme lisateksti kirjet aruandluspuu definitsiooni iga aruandlusüksuse puhul. Lisatekst kuvatakse aruandes aruandlusüksuse puhul, millele tekst on määratud. Saate lisada tekstikirjeid readefinitsiooni veerust **Kirjeldus** ja aruande definitsiooni vahekaardilt **Päised ja jalused**.

1. Avage aruande kujundajas muudetav aruandluspuu.
2. Topeltklõpsake aruandlusüksuse rea puhul lahtrit **Lisatekst**.
3. Sisestage lahtri **Lisatekst** esimesele tühjale reale tekst. Esimese teksti sisaldava rea viiteks on UnitText1 olenemata selle asukohast dialoogiboksis **Lisatekst**.
4. Täiendavate tekstikirjete lisamiseks selle aruandlusüksuse puhul sisestage tekst tühjale reale.
5. Klõpsake nupul **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Lisateksti eemaldamine aruandlusüksusest

1. Avage aruandekoosturis muudetav aruandluspuu definitsioon.
2. Topeltklõpsake aruandlusüksuse rea lahtrit **Täiendav tekst**.
3. Valige eemaldatav kirje dialoogiboksist **Lisatekst** ja seejärel klõpsake käsku **Tühjenda**. Teine võimalus on teha kirjel paremklõps ja valida **Lõika**.
4. Klõpsake nupul **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Aruandlusüksusele juurdepääsu piiramine

Saate vältida teatud kasutajate ja gruppide juurdepääsu aruandlusüksusele. Saate määratleda ja piirangud, nii et need kehtiksid aruandlusüksuse tütarüksustele.

1. Avage aruande kujundajas muudetav aruandluspuu.
2. Topeltklõpsake selle aruandlusüksuse rea lahtrit **Üksuse turve**, millele soovite juurdepääsu piirata.
3. Klõpsake dialoogiboksis **Üksuse turvalisus** suvandit **Kasutajad ja grupid**.
4. Valige kasutajad või grupid, kellel peaks olema aruandlusüksusele juurdepääs, ja seejärel klõpsake nuppu **OK**.
5. Aruandluse tütarüksustele juurdepääsu piiramiseks märkige ruut **Turvalisuse lisamine aruandluse tütarüksustele**.
6. Klõpsake nupul **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Aruandlusüksusele juurdepääsu eemaldamine

1. Avage aruande kujundajas muudetav aruandluspuu.
2. Topeltklõpsake lahtrit **Üksuse turvalisus** selle aruandlusüksuse rea puhul, millele juurdepääsu soovite eemaldada.
3. Valige nimi dialoogiboksist **Üksuse turvalisus** ja seejärel klõpsake käsku **Eemalda**.
4. Klõpsake valikut **OK**.

## <a name="examples"></a>Näited
### <a name="reporting-unit-structure--example-1"></a>Aruandlusüksuse struktuur – näide 1

Siin on aruandlusüksuse struktuur järgmises aruandluspuus.

- Aruandlusüksus Contoso Japan on tütarüksuste Contoso Japan Sales ja Contoso Japan Consulting emaüksus.
- Üksus Contoso Japan Sales on üksuse Contoso Japan tütarüksus ja üksuste Home Sales ja Auto Sales emaüksus.
- Madalaima taseme üksikasjade aruandlusüksused (Home Sales, Auto Sales, Client Services ja Operations) kajastavad finantsandmete osakondi. Need aruandlusüksused on diagrammi varjutatud alas.
- Kõrgema taseme kokkuvõtte üksused esitavad üksikasjade üksuste teabe kokkuvõtte.

[![Contoso Kokkuvõtte Aruandestruktuur – Näide 1.](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Aruandlusüksuse struktuur – näide 2

Järgmisel diagrammil on aruandluspuul ettevõtte funktsiooni järgi jaotatud organisatsiooni struktuur.

[![Contoso Kokkuvõtte Aruandestruktuur – Näide 2.](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Näide aruandlusüksuste sisestamise kohta dimensioonide dialoogiboksist

Järgmisel illustratsioonil on dialoogiboksi **Sisesta aruandlusüksused dimensioonidest** näide. Selles näites annavad tulemused äriüksuste, kulukeskuste ja osakondade kombinatsiooni.

[![Aruandlusüksuse lisamine.](./media/insertreportingunits.png)](./media/insertreportingunits.png)

Saadud aruandluspuu definitsiooni sorditakse äriüksuse, siis kulukeskuse ja siis osakonna järgi. Viienda aruandlusüksuse dimensioon on **Äriüksus = \[001\], Kulukeskus = \[\], Osakond = \[022\]** ja tähistab äriüksuse 001 osakonda 022 puudutavate kontode aruandlusüksust.

[![Aruandluspuu Illustratsioon.](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Andmete koondamise näited

Järgmistes näidetes on võimalik teave, mida koondatavate andmete aruandluspuu definitsioonis kasutatakse.

#### <a name="example-1"></a>Näide 1

[![Multi-ettevõtte ümberpööramine.](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Näide 2

[![Ettevõtetevahelise osakonna ümberpööramine.](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandlus](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
