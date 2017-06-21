---
title: Aruandluspuu definitsioonid finantsaruannetes
description: "See artikkel käsitleb aruandluspuu definitsioone. Aruandluspuu definitsioon on aruande komponent (koosteüksus), mis aitab määratleda teie organisatsiooni struktuuri ja hierarhiat."
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 331f3480b8454dac7da12be169ba017f36cefa06
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="reporting-tree-definitions-in-financial-reports"></a>Aruandluspuu definitsioonid finantsaruannetes

[!include[banner](../includes/banner.md)]


See artikkel käsitleb aruandluspuu definitsioone. Aruandluspuu definitsioon on aruande komponent (koosteüksus), mis aitab määratleda teie organisatsiooni struktuuri ja hierarhiat.

Finantsaruandlus toetab paindlikku aruandlust nii, et ettevõtte struktuuri muutumisel oleks lihtne muudatusi teha. Aruanded koostatakse mitmesugustest komponentidest (koosteüksustest). Üks neist koosteüksustest on aruandluspuu definitsioon. Aruandluspuu definitsioon aitab määratleda teie organisatsiooni struktuuri ja hierarhia. See on dimensioonidevaheline hierarhiastruktuur, mis põhineb finantsandmete dimensiooniseostel. See annab teavet aruandlusüksuse tasandil ja kõigi puu üksuste koondtasandil. Aruandluspuu definitsioone saab kombineerida veerudefinitsioonide ja aruande definitsioonidega koosteüksuste grupi loomiseks, mida saavad kasutada mitu ettevõtet. Aruandlusüksust kasutatakse organisatsiooniskeemi iga välja puhul. Aruandlusüksuseks võib olla üksik osakond finantsandmetest või selleks võib olla kõrgema taseme kokkuvõtte üksus, mis ühendab teavet teistest aruandlusüksustest. Aruandluspuud sisaldava aruande definitsiooni puhul luuakse aruanne iga aruandlusüksuse ja kokkuvõtte taseme puhul. Kõik need aruanded kasutavad aruande definitsioonis määratud rea ja veeru definitsioone, v.a juhul, kui aruande definitsioon näeb ette aruandluspuu kasutamise readefinitsioonist. Rea ja veeru definitsioonid on finantsaruannete kujunduse ja toimivuse olulised komponendid. Aruandluspuud võimendavad komponente ja toetavad paindlikku aruandlust ettevõtte struktuuri muutumisel. Aruandluspuul mittepõhinevad finantsaruanded kasutavad ainult osasid finantsaruandluse võimalusi. Saate kasutada mitut aruandluspuu definitsiooni koos sama rea ja veeru definitsioonidega, et vaadata oma ettevõtte andmeid eri viisil.

## <a name="reporting-tree-best-practices"></a>Aruandluspuu head tavad
Enne aruandluspuu loomist arvestage järgmisi häid tavasid.

-   Esmalt määrake, milliseid aruandluse dimensioone teie juriidiline isik või ettevõte vajab.
-   Arvestage sellega, kuidas olete struktuuri seadistanud, ja seejärel koostage oma ettevõtte organisatsiooniskeem. Organisatsiooniskeem aitab teil visualiseerida, kuidas aruandlusüsksusi ühte või mitmese aruandluspuusse grupeerida.
-   Alustage madalaimast olemasolevast üksikasjatasemest, näiteks finantsandmetes määratletud osakondadest ja projektidest. Lisage üksikasjatasemele nii palju välju, kui vaja, et kuvada kõrgema taseme jaotused või regioonid. Iga väli tähistab võimalikku aruandlusüksust mis tahes teie loodud aruandluspuus.
-   Peate arvestama ka puude loomise parimat moodust. Saate aruandluspuu loomiseks kasutada automaatset koostamisprotsessi või luua aruandluspuu käsitsi. Enne puude kujundamist on oluline mõista mõlemat meetodit.
-   Aruandlusüksuste lisamiseks aruandluspuu definitsiooni saate kasutada teie finantsandmetes määratletud aruandlusüksusi.

## <a name="create-multiple-reporting-trees"></a> Mitme aruandluspuu loomine
Oma organisatsiooni andmete eri viisil vaatamiseks saate luua piiramatul arvul aruandluspuid. Iga aruandluspuu võib sisaldada osakondade ja kokkuvõtte üksuste kombinatsiooni. Aruande definitsioon võib sisaldada korraga linki ainult ühele aruandluspuule. Aruandlusüksuste struktuuri ümberkorraldamisel saate luua erinevaid aruandluspuid. Seejärel saate kasutada iga aruandluspuu jaoks samu rea- ja veerudefinitsioone. Sel viisil saate kiiresti luua erinevaid finantsaruande paigutusi. Mitme aruandluspuu loomisel saate iga kuu printida finantsaruannete seeria, mis analüüsib ja esitab teie ettevõtte toiminguid mitmesugusel viisil. Lisateavet leiate aruandlusüksuse struktuuride näidetest selle artikli lõpus.

## <a name="create-a-reporting-tree-definition"></a> Aruandluspuu definitsiooni loomine
Aruandluspuu definitsioon sisaldab järgmises tabelis kirjeldatud veerge.

| Aruandluspuu veerg | Kirjeldus|
|---|---|
| Ettevõte               | Aruandlusüksuse ettevõtte nimi. Väärtus **@ANY**, mis on tavaliselt määratud ainult kokkuvõtte tasemele, võimaldab aruandluspuu kasutamist kõigis ettevõtetes. Kõigile tütarharudele on määratud ettevõte.|
| Üksuse nimi             | Kood, mis määratleb selle aruandlusüksuse graafilises aruandluspuus. Veenduge, et looksite kordumatu kodeerimissüsteemi, mis on järjepidev ja mida kasutajatel on lihtne mõista. |
| Üksuse kirjeldus      | Aruandlusüksuse pealkiri kuvatakse aruande päises ja jaluses suvandi **UnitDesc** koodina sisestamisel aruande definitsiooni vahekaardil **Päised ja jalused**. Pealkiri kuvatakse aruande rea kirjelduses, kui sisestate suvandi **UnitDesc** readefinitsiooni lahtrisse **Kirjeldus**.|
| Dimensioonid            | Aruandlusüksus, mis tõmbab teavet otse finantsandmetest. See määrab konto ja seotud segmentide loogilise paigutuse ja pikkused. Igal aruandlusüksuse real peab olema selles veerus dimensioon. Saate panna dimensiooni ka kokkuvõtva üksuse reale (nt kulud, mis on selle üksusega otseselt seotud). Kokkuvõtva üksuse reale dimensiooni sisestamisel ei tohiks emaüksustes kasutatavaid kontosid kasutada tütarüksustes. Vastasel korral võidakse summasid dubleerida.|
| Readefinitsioonid       | Aruandlusüksuse readefinitsiooni nimi. Sama readefinitsiooni kasutatakse aruandluspuu iga üksuse puhul. Aruande koostamisel kasutatakse seda readefinitsiooni iga aruandlusüksuse puhul. Readefinitsioon võib sisaldada mitme finantsdimensiooni linke. Kui aruandluspuul on määratletud readefinitsioon, märkige ruut **Kasuta aruandluspuu readefinitsiooni** aruande definitsiooni vahekaardil **Aruanne**.|
| Rea link              | Aruandlusüksuse puhul kasutatav rea link. Rea lingid määratletakse readefinitsiooni puhul lingitavate finantsdimensioonide tuvastamiseks.|
| Väline link         | Selle aruandlusüksuse puhul kasutatav rea link. Rea lingid määratletakse readefinitsiooni puhul lingitava aruande tuvastamiseks.|
| Välisfail         | Finantsaruandluse töölehe faili tee, kust andmeid tuua.|
| Lehe suvandid          | See veerg juhib, kas aruandlusüksuse andmed keelatakse aruande vaatamisel või printimisel.|
| Ümberarvestuse %              | Emaüksusele eraldatava aruandlusüksuse protsent. Sellesse veergu sisestatud protsent rakendub readefinitsiooni igale reale enne rea väärtuse lisamist emaaruandesse. Näiteks kui tütarüksus tuleb jagada võrdselt kahe osakonna vahel, korrutatakse igal real olevaid summasid 50 protsendiga enne selle väärtuse aruandesse lisamist. Ühel aruandlusüksusel ei saa olla kahte emaüksust. Aruandlusüksuse summade eraldamiseks kahele emaüksusele looge teine sama dimensiooniga aruandlusüksus täiendava 50 protsendi koondamiseks. Sisestage kümnendkohtadeta täisprotsendid. Näiteks **25** tähistab 25 protsendi eraldamist emaüksusele. Kui lisate koma (**.25**), eraldatakse emaettevõttele 0,25%. Alla 1 protsendi suuruse protsendi kasutamiseks kasutage aruande definitsiooni valikut **Luba ümberarvestus &lt;1%**. See suvand asub vahekaardil **Lisasuvandid** dialoogiboksis **Aruande sätted**. Pääsete selle dialoogiboksi juurde nupuga **Muud** aruande definitsiooni vahekaardil **Sätted**. |
| Üksuse turvalisus         | Piirangud selle kohta, millised kasutajad ja grupid pääsevad aruandlusüksuse teabe juurde.|
| Lisatekst       | Aruandel olev tekst.|

Aruandluspuu definitsiooni loomiseks tehke järgmist.

1.  Avage aruande kujundaja.
2.  Klõpsake **Fail** &gt; **Uus** &gt; **Aruandluspuu definitsioon**.
3.  Klõpsake **Redigeeri** &gt; **Sisesta aruandlusüksused dimensioonidest**.
4.  Märkige dialoogiboksis **Sisesta aruandlusüksused dimensioonidest** märkeruut iga aruandluspuusse kaasatava dimensiooni puhul. Dialoogiboks **Sisesta aruandlusüksused dimensioonidest** sisaldab järgmisi jaotisi.

    | Lõik                          | Kirjeldus                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
    |----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Dimensiooni segmentimise aruandlus | Kasutage nuppe **Tükelda segmendid** ja **Ühenda segmendid** segmentide arvu ja pikkuse muutmiseks. **Märkus.** Ühendada saab ainult tükeldatud segmente. Kasutage mitme dimensiooni kombineerimiseks dimensiooniväärtustes metamärke.                                                                                                                                                                                                          |
    | Kaasa/märgi asukoht       | Selles jaotises on loetletud finantsandmetes määratletud dimensioonid ja kuvatud märkide arv kõige pikemas igale dimensioonile määratud väärtuses. Selle dimensiooni lisamiseks aruandluspuu hierarhiasse märkige dimensioonil see ruut.                                                                                                                                                                                           |
    | Segmendi hierarhia ja vahemikud     | See jaotis kuvab dimensioonide hierarhia. Dimensioonide aruandluse järjekorra muutmiseks saate dimensioone loendis liigutada. Väljadel **Alates dimensioonist** ja **Kuni dimensioonini** saate määrata iga dimensiooni väärtuste vahemiku. Kui te vahemikku ei määra, lisatakse aruandluspuule kõik dimensiooniväärtused. **Märkus.** Mitme dimensiooni kasutamisel kuvatakse tulemustes ainult need dimensioonide kombinatsioonid, millesse on midagi sisestatud. |

    Ekraanipildi, millel on näide dialoogiboksist **Sisesta aruandlusüksused dimensioonidest**, leiate selle artikli edasisest jaotisest Näide dialoogiboksi Sisesta aruandlusüksused dimensioonidest kohta.
5.  Lisasegmentide loomiseks (näiteks ühe segmendi jaotamiseks kaheks lühemaks segmendiks) klõpsake õiget asukohta väljal **Märgi asukoht** ja seejärel klõpsake käsku **Tükelda segmendid**.
6.  Kahe segmendi mestimiseks ühte segmenti klõpsake segmentide liitmiseks ühte segmendivälja ja seejärel klõpsake käsku **Ühenda segmendid**.
7.  Hierarhia määratleb, kuidas dimensioonid üksteisele ja iga dimensiooni vahemiku puhul aruande esitavad. Dimensioonide hierarhia muutmiseks valige alal **Segmendi hierarhia ja vahemikud** teisaldatav dimensioon ja seejärel klõpsake käsku **Liigu üles** või **Liigu alla**.
8.  Uude aruandluspuusse lisatavate dimensiooniväärtuse vahemiku määramiseks järgige alas **Segmendi hierarhia ja vahemikud** järgmisi etappe.
    1.  Sisestage selle dimensiooni väljale **Alates dimensioonist** vahemiku esimene väärtus.
    2.  Sisestage väljale **Kuni dimensioonini** vahemiku viimane väärtus.

9.  Korrake iga dimensiooni puhul alal **Segmendi hierarhia ja vahemikud** toiminguid 7–8.
10. Kui olete lõpetanud selle määratlemise, kuidas aruandlusüksused uude aruandluspuusse tuua tuleks, klõpsake nuppu **OK**.
11. Aruandluspuu salvestamiseks klõpsake valikuid **Fail** &gt; **Salvesta**. Sisestage aruandluspuu kordumatu nimi ja kirjeldus ja seejärel klõpsake nuppu **OK**.

### <a name="open-an-existing-reporting-tree-definition"></a>Olemasoleva aruandluspuu definitsiooni avamine

1.  Klõpsake aruande kujundajas navigeerimispaanil suvandit **Aruandluspuu definitsioonid**.
2.  Topeltklõpsake aruandluspuu loendis nime selle avamiseks.
3.  Mis tahes aruandluspuuga seostatud koosteüksuse vaatamiseks paremklõpsake aruandluspuu definitsiooni ja seejärel valige **Seosed**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Aruandluspuu andmete koondamine

Aruandluspuu kasutamisel saate koondada summad aruandluse tütarüksusest aruandluse emaüksuse tasemel. Seda nimetatakse andmete koondamiseks. Summade koondamiseks aruandluspuu emaüksustele kasutatakse järgmisi reegleid.

-   Aruandluspuul peavad tütarüksused sisaldama dimensioone, kui pole tegemist üksiktaseme puuga. Emaüksuste puhul pole aruandluspuul üldjuhul dimensioone. **Märkus.** Dimensioonide määramine nii tütar- kui ka emaüksustele võib põhjustada aruandes andmete dubleerimist.
-   Aruandluspuus dimensioone sisaldavad aruandlusüksused vastavad dimensioonidele, mida kasutatakse rea ja veeru definitsioonides. Dimensioonikombinatsioon määrab selle üksuse puhul tagastatavad summad. Näiteks selle artikli edaspidises näites 2 annavad read 6 ja 7 väärtused ainult osakondadele 00 ja 01.
-   Aruandluspuul dimensioone mittesisaldavate aruandluse emaüksuste summad määratakse tütarüksuse aruandes ja summa koondatakse määratud emaüksusesse. Näiteks kui emaüksusel (vt Contoso USA-d andmete koondamise näites 2) on kaks tütarüksust (022 ja 023) ja see ei sisalda dimensioone, luuakse aruanne iga tütar- ja emaüksuse kohta. Emaüksuse kogusumma on kahe tütarüksuse summa.

### <a name="manage-reporting-units"></a>Aruandlusüksuste haldamine

Iga aruandluspuu definitsioon kuvatakse kordumatus vaates. Ema/tütre hierarhia kuvamiseks on graafiline vaade ja töölehe vaade, milles kuvatakse iga aruandlusüksuse konkreetne teave. Graafiline vaade ja töölehe vaade on ühendatud. Aruandlusüksuse valimisel ühes vaates valitakse see ka teises vaates. Saate luua dimensioonidevahelisi hierarhiaid finantsandmete dimensiooniseoste põhjal. Aruandluspuu definitsiooni loomisel saate kasutada samu readefinitsioone mitu korda, olenemata sellest, kas koostate osakondade kasumiaruande või konsolideeritud kasumi koondaruande. Teie organisatsiooni tulemuste mitmesuguste vaadete pakkumiseks saab readefinitsioonis määratletud dimensioone kombineerida aruandluspuu dimensioonidega.

### <a name="reporting-unit-structure"></a> Aruandlusüksuse struktuur

Finantsaruandluses kasutatakse järgmist tüüpi aruandlusüksusi.

-   Üksikasjade üksus tõmbab teavet otse finantsandmetest, Exceli arvutustabelist või mõnelt muult finantsaruandluse töölehelt.
-   Kokkuvõtte üksus koondab madalama taseme üksuste andmed.

Aruandluse emaüksus on kokkuvõtte üksus, mis koondab üksikasjade üksuse kokkuvõtteandmed. Kokkuvõttev üksus võib olla nii üksikasjade üksus kui ka kokkuvõttev üksus. Seega võib kokkuvõttev üksus tuua andmeid madalama taseme üksusest, finantsandmetest või Exceli töölehelt. Emaüksus võib olla kõrgema taseme emaüksuse tütarüksus. Aruandluse tütarüksus võib olla üksikasjade üksus, mis tõmbab andmeid otse finantsandmetest või Exceli töölehelt. Aruandluse tütarüksus võib olla ka kesktaseme kokkuvõtteüksus. Teisisõnu võib see olla madalama taseme üksuse emaüksus ja samuti kõrgema taseme kokkuvõtva üksuse tütarüksus. Kõige tavalisema aruandlusüksuste stsenaariumi korral on emaüksustel veerus **Dimensioonid** tühi lahter ja tütarüksustel lingid kindlatele või metamärgiga dimensioonikombinatsioonidele.

### <a name="organize-reporting-units"></a> Aruandlusüksuste korraldamine

Saate aruandluspuu definitsiooni organisatsioonistruktuuri ümber korraldada, liigutades graafilises vaates aruandlusüksusi. Saate viia aruandlusüksusi ka aruandluspuu kõrgemale tasemele või madalamale tasemele.

1.  Avage aruande kujundajas muudetav aruandluspuu.
2.  Valige aruandluspuu definitsiooni graafilises vaates aruandlusüksus.
3.  Lohistage üksus uude asukohta. Teine võimalus on teha üksusel paremklõps ja valida siis **Edenda aruandlusüksust** või **Alanda aruandlusüksust**.
4.  Klõpsake muudatuste salvestamiseks valikuid **Fail** &gt; **Salvesta**.

### <a name="add-text-about-a-reporting-unit"></a> Teksti lisamine aruandlusüksuse kohta

Lisateksti kirje on staatiline kuni 255 märgi pikkune tekstistring, mis lisab aruandluspuu definitsiooni teavet. Näiteks võib lisatekst olla ettevõtte lühikirjeldus. Saate luua kuni kümme lisateksti kirjet aruandluspuu definitsiooni iga aruandlusüksuse puhul. Lisatekst kuvatakse aruandes aruandlusüksuse puhul, millele tekst on määratud. Saate lisada tekstikirjeid readefinitsiooni veerust **Kirjeldus** ja aruande definitsiooni vahekaardilt **Päised ja jalused**.

1.  Avage aruande kujundajas muudetav aruandluspuu.
2.  Topeltklõpsake aruandlusüksuse rea puhul lahtrit **Lisatekst**.
3.  Sisestage lahtri **Lisatekst** esimesele tühjale reale tekst. Esimese teksti sisaldava rea viiteks on UnitText1 olenemata selle asukohast dialoogiboksis **Lisatekst**.
4.  Täiendavate tekstikirjete lisamiseks selle aruandlusüksuse puhul sisestage tekst tühjale reale.
5.  Klõpsake nupul **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Lisateksti eemaldamine aruandlusüksusest

1.  Avage aruande kujundajas muudetav aruandluspuu.
2.  Topeltklõpsake aruandlusüksuse rea puhul lahtrit **Lisatekst**.
3.  Valige eemaldatav kirje dialoogiboksist **Lisatekst** ja seejärel klõpsake käsku **Tühjenda**. Teine võimalus on teha kirjel paremklõps ja valida **Lõika**.
4.  Klõpsake nupul **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Aruandlusüksusele juurdepääsu piiramine

Saate vältida teatud kasutajate ja gruppide juurdepääsu aruandlusüksusele. Saate määratleda ja piirangud, nii et need kehtiksid aruandlusüksuse tütarüksustele.

1.  Avage aruande kujundajas muudetav aruandluspuu.
2.  Topeltklõpsake lahtrit **Üksuse turvalisus** selle aruandlusüksuse rea puhul, millele juurdepääsu soovite piirata.
3.  Klõpsake dialoogiboksis **Üksuse turvalisus** suvandit **Kasutajad ja grupid**.
4.  Valige kasutajad või grupid, kellel peaks olema aruandlusüksusele juurdepääs, ja seejärel klõpsake nuppu **OK**.
5.  Aruandluse tütarüksustele juurdepääsu piiramiseks märkige ruut **Turvalisuse lisamine aruandluse tütarüksustele**.
6.  Klõpsake nupul **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Aruandlusüksusele juurdepääsu eemaldamine

1.  Avage aruande kujundajas muudetav aruandluspuu.
2.  Topeltklõpsake lahtrit **Üksuse turvalisus** selle aruandlusüksuse rea puhul, millele juurdepääsu soovite eemaldada.
3.  Valige nimi dialoogiboksist **Üksuse turvalisus** ja seejärel klõpsake käsku **Eemalda**.
4.  Klõpsake nupul **OK**.

### <a name="link-to-reports"></a>Link aruannete juurde

Pärast **aruande** veeru loomist readefinitsioonis ja aruandesse kaasatava aruande määratlemist peate värskendama aruandluspuud lingitud veeru ja aruande teabega. Aruande saab importida aruandluspuu mis tahes üksusesse.

### <a name="identify-the-report-in-a-reporting-tree"></a>Aruande tuvastamine aruandluspuus

1.  Avage aruande kujundajas muudetav aruandluspuu.
2.  Veerus **Readefinitsioonid** põhineb lahtrite teave valitud rea teabel, kuna sama readefinitsiooni tuleb kasutada kõigis aruandluspuu üksustes. Topeltklõpsake lahtrit **Readefinitsioonid** ja seejärel valige readefinitsioon, mis sisaldab teavet aruande kohta.
3.  Valige aruandlusüksuse lahtrist **Töölehe link** aruandele vastava lingi nimi.
4.  Sisestage aruandlusüksuse lahtrisse **Töövihiku või aruande tee** aruande nimi või sirvige aruande valimiseks.
5.  Aruande töölehe määramiseks sisestage töölehe nimi lahtrisse **Töölehe nimi**.
6.  Korrake etappe 3 kuni 5 iga aruandlusüksuse puhul, mis peaks aruandest andmeid saama. Aruandes valede andmete kuvamise vältimiseks veenduge, et aruandluspuu asjakohases üksuses kuvatakse õige aruande nimed.

## <a name="examples"></a>Näited
### <a name="reporting-unit-structure--example-1"></a>Aruandlusüksuse struktuur – näide 1

Siin on aruandlusüksuse struktuur järgmises aruandluspuus.

-   Aruandlusüksus Contoso Japan on tütarüksuste Contoso Japan Sales ja Contoso Japan Consulting emaüksus.
-   Üksus Contoso Japan Sales on üksuse Contoso Japan tütarüksus ja üksuste Home Sales ja Auto Sales emaüksus.
-   Madalaima taseme üksikasjade aruandlusüksused (Home Sales, Auto Sales, Client Services ja Operations) kajastavad finantsandmete osakondi. Need aruandlusüksused on diagrammi varjutatud alas.
-   Kõrgema taseme kokkuvõtte üksused esitavad üksikasjade üksuste teabe kokkuvõtte.

[![ContosoEntertainmentSummaryReportStructure](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Aruandlusüksuse struktuur – näide 2

Järgmisel diagrammil on aruandluspuul ettevõtte funktsiooni järgi jaotatud organisatsiooni struktuur. [![summaryofallunitscontoso](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Näide aruandlusüksuste sisestamise kohta dimensioonide dialoogiboksist

Järgmisel illustratsioonil on dialoogiboksi **Sisesta aruandlusüksused dimensioonidest** näide. Selles näites annavad tulemused äriüksuste, kulukeskuste ja osakondade kombinatsiooni. [![InsertReportingUnits](./media/insertreportingunits.png)](./media/insertreportingunits.png) Saadud aruandluspuu definitsiooni sorditakse äriüksuse, siis kulukeskuse ja siis osakonna järgi. Viienda aruandlusüksuse dimensioon on **Äriüksus = \[001\], Kulukeskus = \[\], Osakond = \[022\]** ja tähistab äriüksuse 001 osakonda 022 puudutavate kontode aruandlusüksust. [![ReportingTree](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Andmete koondamise näited

Järgmistes näidetes on võimalik teave, mida koondatavate andmete aruandluspuu definitsioonis kasutatakse.

#### <a name="example-1"></a>Näide 1

[![MutliCompanyRollUp](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Näide 2

[![CrossCompanyDepartmentRollUp](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

# <a name="see-also"></a>Vt ka

[Finantsaruandlus](financial-reporting-intro.md)




