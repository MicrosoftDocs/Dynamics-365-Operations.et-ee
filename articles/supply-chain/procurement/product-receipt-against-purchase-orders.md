---
title: Toote sissetulek ostutellimuste suhtes
description: Selles teemas kirjeldatakse mitmesuguseid toodete sisstuleku registreerimise valikuid.
author: mkirknel
manager: tfehr
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, VendPackingSlipJournalListPage, VendPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cead310eaa86d755399e512f99d6782bfa551211
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426582"
---
# <a name="product-receipt-against-purchase-orders"></a>Toote sissetulek ostutellimuste suhtes

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse mitmesuguseid toodete sisstuleku registreerimise valikuid.

Toote sissetulek on protsess, millega näidatakse, et tellitud tooted on kätte saadud, et ostutellimuse ridu saaks siis arveldamiseks töödelda. Mõnikord läbivad tooted eelregistreerimise, mille käigus enne toodete vastuvõtmist registreeritakse tarnijalt saadud lisateave. Kui saabuvad, märgitakse need kõigepealt olekuga **Registreeritud**. Tooted võivad seejärel läbida lisaprotsesse (nt kvaliteedijuhtimine), enne kui nende olekuks märgitakse lõpuks **Saadud**.

## <a name="preregistration-asn"></a>Eelregistreerimine (ASN)
Tarnijad võivad jagada lähetatavate toodete kohta teavet. Sellisel juhul saate tooted eelregistreerida selle teabe salvestamiseks enne toodete saamist. Toodete eelregistreerimisega vähendate kauba registreerimise ja vastuvõtmise ajal vajaliku töö hulka. Tarnijad võivad edastada tooteteabe elektrooniliselt saadetise eelteatise (ASN) kaudu, mis siis automaatselt süsteemis salvestatakse. ASN-il olev teave sisaldab lähetatavate toodete kogust ja nende lähetuskuupäeva. ASN-il võib olla ka teave nagu partii- või seerianumbrid. ASN-i registreerimine toimub moodulis **Transpordihaldus**.

## <a name="registration"></a>Registreerimine
Toote sissetuleku registreerimine toimub sageli lao saabumisalal. See toimub käsiseadme või saabumise töölehtede kaudu. Teine võimalus on registreerida toote sissetulek käsitsi, kasutades toimingut **Registreerimine** lehel **Ostutellimus**. Mõlemal juhul märgitakse toodete olekuks **Registreeritud**. Pange tähele, et toodete olekuks pole veel märgitud **Saadud**.  

Tooted, mis laos vastu võetakse, võivad läbida enne varudesse paigutamist kvaliteedikontrolli. Kvaliteedikontrolli tegemiseks võib kasutada kvaliteettellimusi või vahelaoordereid. Kui kasutatakse kvaliteettellimusi, võite konfigureerida protsessi tooteid reserveerimise kaudu ajutiselt blokeerima, kuni neid kontrollitakse. Vahelaoorderite kasutamisel viiakse tooted kontrollimiseks teise lattu. Seda ladu nimetatakse vahelaoks. Mõlema kvaliteedikontrolli protsessi puhul võidakse osa kaupadest praagiks tunnistada, kuna need ei vasta kvaliteedinõuetele või kuna kvaliteedikontroll hõlmab tootenäidise purustavat katset.

## <a name="product-receipt"></a>Toote sissetulek
Kõige sagedamini kasutatakse toimingut **Toote sissetulek** lehel **Ostutellimused** selleks, et märkida ostutellimusel toodete olekuks **Saadud**. Lehel **Toote sissetuleku sisestamine** on mitmesuguseid valikuid vastuvõetuks märgitud koguste kohta. Näiteks saate määrata välja **Kogus** olekuks **Tellitud kogus** või **Kohe tarnitav kogus**. Teise võimalusena, kui on kasutatud lattu saabumise protsessi, määratakse sellel väljal sageli väärtus **Registreeritud kogus**. Saate muuta koguseid igal tellimuse real, mille olekuks määratakse **Saadud**, et kajastada igasuguseid lahknevusi, nt ala- või ületarnet. Toote sissetuleku ajal tuleb määrata toote sissetuleku identifikaator, mis on tavaliselt hankija saatelehe viide. See ID on raamatupidamise jaoks vajalik, kuna see võimaldab võrrelda hankija saatelehti ja saadud kaupu ning kontrollida arvestatud varusid või kulusid.  

Ostutellimusi saab koostada toodetele, mis pole mõeldud varudeks, vaid mida käsitletakse kuluna. See kategooria hõlmab tellimuse ridu, millel tooted on märgitud laomudeligrupi järgi olekuga **Ladustamata**, ja samuti ridu, mis kasutavad hankekategooriaid. Sel juhul ei pruugi kaubad läbida laos saabumise registreerimist ja vastuvõtmist. Selle asemel kasutatakse toimingut **Toote sissetulek** sissetuleku kajastamiseks otse ostutellimusel ja sissetulek põhineb tellitud, mitte registreeritud kogusel.  

Saate luua ostutellimuse ridu, millel on lubatud valik **Uus põhivara**. See valik näitab, et ostu tuleks käsitleda varude asemel põhivarana. Sellisel juhul määravad konfigureeritud põhivara määramise reeglid, kas toote või kategooria ost ületab konkreetseid lävesid ja kas seetõttu tuleks seda käsitleda varana ning läbida põhivara haldus. Oste saab teha ka olemasoleva põhivara suhtes. Sellisel juhul korrigeeritakse summat vajalikul viisil.  

Võite valida mitu tellimust ja töödelda kõigi nende tellimuste sissetulekut korraga. Sellist lähenemist ei kasutata kuigi sageli, kuid seda võib olla vaja kasutada, kui hankijal on teile ühes koormas konsolideeritud saadetised. Ostu toote sissetuleku käigus saab kasutada koondvärskenduste tegemise funktsiooni. Koondvärskendused võimaldavad sisestada ühe hankija saatelehe mitme ostutellimuse jaoks.  

Valiku **Otsetarne** korral võidakse koostada ostutellimusi müügitellimusest. Otsetarne kasutamisel ei saabu tooted kunagi teie lattu, vaid hankija viib need otse kliendile. Sellisel juhul kajastatakse sissetulek tavaliselt otse ostutellimusel. Sissetuleku saab vormistada automaatselt, nt elektroonilise andmevahetuse (EDI) integreerimise kaudu hankijaga. Kui tegemist on kontsernisisese ostutellimusega, siis on olemas ka võimalus, et Supply Chain Management automatiseerib kontsernisisese müügitellimuse sissetuleku, kui tarne toimub. Otsetarne kasutamisel käsitletakse tooteid endiselt varudena, kuigi need ei saabu füüsiliselt lattu. Seetõttu, kui toote sissetulek ostutellimusel registreeritakse, värskendatakse müügitellimust automaatselt saatelehe andmetega, nii et üldine varude muutus on 0 (null). Otsetarne stsenaariumide puhul ei tohiks eelregistreerimine vajalik olla. Kui kasutate ladusid, milles on lubatud laohaldus, võite litsentsiplaadi registreerimise nõudest mööda minna, määrates selle asemel virtuaalse lao. Selle lao saab määrata toote väljal **Otsetarne ladu**. 

Pärast toote sissetuleku töötlemist ostutellimusel määratakse ostutellimuse olekuks **Saadud** näitamaks, et tellimuse arvet võib töödelda. Juba saadud toodete üksikasju saab vaadata lehelt **Toote sissetuleku töölehed**.  

Sellele lehele pääsete tegevusgrupist **Sissetulek** lehel **Ostutellimus**. Töölehtedel olev teave sisaldab koguste, kuupäevade ja mõõtmete andmeid.

<a name="additional-resources"></a>Lisaressursid
--------

[Ostutellimuse ülevaade](purchase-order-overview.md)

[Ostutellimuste loomine](purchase-order-creation.md)

[Ostutellimuste kinnitamine](purchase-order-approval-confirmation.md)

[Hankija arvete ülevaade](../../financials/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]