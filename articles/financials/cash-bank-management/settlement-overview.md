---
title: "Tasakaalustuse ülevaade"
description: "Selles artiklis antakse üldist teavet tasakaalustamisprotsessi kohta. See kirjeldab kannete tüüpe, mida saab tasakaalustada, seda, millal ja kuidas kandeid saab tasakaalustada, ja tasakaalustusprotsessi tulemusi."
author: kweekley
manager: AnnBe
ms.date: 12/06/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 075d0f5dc0c9dc4e46dc92a2da75da9f7a207472
ms.openlocfilehash: 9b82c6afa2812344ff8200e227ee8c5f2451584f
ms.contentlocale: et-ee
ms.lasthandoff: 12/06/2018

---

# <a name="settlement-overview"></a>Tasakaalustuse ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis antakse üldist teavet tasakaalustamisprotsessi kohta. See kirjeldab kannete tüüpe, mida saab tasakaalustada, seda, millal ja kuidas kandeid saab tasakaalustada, ja tasakaalustusprotsessi tulemusi.

Tasakaalustuse ajal rakendatakse ühe dokumendi kanded teise dokumendi kannetele, et suurendada või vähendada kummagi dokumendi saldot. Näiteks saate makse arvele rakendada. Erinevaid kande tüüpe saab erinevatel aegadel ja erinevate meetodite kaudu tasakaalustada. Tasakaalustus võib põhjustada ka uute kannete loomist.

## <a name="what-transactions-can-be-settled"></a>Milliseid kandeid saab tasakaalustada?
Ostureskontro ja müügireskontro tasakaalustus võib toimuda mis tahes kandetüüpide vahel, mis mõjutavad hankija saldot või kliendi saldot, nagu arved, maksed, kreeditarved ja tasud. Iga kandetüübi saab tasakaalustada teise kandetüübi suhtes. Näiteks saate tasakaalustada makse arve suhtes, kreeditarve arve suhtes, ühe arve teise arve suhtes ja ühe makse teise makse suhtes. Saate tasakaalustada makseid samas juriidilises isikus või teises juriidilises isikus olevate kannete suhtes. Organisatsioonid, mis kasutavad tsentraliseeritud maksemudelit, [tsentraliseeritud maksed](set-up-centralized-payments.md) saavad aidata makseprotsessi sujuvamaks muutmisel.

## <a name="when-to-settle-transactions"></a>Millal kandeid tasakaalustada?
Kandeid saab tasakaalustada makse sisestamise ajal. Näiteks kui teete makse hankijale, valite tavaliselt makstavad arved. Arvete valimisega märgistate need makse suhtes tasakaalustamiseks. Kui Müügireskontro makseametnikud kirjendavad kliendimakse, saavad nad kliendimaksesse lisatud teabe põhjal sobivad arved tasakaalustamiseks märgistada. Makseid saab tasakaalustamiseks märkida lehel **Kannete tasakaalustamine**. Selle lehe saate avada mis tahes sisestamata arvelt või makselt. Kande sisestamisel sisestatakse ka tasakaalustus. Kandeid saab tasakaalustada ka pärast sisestamist. Saate sisestada kliendimakse ilma seda arvete suhtes tasakaalustamata. Siiski peate võib-olla esmalt uurima, kas makse on õige arve suhtes tasakaalustatud. Lehe **Kannete tasakaalustamine** saab avada lehelt **Kõik kliendid** või **Kõik hankijad** või mis tahes kliendi või hankija lehelt **Kanded**. Samuti saate arve jaoks sisestatud ettemakseid reserveerida, märkides makse ostutellimuse või müügitellimuse suhtes tasakaalustamiseks. Sellisel juhul on maksel endiselt avatud saldo, kuid selle saab tasakaalustada teise arve suhtes. Makse tasakaalustatakse automaatselt ostu- või müügitellimusest loodud arve suhtes.

## <a name="how-to-settle-transactions"></a>Kuidas kandeid tasakaalustada?
Kandeid saab tasakaalustada käsitsi, automaatselt või kaht meetodit kombineerides. Tasakaalustusmeetodi valik sõltub äriprotsessidest, mille saab seejärel rakendada tasakaalustuse seadistuse kaudu ostureskontro parameetrites ja müügireskontro parameetrites. Saate luua hankijamakseid ja kliendi otsekorraldusmakseid, kasutades maksesoovitust, mida kasutatakse makstavate arvete valimiseks. Maksesoovitus käivitatakse käsitsi, kuid seejärel märgistab rakendus Microsoft Dynamics 365 for Finance and Operations maksete loomisel valitud arved automaatselt tasakaalustamiseks. Kui maksed luuakse käsitsi, saate tasakaalustatavad arved valida lehel **Kannete tasakaalustamine**. Saate arveid käsitsi valida või kasutada suvandit **Märgi prioriteedi alusel**, et arved märgitaks tasakaalustamiseks automaatselt. Suvand **Märgi prioriteedi alusel** on saadaval ainult müügireskontro puhul. Selle suvandi lubamiseks kasutage müügireskontro parameetrites lehte **Tasakaalustuse prioriteet**. Kui makseametnik sisestab makse, kuid ei tasakaalusta seda makset enne sisestamist, saab makse automaatselt tasakaalustada. Saate automaatse tasakaalustamise lubada müügi- ja ostureskontro parameetrites. Automaatse tasakaalustuse kasutamisel saate kasutada eelmääratletud tasakaalustuse järjekorda või saate müügireskontro parameetrites määratleda teie enda tasakaalustuse prioriteedijärjestuse. See funktsioon on saadaval ainult müügireskontro puhul.

## <a name="results-of-settlement"></a>Tasakaalustamise tulemused
Kui kanded on tasakaalustatud, suurendatakse või vähendatakse iga kande saldo vajadust mööda. Tüüpilise stsenaariumi puhul, kus arve ja makse on tasakaalustatud, värskendatakse iga kande olekut ja saldot järgmiste reeglite järgi.

-   Kui makse summa on suurem kui arve summa, vähendatakse arve saldo väärtusele 0,00 ja arve suletakse. Makse jääb avatuks ja saldo on summa, mille võrra makse ületab arve summat.
-   Kui makse summa on väiksem kui arve summa, vähendatakse makse saldo väärtusele 0,00 ja makse suletakse. Arve jääb avatuks ja saldo on summa, mille võrra on makse summa arve summast väiksem.
-   Kui makse summa on arve summaga võrdne, suletakse nii makse kui ka arve ja mõlema saldo on 0,00.

Kui [makse on väiksem kui arve summa](../accounts-payable/vendor-payments-partial-amount.md) ja selle põhjuseks on skonto, mahakandmine või alamakse, võidakse arve ja makse siiski sulgeda, olenevalt tasakaalustuse seadistusest ostureskontro parameetrites ja müügireskontro parameetrites. Tasakaalustus saab luua ka kandeid. Näiteks võib arve ja makse tasakaalustamine tekitada skonto, realiseeritud kasumi või kahjumi, käibemaksu korrigeerimisi, mahakandmisi või sendierinevusi.


## <a name="additional-resources"></a>Lisaressursid
- [Jäägi tasakaalustus](settle-remainder.md)


