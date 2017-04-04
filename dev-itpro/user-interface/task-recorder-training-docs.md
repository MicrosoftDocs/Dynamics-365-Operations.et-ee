---
title: "Dokumentide või koolituse loomine tegevuse salvestiste abil"
description: "See teema selgitab, kuidas ülesanne recorder ja ülesandeks juhendid, kuidas luua tööülesande salvestisi ja kohandamine Microsoft ülesandeks juhendid ning lisab need teie abi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Dokumentide või koolituse loomine tegevuse salvestiste abil
See teema selgitab, kuidas ülesanne recorder ja ülesandeks juhendid, kuidas luua tööülesande salvestisi ja kohandamine Microsoft ülesandeks juhendid ning lisab need teie abi.

<a name="learn-about-task-recorder"></a>Teave tegevuse salvestaja kohta
-------------------------

Ülesanne recorder on Microsoft Dynamics 365 toimingute vahend, mille abil saate salvestada toiminguid, mida te võtate toote kasutajaliidese (UI). Tegevuse salvestaja kasutamisel jäädvustatakse kõik sündmused, mida kasutajaliideses teete ja mis serveri suhtes käivitatakse, sh väärtuste lisamine, sätete muutmine ja andmete eemaldamine. Salvestatud toiminguid nimetatakse ühiselt *tegevuse salvestiseks*. Tegevuse salvestisi saab kasutada mitmesugusel moel.

-   **Tegevuse salvestisi saab esitada tegevuse juhistena.** Ülesanne on toimingud aitavad kogemusi Dynamics 365 lahutamatu osa. Ülesande juhend on kontrollitud, giidiga, interaktiivne kogemus läbi äriprotsessi. Kasutajal palutakse läbida iga etapp hüpikviiba (ehk mulli) abil, mis liigub läbi kasutajaliidese ja osutab kasutajaliidese elemendile, millega kasutaja peaks suhtlema. "Mull" kirjeldab ka suhelda elementi, nagu "Click here" või "Sellele väljale Sisestage väärtus." Ülesande juhend töötab vastu kasutaja praeguse kogumi ja sisestatud andmed salvestatakse kasutaja keskkonnas.
-   **Ülesanne salvestisi võib kuvada spikripaani menetlustoiminguid.** Saate otsida ja kuvada ülesande salvestisi spikripaani. Pääsete paani spikker klõpsates selle **?** Ikooni peal navigeerimisribal või kasutada kiirklahvi kombinatsioon, **Ctrl + Shift +?**. Lugege juhiseid salvestamise spikripaani ülesande või saate valida, kas mängida salvestus ülesande juhend, et UI kasutatakse.
-   **Tegevuse salvestised saab BPM-i salvestada.** Saate salvestada oma tegevuse salvestise hierarhia reale äriprotsessi modelleerija (BPM-i) teegis teenuses Lifecycle Services (LCS). Salvestisest luuakse toimingute loend ja äriprotsessi voodiagramm. Ülesanne salvestisi, BPM teeki salvestatud saab näidata Dynamics 365 toiminguteks nagu aidata.
-   **Tegevuse salvestised saab salvestada Wordi dokumentidena.** See võimaldab hõlpsasti prinditavaid koolitusjuhendeid koostada.

Saate luua oma ülesande salvestiste, mängida ülesanne salvestisi Microsofti või Microsofti lisatud ülesande salvestisi kajastada oma konfiguratsiooni muuta. Ülesanne salvesti kohta lisateabe saamiseks vaadake [ülesande salvesti Dynamics 365 operatsioonide](task-recorder.md).

## <a name="plan-your-task-recording"></a>Tegevuse salvestaja plaanimine
Kui loote uut tegevuse salvestust või tuginete oma salvestise puhul Microsofti tegevuse salvestisele, pidage meeles järgmist.

-   Plaanige oma salvestist sarnaselt videole. Tehke kõik otsused aegsasti.
-   Läbige äriprotsess vähemalt üks kord ilma seda salvestamata, et toimingutest aru saada.
-   Kui protsessis liigute, siis pange enne salvestamist tähele, kus kasutate kiirklahve või klahvi **Enter**, et saaksite nende kasutamist tegeliku salvestamise ajal vältida.
-   Tuvastage järgmine.
    -   Kas soovite grupeerida toimingud alamtegevusteks? Alamtegevused eraldavad visuaalselt protsessi osi. Näiteks kui loote salvestist toimingust Toote loomine ja väljastamine, võib olla vaja grupeerida toimingud, mida on vaja toote loomiseks, ja seejärel grupeerida toimingud, mida on vaja toote väljastamiseks. Alamtoimingud muudavad ka pikkade protsesside lugemise hõlpsamaks.
    -   Kas soovite lisada marginaale ja kui soovite, siis kuhu? Vt lisateavet allolevast jaotisest Erinevad marginaalide tüübid.
    -   Millised väärtused lisate erinevatele väljadele, kui äriprotsessi toiminguid teete? On hea teada, mida jätkates valida või sisestada, et salvestamise ajal ei peaks tagasi minema ega vigu parandama.

**Kirjutage oma kirjeldus ja marginaalid aegsasti valmis**

-   Iga tegevuse salvestise alguses on kirjelduse väli, kuhu saab sisestada salvestise tutvustuse. Kirjeldus tasub kirjutada ja salvestada aegsasti eraldi dokumenti, et saaksite selle salvestamise ajal kopeerida ja tegevuse salvestisse kleepida. Sel viisil saate teksti viimistlemiseks aega võtta, kui te parajasti salvestamisega ei tegele. Teksti lõikamine ja kleepimine muudab salvestusprotsessi kiiremaks ja sujuvamaks.
-   Iga tegevuse salvestamise toimingu ajal saate marginaale koostada. Tegevuse juhise taasesitamise ajal kuvatakse marginaalid „mullis” toimingu teksti kohal või all. Kui vaadata spikripaani tekstina kuvatakse teksti sees sammus marginaalid. Nagu kirjelduste puhul, tasub marginaalid eraldi dokumenti kirjutada ja salvestada. Tegevuse salvestise salvestamise ajal saate marginaale sellest dokumendist lõigata ja kleepida.

**Erinevad marginaalide tüübid** Kõik marginaalid on valikulised. Lisage need ainult siis, kui nad annavad kasutajale kasulikku teavet.

-   **Jaotise**: jaotise Märkus ilmub enne samm teksti ülesandeid salvesti automaatselt loob. Saatekavas ülesanne automaatselt loodud teksti kohal kuvatakse jaotise Märkus. Kasutage seda tüüpi marginaali selgitamiseks, miks kasutaja seda toimingut teeb, või täiendava konteksti pakkumiseks.

See on redigeerimispaan, mida marginaali lisamisel näete, kui oma salvestist teete. Sisestage marginaali pealkiri väljale **Pealkiri**. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Selline näeb välja marginaali pealkiri tegevusjuhises mullina. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **Märkmed.** Märkmete marginaal kuvatakse pärast toimingu teksti, mille tegevuse salvestaja automaatselt loob. Tegevuse juhises on see nähtav ainult juhul, kui kasutaja klõpsab linki **Kuva rohkem** ülesande juhise mullis. Kasutage seda tüüpi marginaali millegi kirjeldamiseks, mida kasutajal on toimingu tegemiseks vaja teada.

See on redigeerimispaan, mida marginaali lisamisel näete, kui oma salvestist teete. Sisestage marginaali märkused väljale **Märkused**. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

See on märkmeid marginaali näeb "mull" ülesande juhend.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Info samm**: need marginaalid on loodud hiire parema nupu klõpsuga vormi juhtelemente või kusagil &lt;**ülesande recorder**&lt; ** lisa info samm. ** Info sammud kuvatakse nummerdatud sammuna mingil hetkel abil lisada, kuigi midagi registreeriti UI. Saate lisada vormi-taseme teabeetapi või juhtelemendiga seotud teabeetapi. Kui teabeetapp on vormiga seotud, ilmub vormile tegevuse juhise esitamisel tegevuse juhise „mull” ilma kursorita. Kui info samm on seotud juhtelemendile, osutab ülesande juhend "mull" kontrolli kui ülesande juhend on mänginud. Paanil Spikker kuvatakse info samm kommentaari nummerdatud sammuna sisestatud mis tahes tekstiga. Info juhiste abil saate valmistada ette järgmised sammud kasutajalt samme, mis tuleb teha väljaspool Dynamics 365 operatsioonide või viidata teistele salvestustele (kuigi te ei saa luua hyperinks marginaalid.) kirjeldamiseks.

**Määrake, kui pika salvestise teete**

-   Kasutaja tavaliselt loeb salvestist või esitab selle algusest lõpuni, seega ärge kombineerige etappe või toiminguid, mida on parem teha eraldi.
-   Püüdke mitte salvestada pikka stsenaariumi, mis hõlmab mitut alamprotsessi. Näiteks toiming Poe klienditeenuse laua kasutamine on liiga lai; jagage see lühemateks toiminguteks nagu Tagastuste aktsepteerimine ja Kinkekaardile lisamine.
-   Kui tegevust saab teha mitme äriprotsessi raames, looge sellele eraldi salvestis ja saate sellele teistes salvestistes viidata.
-   Kui protsess hõlmab mitut tegevust, mida inimene tõenäoliselt korraga teeb, võite hoida tegevusi ühes salvestises, nt Funktsiooniprofiilide seadistamine ja määramine.
-   Kui see on midagi sellist, mida tehakse üks kord (nt konfigureerimine) ja siis tehakse kohe teine tegevus, mida võidakse teha korduvalt ja eraldi, eraldage need kaheks tegevuse salvestiseks.

**Otsustada, kuhu UI salvestamist alustama** leht, et te olete tööülesande salvestamine andmete salvestamise alustamisel mõjutab kus ülesande juhend kuvatakse lehekülg. Näiteks kui soovite, kui kasutaja klõpsab aidata pearaamatu parameetrite lehel loetletud spikripaani salvestust ülesanne, tuleb alustada salvestust lehel pearaamatu parameetrid. **Salvestiste salvestamine axtr-failidena** Kui olete tegevuse salvestise loomise või redigeerimise lõpetanud, kuvatakse teile mitu valikut salvestise allalaadimiseks või salvestamiseks. Saate laadida failid alla tegevuse salvestise paketina (.axtr), laadida need alla töötlemata salvestise failina (.xml), Wordi dokumendina või salvestada faili LCS-i teeki. On soovitatav salvestada tegevuse salvestis alati tegevuse salvestise paketifailina (.axtr). See aitab faili hõlpsamini hallata, kui hiljem peaks olema vaja protseduure või marginaale muuta. Kui soovite laadida faili alla Wordi dokumendina, salvestage see samuti tegevuse salvestise paketifailina.

## <a name="create-your-task-recording"></a>Tegevuse salvestise loomine
Üksikasjalikud walk-through kohta leiate [loomise ülesanne salvestis](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsofti tegevuse salvestiste kopeerimine ja kohandamine
Saate alla laadida ja muuta Microsofti ülesanne salvestisi kasutada neid oma dokumentatsiooni või koolitusmaterjalid. Microsofti tegevuse salvestise allalaadimiseks tehke järgmist.

1.  Dynamics 365 toiminguteks, avage ülesande salvesti. Tegevuse salvestaja asub menüüs **Sätted**.
2.  Klõpsake tegevuse salvestaja paanil valikut **Salvestise haldamine.**
3.  Jaotises **Kus salvestis asub** klõpsake valikut **See on LCS-i teegis**.
4.  Klõpsake valikut **LCS-i teegi valimine**.
5.  Valige Microsoft global Raamatukogu.
6.  Valige puult äriprotsessi teegi sõlm, millega tegevuse salvestis on seotud.
7.  Klõpsake nupul **OK**.
8.  Klõpsake käsku **Käivita**.
9.  Sel hetkel liikuda salvestamine, muutmine tarvitusele lähete uuesti salvestamiseks. **Märkus**: kui teil on vaja ainult muuta salvestuse teksti, saate avada kandmist **muuta salvestuse 's marginaalid** režiim, ja seejärel salvestage see.
10. Kui salvestis on lõpuni mänginud, klõpsake ekraani ülaosas tegevuse salvestaja ribal nuppu **Peata**.
11. Valige, kuidas tegevuse salvestist salvestada soovite.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Sisaldab salvestised ülesanne paanil Spikker
Näita oma kohandatud salvestiste paanil Spikker, et nad saaksid esitada ülesandeks juhendid või tekstina vaadata, salvestised ülesanne BPM teeki salvestada ja seejärel värskendage teie abi süsteemi parameetrid punkti BPM teeki. Lisateabe saamiseks vaadake [ühendada spikrisüsteemi.](../get-started/help-connect.md)

<a name="see-also"></a>Vt ka
--------

[Dynamics 365 operatsioonide aidata](..\get-started\help-overview.md)

[Ühenduse abi](..\get-started\help-connect.md)

[Ülesanne salvesti Dynamics 365 toiminguteks](task-recorder.md)

[Hiljuti lisatud ülesande salvesti funktsioonid](\core\get-started\recently-added-editing-features-in-task-recorder)

[Uus koolitus raamatukogude loomise Dynamics AX jooksul elutsükli teenuste kasutamise lindistaja ülesanne (External link)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Loo rikas spikriteemasid ülesanne Recorder (väline link)](https://mbspartner.microsoft.com/AX/Videos/970)


