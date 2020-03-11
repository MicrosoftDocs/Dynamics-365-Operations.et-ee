---
title: Pakkematerjalid ja tasud
description: Selles teemas leiate teavet pakkematerjalide tasude kohta, mida makstakse kindla ajavahemiku järel jäätmekäitlusfirmadele.
author: MarkusFogelberg
manager: AnnBe
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2351cce9dc6e1a554800817f75591c4a4e24d43
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076243"
---
# <a name="packing-materials-and-fees"></a>Pakkematerjalid ja tasud

[!include [banner](../includes/banner.md)]

Pakkematerjalitasud makstakse jäätmekäitlusfirmale kindlate ajavahemike kaupa. Iga materjali eest, millest pakkimisühik koosneb, tuleb maksta summa kaaluühiku kohta. Olgugi pakkematerjalitasud arvutatakse ja esitatakse, siis ühtegi pearaamatukannet ei sisestata, sest neid tasusid ei loeta riigile makstavateks maksudeks.

Pakkematerjalide kaalud ja tasud arvutatakse müügi- ja ostutellimuste ridade jaoks.

Saate määratleda ühele kaubale, kaubagrupile (pakkimisgrupile) või kõikidele kaupadele vähemalt ühe pakkimisühiku. Pakkimisühik koosneb pakkematerjalidest, nende kaaludest ja pakkimisühikus sisalduvate kaupade arvust. Igale määratletud pakkematerjali tüübile määratakse pakkematerjali kood. Pakkematerjali koodi alusel saate määrata hinna kindlaks perioodiks. Pakkematerjali tasu arvutatakse selle teabe alusel.

> [!NOTE]
> Juhul, kui teie ettevõte ei maksa pakkematerjalitasu, saate seda funktsiooni kasutada pakkematerjalide kaalu statistika arvutamiseks.

## <a name="allocations"></a>Pakkematerjali eraldamise seadistamine

Enne pakkematerjali kaalu, pakkematerjali tasude või mõlema arvutamist peate arvutuse sisse lülitama ja määratlema, milliseid materjale ja tasusid millistele kaupadele rakendada.

1. Avage **Varude haldus \> Seadistus \> Varude ja laohalduse parameetrid**.
1. Vahekaardil **Üldine** jaotises **Pakkematerjal** määrake suvand **Arvuta pakkematerjali tasud** valikule **Jah**.
1. Avage **Varude haldus \> Seadistus \> Pakkematerjal \> Pakkimisgrupid** ja looge kõik pakkimisgrupid, mida kasutate. Kõik pakkimisgrupi kaubad kasutavad sama pakkematerjali eraldamist. Kui te pakkimisgruppe ei kasuta, võite selle sammu vahele jätta.

    > [!TIP]
    > Pärast pakkimisgruppide loomist saate igale tootele määrata vastavalt vajadusele grupi. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**, valige toode ja seejärel kiirkaardil **Varude haldus** väljal **Pakkimisgrupp** valige sobiv pakkimisgrupp.

1. Avage **Varude haldus \> Seadistu \> Pakkematerjal \> Pakkematerjali koodid**, määratlege iga pakkematerjali tüüp, mida kasutate, ja määratlege saadetiste ettevalmistamisel kasutatava pakkematerjali ühik.
1. Avage **Varude haldus \> Seadistus \> Pakkematerjal \> Pakkematerjali tasud** ja määrake iga just määratletud pakkematerjali tüübi tasu. Tasud arvutatakse tarbitud ühiku hinna alusel.
1. Pakkematerjali üksustele eraldamiseks avage **Varude haldus \> Seadistus \> Pakkematerjal \> Pakkematerjali eraldamine** ja looge eraldamised. Saate luua nii palju eraldamisi kui vaja. Saate eraldada pakkematerjalid üksikutele kaupadele, kaubagruppidele (pakendigrupid) või kõikidele kaupadele, olenevalt sellest, kuidas teie eraldamised peaksid olema.

    Kõikide loodavate eralduse puhul toimige järgmiselt.

    1. Määrake kiirkaardil **Üldine** järgmised väljad.

        - **Kaubakood** – valige eraldamise ulatus.

            - **Tabel** – looge ühe kindla kauba eraldamine.
            - **Grupp** – looge eraldamine kõikidele üksustele, mis kuuluvad pakendigruppi, mis on määratletud lehel **Pakendigrupid**.
            - **Kõik** – looge eraldamine kõikidele kaupadele.

            > [!NOTE]
            > Tavaliselt peaksite tegema kõik oma eraldanised samal tasemel (**Tabel**, **Grupp** või **Kõik**). Kui kasutate rohkem kui ühte taset, kasutatakse iga kauba puhul kõige täpsemat ühtivat eraldamist. (Tase **Tabel** on tasemest **Grupp** tähtsam ja mõlemad tasemed on tähtsamad kui tase **Kõik**.)

        - **Kauba seos** – kui eraldate ühe kauba jaoks, valige kaup. Kui eraldate kaubagrupi jaoks, valige pakkimisgrupp. Kui eraldate kõikide kaupade jaoks, jätke see väli tühjaks.
        - **Konfiguratsioon**, **Suurus**, **Värv** ja **Stiil** – sisestage nende dimensioonide väärtused vastavalt vajadusele, et veelgi täpsustada kaupa, mille jaoks eraldate.
        - **Pakkimisühik** – valik ühik, mille sisse kaubad pakkematerjali kasutamisel pakendatakse. See ühik võib erineda ühikust, mille sees kaup osteti ja hoiustati.
        - **Pakkimisühiku tegur** – sisestage teisendustegur, mida kasutatakse varude ühikust pakkimisühikusse teisendamiseks. (Teisendus kasutab valemit *Pakkimisühikud* = *Kauba ühikud* × *Pakkimisühiku faktor*.)

    1. Lisage kiirkaardil **Pakkimismaterjal** rida iga pakkimismaterjali tüki jaoks, mis on vajalik praeguse eraldamise jaoks. Määrake igal real materjali tüüp (nagu on määratletud lehel **Pakkematerjali koodid**) ja selle summa, mida kasutatakse praeguse kauba iga saadetava ühiku kohta.

## <a name="packing-units-on-sales-order-lines"></a>Pakkimisühikud müügitellimuse ridadel

Pärast seda, kui olete [pakkematerjali tasude arvutuse sisse lülitanud seadistanud eraldamised](#allocations), kinnitab süsteem, et pakkimisühikud on määratud igale müügitellimusse lisatud kaubale. Seejärel arvutab see kõik vajalikud tasud. Kui kaup lisatakse müügitellimusele, leiab aset üks järgmistest sammudest.

- **Kui kaubale kehtib pakkimise eraldamine:** süsteem uuendab müügitellimuse rida automaatselt koos määratud pakkimisühikuga ja pakkimisühiku kogusega. (Pakkimisühiku kogus arvutatakse automaatselt, kasutades valemit *pakkimisühiku kogus* = *tellitud kogus* ÷ *kaupade arv valitud pakkimisühikus*.)
- **Kui kaubale ei kehti pakkimise eraldamist:** saate pakkimisühiku ja pakkimisühiku koguse müügitellimuse reale käsitsi sisestada.

Pakkimisühikut ja pakkimisühiku kogust saab ka müügitellimuse rea sisestamisel muuta. See võimalus on asjakohane, kui müügitellimuse rida tarnitakse või arveldatakse vaid osaliselt.

Müügitellimuse eest arve esitamisel loob süsteem pakkematerjali kanded. Pakkematerjali kanded sisaldavad müügirea pakkematerjali kaalusid. Pärast nende eest arve esitamist saate kandeid muuta. Seejärel saate luua uued tehingud.

## <a name="packing-units-on-purchase-order-lines"></a>Pakkimisühikud ostutellimuse ridadel

Süsteem ei loo pakkematerjali kandeid müügitellimuse ridade jaoks. Selle asemel loote arveldatud ostutellimuse ridade kanded lehel **Pakkematerjali kanded**.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Litsentsinumbrite seadistamine klientidele, kellelt küsitakse pakkimismaterjali eest tasu

Kui kindla kliendi müügitellimused peaksid sisaldama iga tellimuse jaoks kasutatavate pakkematerjalide tasusid, toimige järgmiselt.

1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Valige klient, kellelt peaks pakkematerjalide eest tasu küsima.
1. Määrake kiirkaardil **Arve ja tarne** järgmised väljad.

    - Jaotises **Käibemaks** väljal **Pakendimaksu litsentsi number** sisestage ettevõtte litsentsi number.
    - Jaotises **Pakkematerjali tasu** väljal **Litsentsi number** sisestage ettevõtte litsentsi number.

Nüüd, kui loote ja väljastate arve müügitellimuse eest, mis sisaldab ühte või mitut pakkematerjali kasutavat kaupa, on arvel toodud pakkematerjali tasud.

Klientide jaoks, kes ei pea pakkematerjali tasusid maksma, järgige neid samu samme, kuid kustutage litsentsi numbrid väljadelt **Pakendimaksu litsentsi number** ja **Litsentsi number**. Nende klientide arved, kes ei pakkematerjali eest ei maksa, näitavad pakkematerjalide kaalu, kuid ei näita tasusid.

Aruande loomiseks, mis näitab kõiki pakkematerjali tasusid, mida teie ettevõte kindla perioodi eest võlgneb, avage **Varude haldus \> Päringud ja aruanded \> Pakkematerjali aruanded \> Pakkematerjali tasu arvutamine**, määrake kuupäevavahemik ja seejärel valige **OK**.

## <a name="print-packing-material-weights-on-invoices"></a>Pakkematerjalide kaalu printimine arvetele

Saate printida arvele pakkematerjali kaalu ja näidata, kes maksab seotud tasud. Kaalud summeeritakse pakkimiskoodi järgi.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
1. Vahekaardil **Uuendused** kiirkaardil **Arve** määrake suvand **Pakkematerjali kaalu printimine** valikule **Jah**.
