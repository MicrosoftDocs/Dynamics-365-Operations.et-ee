---
title: "Tasakaalustuse ülevaade"
description: "Selles artiklis antakse üldist teavet tasakaalustamisprotsessi kohta. See kirjeldab kannete tüüpe, mida saab tasakaalustada, seda, millal ja kuidas kandeid saab tasakaalustada, ja tasakaalustusprotsessi tulemusi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: adbfa6f99c481129e8cbf4a2dc4b23b4be1e8b34
ms.lasthandoff: 03/31/2017


---

# <a name="settlement-overview"></a>Tasakaalustuse ülevaade

Selles artiklis antakse üldist teavet tasakaalustamisprotsessi kohta. See kirjeldab kannete tüüpe, mida saab tasakaalustada, seda, millal ja kuidas kandeid saab tasakaalustada, ja tasakaalustusprotsessi tulemusi.

Tasakaalustuse ajal rakendatakse ühe dokumendi kanded teise dokumendi kannetele, et suurendada või vähendada kummagi dokumendi saldot. Näiteks saab rakendada makse arve. Erinevate tehingutüüpide lõikes saate tasakaalustada eri aegadel ja erinevate meetodite abil. Tasakaalustus võib põhjustada ka uute kannete loomist.

## <a name="what-transactions-can-be-settled"></a>Milliseid kandeid saab tasakaalustada?
Ostureskontro ja müügireskontro tasakaalustus võib toimuda mis tahes kandetüüpide vahel, mis mõjutavad hankija saldot või kliendi saldot, nagu arved, maksed, kreeditarved ja tasud. Iga kandetüübi saab tasakaalustada teise kandetüübi suhtes. Näiteks saate tasakaalustada makse arve suhtes, kreeditarve arve suhtes, ühe arve teise arve suhtes ja ühe makse teise makse suhtes. Saate tasakaalustada makseid samas juriidilises isikus või teises juriidilises isikus olevate kannete suhtes. Kasutada tsentraliseeritud makse mudel [keskne maksete](set-up-centralized-payments.md) aitab lihtsustada maksetoimingute.

## <a name="when-to-settle-transactions"></a>Millal kandeid tasakaalustada?
Kandeid saab tasakaalustada makse sisestamise ajal. Näiteks kui teete makse hankijale, valite tavaliselt makstavad arved. Kui valite arve, te märgite need makse tasakaalustamine. Kui Müügireskontro makse ametnikud kirjendate kliendimakse, nad kaubamärgi korral arvete tasakaalustamiseks, põhineb teabel, mis sisaldub kliendi maksekorralduse. Makseid saab tasakaalustamiseks märkida lehel **Kannete tasakaalustamine**. Selle lehe saate avada mis tahes sisestamata arvelt või makselt. Kande sisestamisel sisestatakse ka tasakaalustus. Kandeid saab tasakaalustada ka pärast sisestamist. Saate sisestada kliendimakse ilma seda arvete suhtes tasakaalustamata. Siiski peate võib-olla esmalt uurima, kas makse on õige arve suhtes tasakaalustatud. Lehe **Kannete tasakaalustamine** saab avada lehelt **Kõik kliendid** või **Kõik hankijad** või mis tahes kliendi või hankija lehelt **Kanded**. Samuti saate arve jaoks sisestatud ettemakseid reserveerida, märkides makse ostutellimuse või müügitellimuse suhtes tasakaalustamiseks. Sel juhul makse on veel avatud saldot, kuid see ei ole võimalik lahendada teise faktuurarve. Makse tuleb vastu on loodud ostu- või müügitellimuse arve automaatselt lahendada.

## <a name="how-to-settle-transactions"></a>Kuidas kandeid tasakaalustada?
Kandeid saab tasakaalustada käsitsi, automaatselt või kaht meetodit kombineerides. Tasakaalustusmeetodi valik sõltub äriprotsessidest, mille saab seejärel rakendada tasakaalustuse seadistuse kaudu ostureskontro parameetrites ja müügireskontro parameetrites. Saate luua hankijamakseid ja kliendi otsekorraldusmakseid, kasutades maksesoovitust, mida kasutatakse makstavate arvete valimiseks. Maksesoovituse käsitsi paraneda, kuid seejärel Microsoft Dynamics 365 toiminguteks on automaatselt tähistab valitud arvete tasakaalustamiseks maksete loomisel. Kui maksed luuakse käsitsi, saate tasakaalustatavad arved valida lehel **Kannete tasakaalustamine**. Saate arveid käsitsi valida või kasutada suvandit **Märgi prioriteedi alusel**, et arved märgitaks tasakaalustamiseks automaatselt. Suvand **Märgi prioriteedi alusel** on saadaval ainult müügireskontro puhul. Selle suvandi lubamiseks kasutage müügireskontro parameetrites lehte **Tasakaalustuse prioriteet**. Kui makseametnik sisestab makse, kuid ei tasakaalusta seda makset enne sisestamist, saab makse automaatselt tasakaalustada. Saate lubada automaatne tasakaalustus Müügireskontro parameetrid ja Ostureskontro parameetrid. Automaatne tasakaalustus kasutamisel saate kasutada eelmääratletud lahendamise korralduse või oma lahendamise prioriteetide järjestuse saate määratleda Müügireskontro parameetrites. See funktsioon on saadaval ainult müügireskontro puhul.

## <a name="results-of-settlement"></a>Tasakaalustamise tulemused
Kui kanded on tasakaalustatud, suurendatakse või vähendatakse iga kande saldo vajadust mööda. Tüüpilise stsenaariumi puhul, kus arve ja makse on tasakaalustatud, värskendatakse iga kande olekut ja saldot järgmiste reeglite järgi.

-   Kui makse summa on suurem kui arve summa, vähendatakse arve saldo väärtusele 0,00 ja arve suletakse. Makse jääb avatuks ja saldo on summa, mille võrra makse ületab arve summat.
-   Kui makse summa on väiksem kui arve summa, vähendatakse makse saldo väärtusele 0,00 ja makse suletakse. Arve jääb avatuks ja saldo on summa, mille võrra on makse summa arve summast väiksem.
-   Kui makse summa on arve summaga võrdne, suletakse nii makse kui ka arve ja mõlema saldo on 0,00.

Kui [makse on väiksem kui arve summa](../accounts-payable/vendor-payments-partial-amount.md) ja selle põhjuseks on skonto, mahakandmine või alamakse, võidakse arve ja makse siiski sulgeda, olenevalt tasakaalustuse seadistusest ostureskontro parameetrites ja müügireskontro parameetrites. Tasakaalustus saab luua ka kandeid. Näiteks võib arve ja makse tasakaalustamine tekitada skonto, realiseeritud kasumi või kahjumi, käibemaksu korrigeerimisi, mahakandmisi või sendierinevusi.


