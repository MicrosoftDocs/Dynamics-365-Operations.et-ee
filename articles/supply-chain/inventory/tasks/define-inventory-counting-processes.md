---
title: Inventuuriprotsesside määratlemine
description: See protseduur annab ülevaate peamiste varude inventuuriprotsesside konfiguratsioonist, luues inventuurigrupi ja inventuuri töölehe.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 707d4fab58a9c689f32d9e881ecacbe8e64b517c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554249"
---
# <a name="define-inventory-counting-processes"></a>Inventuuriprotsesside määratlemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur annab ülevaate peamiste varude inventuuriprotsesside konfiguratsioonist, luues inventuurigrupi ja inventuuri töölehe. Samuti näitab see, kuidas lubada inventuuripoliitikad lao ja kauba tasemel. Neid ülesandeid täidab üldjuhul laoinspektor. Eeltingimuseks on mõne olemasoleva väljastatud toote ja ladude olemasolu. Demoandmete ettevõtte kasutamisel saate selle protseduuri USMF-ettevõttes käivitada iga ladustatud kaubaga.


## <a name="create-a-counting-group"></a>Looge inventuurigrupp.
1. Avage Varude haldus > Seadistus > Varud > Inventuurigrupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Inventuurigrupp.
4. Sisestage väärtus väljale Nimi.
5. Valige suvand väljalt Inventuurikood.
    * Käsitsi – read kaasatakse iga kord, kui töö käivitate. Teiste sõnadega, saate määrata sellele inventuurigrupile inventuuriintervalli.  Periood – kaasatakse read inventuuritöölehe perioodi jaoks, kui perioodi intervall on aegunud.   Null laoseis – kui vaba laoseis on null (0), luuakse töö käivitamisel inventuuritöölehele read. Kui vaba laoseis muutub nulliks pärast inventuuri, luuakse read järgmise inventuuri käivitamise ajal.   Miinimum – inventuuritöölehele sisestatakse read, kui vaba laoseis on määratud miinimumiga võrdne või sellest väiksem.  
    * Valikuline: kui määrasite välja Inventuurikood väärtuseks Periood, tuleb väljale Inventuuriperiood sisestada perioodivahemik. Intervalli ühikuks on päev.  
    * Inventuuritöölehe uute ridade loomise töö käivitamisel luuakse uued read sellel väljal määratletud intervalliga, olenemata sellest, kui sageli sama töö käivitate. Näiteks kui inventuuriperioodi väärtuseks on 7 ja tööleheridu loodi inventuuriks viimati 1. jaanuaril ja teine töö käivitatakse 5. jaanuaril, pole 7 päeva möödunud ja seega ei looda selle perioodivahemiku puhul töölehel ühtegi rida. Kui käivitate töö uuesti 8. jaanuaril, luuakse read inventuuritöölehe perioodiks, sest 7 päeva on möödunud.  
6. Klõpsake nuppu Salvesta.

## <a name="create-a-counting-journal-name"></a>Looge inventuuri töölehe nimi.
1. Avage Varude haldus > Seadistus > Töölehe nimed > Varud.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige väljal Töölehe tüüp suvand Inventuur.
    * Valikuline: saate valida erineva kandeseeria ID, kui soovite inventuuritöölehtede loomisel loodud kande ID-de puhul konkreetset numbriseeriat. Kandeseeriad luuakse lehel Numbriseeriad.  
6. Valige suvand väljalt Üksikasjatase.
    * See on üksikasjade tase, mis rakendatakse, kui tööleht on sisestatud.  
    * Valikuline: saate muuta väärtust väljal Reserveerimine. See on inventuuris kaupade reserveerimiseks kasutatav meetod.   
    * Käsitsi – kaubad reserveeritakse vormis Reserveerimine käsitsi.   Automaatne – tellimuse kogus on reserveeritud kauba vabast laoseisust.   Jaotamine – reserveerimine on osa kande koondplaanimisest.  
7. Klõpsake nuppu Salvesta.

## <a name="set-standard-counting-journal-name"></a>Standardse inventuuri töölehe nime määramine
1. Avage Varude haldus > Seadistus > Varude ja lao halduse parameetrid.
2. Klõpsake vahekaarti Töölehed.
3. Klõpsake väljal Inventuur otsingu avamiseks ripploendi nuppu.
4. Valige varem loodud tööleht.
    * See tööleht on siis vaikimisi töölehe nimi tüübi Inventuur laotöölehtede puhul.  
5. Klõpsake vahekaarti Üldine.
    * Valikuline: valige see suvand, et lukustada kaup inventuuriprotsessi ajaks, et vältida saatelehtede, komplekteerimislehtede või komplekteerimislehtede registreerimise muutmist.  

## <a name="set-the-counting-policy-for-an-item"></a>Kauba inventuuripoliitika määramine
1. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
2. Klõpsake loendis selle toote kaubakoodi lingil, mille puhul soovite inventuuripoliitikaid seadistada.
    * Pidage meeles, et peate valima kauba, mis on varudes jälgitav. Mitteladustatavat toodet ei saa loendada. USMF-i demoandmete kasutamisel saate valida kauba A0001.  
3. Klõpsake nuppu Redigeeri.
4. Lülitage jaotise Varude haldamine laiendamist.
5. Klõpsake väljal Inventuurigrupp otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis varem loodud inventuurigruppi.
    * See toode kaasatakse nüüd varude inventuuri tööleheridade loomisel selle inventuurigrupiga.  
7. Klõpsake nuppu Salvesta.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Konkreetse lao kauba inventuuripoliitika määramine
1. Klõpsake toimingupaanil suvandit Halda varusid.
2. Klõpsake suvandit Laokaubad.
3. Klõpsake Uus.
4. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
5. Valige loendist ladu, mille puhul soovite konkreetseid inventuuripoliitikaid seadistada.
6. Klõpsake väljal Inventuurigrupp otsingu avamiseks ripploendi nuppu.
7. Valige loendist inventuurigrupp.
    * Siin saate valida konkreetse inventuurigrupi, mis tuleks teie valitud konkreetses laos oleva kauba puhul rakendada. Selles laos inventuuri tegemisel alistab see inventuuripoliitika kauba üldise inventuuripoliitika.  
8. Klõpsake nuppu Salvesta.

