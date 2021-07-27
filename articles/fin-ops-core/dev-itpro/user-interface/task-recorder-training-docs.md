---
title: Dokumentide või koolituse loomine tegevuse salvestaja abil
description: See teema selgitab, mis asjad on tegevuse salvestaja ja tegevuse juhised, kuidas luua salvestisi ja kuidas kohandada Microsoft tegevuse juhiseid ja kaasata neid oma spikrisse.
author: josaw1
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2bc5aa1080709931b3aa71c548a7bf2fb9b1192
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354289"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Dokumentide või koolituse loomine tegevuse salvestaja abil

[!include [banner](../includes/banner.md)]

See teema selgitab, mis asjad on tegevuse salvestaja ja tegevuse juhised, kuidas luua tegevuse salvestisi ja kuidas kohandada Microsoft tegevuse juhiseid ja kaasata neid oma spikrisse.

> [!IMPORTANT]
> Saate salvestada oma rakenduse Dynamics 365 Human Resources tegevusjuhised, kuid ei saa neid praegu äriprotsesside modelleerija (BPM) teeki salvestada ega neid paanilt Spikker avada. Saate need lokaalselt või võrgukohta salvestada ning seejärel neid tegevuse salvestajaga avada ja esitada. 

## <a name="learn-about-task-recorder"></a>Teave tegevuse salvestaja kohta

Tegevuse salvestaja on tööriist, mille abil saab salvestada toote kasutajaliideses tehtavaid toiminguid. Tegevuse salvestaja kasutamisel jäädvustatakse kõik sündmused, mida kasutajaliideses teete ja mis serveri suhtes käivitatakse, sh väärtuste lisamine, sätete muutmine ja andmete eemaldamine. Salvestatud toiminguid nimetatakse ühiselt *tegevuse salvestiseks*. Tegevuse salvestisi saab kasutada mitmesugusel moel.

-   **Tegevuse salvestisi saab esitada tegevuse juhistena.** Tegevusjuhised on spikri kasutuskogemuse lahutamatu osa. Tegevuse juhis on kontrollitud, juhendatud, interaktiivne kogemus, mis juhib teid äriprotsessi etappides. Kasutajal palutakse läbida iga etapp hüpikviiba (ehk mulli) abil, mis liigub läbi kasutajaliidese ja osutab kasutajaliidese elemendile, millega kasutaja peaks suhtlema. „Mull” annab ka teavet selle kohta, kuidas suhelda elemendiga, nagu „Klõpsake siin” või „Sisestage sellele väljale väärtus”. Tegevuse juhis käitatakse kasutaja praeguse andmekogumi suhtes ja sisestatud andmed salvestatakse kasutaja keskkonda.
-   **Tegevuse salvestised saab salvestada Wordi dokumentidena.** See võimaldab hõlpsasti prinditavaid koolitusjuhendeid koostada.

Saate luua oma tegevuse salvestisi, esitada Microsofti pakutavaid tegevuse salvestisi või muuta Microsofti pakutavaid tegevuse salvestisi teie konfiguratsiooni kajastamiseks. Lisateavet tegevuse salvestaja kohta vt teemast [Tegevuse salvestaja](task-recorder.md).

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
-   Iga tegevuse salvestamise toimingu ajal saate marginaale koostada. Tegevuse juhise taasesitamise ajal kuvatakse marginaalid „mullis” toimingu teksti kohal või all. Kui vaadata marginaale spikripaanil tekstina, kuvatakse need toimingu sees tekstina. Nagu kirjelduste puhul, tasub marginaalid eraldi dokumenti kirjutada ja salvestada. Tegevuse salvestise salvestamise ajal saate marginaale sellest dokumendist lõigata ja kleepida.

**Erinevad marginaalide tüübid** Kõik marginaalid on valikulised. Lisage need ainult siis, kui nad annavad kasutajale kasulikku teavet.

-   **Pealkiri**: pealkirja marginaal kuvatakse enne toimingu teksti, mille tegevuse salvestaja automaatselt loob. Tegevuse juhises ilmub automaatselt loodud teksti kohal pealkirja marginaal. Kasutage seda tüüpi marginaali selgitamiseks, miks kasutaja seda toimingut teeb, või täiendava konteksti pakkumiseks.

See on redigeerimispaan, mida marginaali lisamisel näete, kui oma salvestist teete. Sisestage marginaali pealkiri väljale **Pealkiri**. 

[![Pealkirja marginaaliga redigeerimispaan.](./media/screen1.png)](./media/screen1.png) 

Selline näeb välja marginaali pealkiri tegevusjuhises mullina. 

[![Pealkirja marginaali ilme tegevuse juhises.](./media/screen2.png)](./media/screen2.png)

-   **Märkmed.** Märkmete marginaal kuvatakse pärast toimingu teksti, mille tegevuse salvestaja automaatselt loob. Tegevuse juhises on see nähtav ainult juhul, kui kasutaja klõpsab linki **Kuva rohkem** ülesande juhise mullis. Kasutage seda tüüpi marginaali millegi kirjeldamiseks, mida kasutajal on toimingu tegemiseks vaja teada.

See on redigeerimispaan, mida marginaali lisamisel näete, kui oma salvestist teete. Sisestage marginaali märkused väljale **Märkused**. 

[![Redigeerimispaan marginaaliga väljal Märkused.](./media/screen3.png)](./media/screen3.png) 

Selline näeb välja märkuste marginaal tegevusjuhises mullina.

[![Märkuste marginaali ilme tegevuse juhises.](./media/screen4.png)](./media/screen4.png)

-   **Teabeetapp**: nende marginaalide loomiseks paremklõpsake juhtelemendil või kõikjal vormis &lt; **Tegevuse salvestaja** &lt; **Lisa teabeetapp**. Teabeetapid kuvatakse nummerdatud etapina igas punktis, kuhu selle sisestate, isegi kui kasutajaliideses ei salvestatud ühtki tegevust. Saate lisada vormi-taseme teabeetapi või juhtelemendiga seotud teabeetapi. Kui teabeetapp on vormiga seotud, ilmub vormile tegevuse juhise esitamisel tegevuse juhise „mull” ilma kursorita. Kui teabeetapp on seotud juhtelemendiga, osutab tegevuse juhise „mull” tegevuse juhise esitamisel juhtelemendina. Spikripaanil kuvatakse teabeetapi mis tahes sisestatud tekstiga marginaal nummerdatud etapina. Kasutage teabeetappe kasutaja ettevalmistamiseks järgmisteks toiminguteks, väljaspool rakendust tehtavate toimingute kirjeldamiseks või teistele salvestistele viitamiseks (kuigi marginaalides ei saa hüperlinke luua).

**Määrake, kui pika salvestise teete**

-   Kasutaja tavaliselt loeb salvestist või esitab selle algusest lõpuni, seega ärge kombineerige etappe või toiminguid, mida on parem teha eraldi.
-   Püüdke mitte salvestada pikka stsenaariumi, mis hõlmab mitut alamprotsessi. Näiteks toiming Poe klienditeenuse laua kasutamine on liiga lai; jagage see lühemateks toiminguteks nagu Tagastuste aktsepteerimine ja Kinkekaardile lisamine.
-   Kui tegevust saab teha mitme äriprotsessi raames, looge sellele eraldi salvestis ja saate sellele teistes salvestistes viidata.
-   Kui protsess hõlmab mitut tegevust, mida inimene tõenäoliselt korraga teeb, võite hoida tegevusi ühes salvestises, nt Funktsiooniprofiilide seadistamine ja määramine.
-   Kui see on midagi sellist, mida tehakse üks kord (nt konfigureerimine) ja siis tehakse kohe teine tegevus, mida võidakse teha korduvalt ja eraldi, eraldage need kaheks tegevuse salvestiseks.

**Otsustage, kust kasutajaliideses salvestamist alustada** Lehekülg, millel tegevuse salvestise salvestamise käivitamisel asute, mõjutab seda, millisel lehekülje jaoks tegevuse juhis kuvatakse. Näiteks kui soovite, et teie tegevuse salvestis oleks loetletud spikripaanil, kui kasutaja klõpsab lehel Pearaamatu parameetrid spikrit, tuleb alustada salvestamist lehelt Pearaamatu parameetrid. **Salvestiste salvestamine axtr-failidena** Kui olete tegevuse salvestise loomise või redigeerimise lõpetanud, kuvatakse teile mitu valikut salvestise allalaadimiseks või salvestamiseks. Saate laadida failid alla tegevuse salvestise paketina (.axtr), laadida need alla töötlemata salvestise failina (.xml), Wordi dokumendina või salvestada faili LCS-i teeki. On soovitatav salvestada tegevuse salvestis alati tegevuse salvestise paketifailina (.axtr). See aitab faili hõlpsamini hallata, kui hiljem peaks olema vaja protseduure või marginaale muuta. Kui soovite laadida faili alla Wordi dokumendina, salvestage see samuti tegevuse salvestise paketifailina.

## <a name="create-your-task-recording"></a>Tegevuse salvestise loomine
Üksikasjalikud protsessijuhised leiate jaotisest [Tegevuse salvestaja ressursid](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Microsofti tegevuse salvestiste kopeerimine ja kohandamine
Saate Microsofti tegevuse salvestised alla laadida ja neid redigeerida, et kasutada neid oma spikridokumentides või koolitusmaterjalides. Microsofti tegevuse salvestise allalaadimiseks tehke järgmist.

1.  Avage tegevuse salvestaja. Tegevuse salvestaja asub menüüs **Sätted**.
2.  Klõpsake tegevuse salvestaja paanil valikut **Salvestise haldamine.**
3.  Jaotises **Kus salvestis asub** klõpsake valikut **See on LCS-i teegis**.
4.  Klõpsake valikut **LCS-i teegi valimine**.
5.  Valige Microsofti globaalne teek.
6.  Valige puult äriprotsessi teegi sõlm, millega tegevuse salvestis on seotud.
7.  Klõpsake nupul **OK**.
8.  Klõpsake käsku **Käivita**.
9.  Sellel hetkel kerige salvestis läbi, muutes liikudes mis tahes etappe, et see uuesti salvestada. **Märkus**. Kui peate muutma ainult salvestise teksti, saate salvestise avada režiimis **Salvestise marginaalide redigeerimine** ja selle seejärel salvestada.
10. Kui salvestis on lõpuni mänginud, klõpsake ekraani ülaosas tegevuse salvestaja ribal nuppu **Peata**.
11. Valige, kuidas tegevuse salvestist salvestada soovite.



## <a name="additional-resources"></a>Lisaressursid

[Spikrisüsteem](../../fin-ops/get-started/help-overview.md)

[Spikrisüsteemi ühendamine](../../fin-ops/get-started/help-connect.md)

[Tegevuse salvestaja](task-recorder.md)

[Tegevuse salvestajaga Richi spikriteemade loomine (väline link)](https://mbspartner.microsoft.com/AX/Videos/970)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]