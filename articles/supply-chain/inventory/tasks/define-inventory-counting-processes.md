---
title: Inventuuriprotsesside määratlemine
description: See artikkel kirjeldab põhilisi varude loendusprotsesside konfiguratsiooni inventuurigrupi ja inventuuritöölehe loomisega.
author: yufeihuang
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb86c99e74dc8251ed48c0b749c0b0ef1ce75e34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879015"
---
# <a name="define-inventory-counting-processes"></a>Inventuuriprotsesside määratlemine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab põhilisi varude loendusprotsesside konfiguratsiooni inventuurigrupi ja inventuuritöölehe loomisega. Samuti näitab see, kuidas lubada inventuuripoliitikad lao ja kauba tasemel. Neid ülesandeid täidab üldjuhul laoinspektor. Eeltingimuseks on mõne olemasoleva väljastatud toote ja ladude olemasolu. Demoandmete ettevõtte kasutamisel saate selle protseduuri USMF-ettevõttes käivitada iga ladustatud kaubaga.


## <a name="create-a-counting-group"></a>Looge inventuurigrupp.
1. Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Laovarud > Inventuurigrupid**.
2. Valige suvand **Uus**.
3. Uue rea väljale **Inventuurigrupp** sisestage väärtus.
4. Sisestage väärtus väljale **Nimi**.
5. Väljal **Inventuurikood** valige sobiv variant.

    - **Manuaalne** - kaasab ridu iga kord, kui käivitate töö. Teiste sõnadega, saate määrata sellele inventuurigrupile inventuuriintervalli.  
    - **Periood** - kaasab ridu inventuuritöölehe perioodi kohta kui perioodi intervall on aegunud.  
    - **Null laoseis** - kui laoseis jõuab nullini (0), luuakse read inventuuritöölehele, kui töö käivitatakse. Kui vaba laoseis muutub nulliks pärast inventuuri, luuakse read järgmise inventuuri käivitamise ajal.  
    - **Minimaalne** - sisestab ridu inventuuritöölehele, kui laoseis on võrdne või väiksem kui seadistatud miinimum.  
    - Valikuline: kui olete täpsustanud **Perioodi** väljal **Inventuurikood**, peate sisestama perioodi intervalli väljal **Inventuuri periood**. Intervalli ühikuks on päev.  
    - Inventuuritöölehe uute ridade loomise töö käivitamisel luuakse uued read sellel väljal määratletud intervalliga, olenemata sellest, kui sageli sama töö käivitate. Näiteks kui välja **Inventuuri periood** väärtuseks on 7 ja töölehe read loodi viimati inventuuriks 1. jaanuaril, kui teine töö alustati 5. jaanuaril, pole seitse päeva möödunud ja selle perioodi intervalli kohta ei looda ridu töölehele. Kui käivitate töö uuesti 8. jaanuaril, luuakse read inventuuritöölehe perioodiks, sest 7 päeva on möödunud.  

6. Valige käsk **Salvesta**.

## <a name="create-a-counting-journal-name"></a>Looge inventuuri töölehe nimi.
1. Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Töölehe nimed > Laoseis**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Nimi**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Väljal **Töölehe tüüp** valige **Inventuur**. Valikuline: saate valida erineva kandeseeria ID, kui soovite inventuuritöölehtede loomisel loodud kande ID-de puhul konkreetset numbriseeriat. Kandeseeriad luuakse lehele **Numbriseeriad**.  
6. Väljal **Üksikasja tase** valige sobiv variant.  

    - See on üksikasjade tase, mis rakendatakse, kui tööleht on sisestatud.  
    - Valikuline: saate muuta väärtust väljal Reserveerimine. See on inventuuris kaupade reserveerimiseks kasutatav meetod.   
    - **Manuaalne** - kaubad reserveeritakse käsitsi reserveerimisvormil.  
    - **Automaatne** - tellimuse kogus on reserveeritud olemasolevast kauba laoseisust.   
    - **Koosnevus** - reserveering on osa kande koondplaneerimisest.  

7. Valige käsk **Salvesta**.

## <a name="set-standard-counting-journal-name"></a>Standardse inventuuri töölehe nime määramine
1. Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Ladu > Varude ja laohalduse parameetrid**.
2. Valige vahekaart **Töölehed**.
3. Välja **Inventuur** rippmenüüst valige varem loodud tööleht. See tööleht on nüüd vaikimisi töölehe nimi laoseisu töölehtede jaoks tüübi **Inventuur** jaoks.  
4. Valige vahekaart **Üldine**. Valikuline: valige see suvand, et lukustada kaup inventuuriprotsessi käigus, et ennetada saatelehtede, komplekteerimislehtede või komplekteerimislehtede registreerimise värskendusi.  

## <a name="set-the-counting-policy-for-an-item"></a>Kauba inventuuripoliitika määramine
1. Navigeerimispaanil avage **Moodulid > Toote teabe haldus > Tooted > Väljastatud tooted**.
2. Loendist valige link kauba tootekoodi jaoks, mille kohta soovite seadistada inventuuripoliitikat. Peate valima kauba, mille laoseis on jälgitav. Mitteladustatavat toodet ei saa loendada. USMF-i demoandmete kasutamisel saate valida kauba A0001.  
3. Valige suvand **Redigeeri**.
4. Lülituge ümber jaotise **Halda laoseisu** laiendusele.
5. Välja **Inventuurigrupp** rippmenüüst valige varem loodud inventuurigrupp. See toode kaasatakse nüüd varude inventuuri tööleheridade loomisel selle inventuurigrupiga.  
6. Valige käsk **Salvesta**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Konkreetse lao kauba inventuuripoliitika määramine
1. Klõpsake toimingupaanil suvandit **Halda varusid**.
2. Valige **Lao üksused**.
3. Valige suvand **Uus**.
4. Välja **Ladu** rippmenüüst valige ladu, mille kohta soovite seadistada konkreetset inventuuripoliitikat.
5. Välja **Inventuurigrupp** rippmenüüst valige inventuurigrupp. Saate valida konkreetse inventuurigrupi, mis peaks rakenduma kaubale konkreetses laos, mille olete valinud. Selles laos inventuuri tegemisel alistab see inventuuripoliitika kauba üldise inventuuripoliitika.  
6. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]