---
title: Topeltkirjutuse ülevaade
description: See teema annab topeltkirjutamisest ülevaate. Topeltkirjutus on infrastruktuur, mis pakub reaalaja lähedast suhtlust Microsoft Dynamics 365 mudelipõhiste rakenduste ja Finance and Operationsi rakenduste vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c4a643d4981364cea5b549118c201ac8a9798e02
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113870"
---
# <a name="dual-write-overview"></a>Topeltkirjutuse ülevaade

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a>Mis on topeltkirjutus?

Topeltkirjutus on valmiskujul infrastruktuur, mis pakub reaalaja lähedast suhtlust Microsoft Dynamics 365 mudelipõhiste rakenduste ja Finance and Operationsi rakenduste vahel. Kui andmed klientide, toodete, inimeste ja operatsioonide kohta liiguvad rakenduse piiridest välja, omavad organisatsiooni kõik osakonnad võimalust.

Topeltkirjutus pakub tihedalt ühendatud, kahesuunalist integratsiooni Finance and Operationsi rakenduste ja teenuse Common Data Service vahel. Mis tahes andmete muudatus Finance and Operationsi rakendustes põhjustab kirjutamist teenusesse Common Data Service ja mis tahes andmete muudatused teenuses Common Data Service põhjustab kirjutamist Finance and Operationsi rakendustesse. See automatiseeritud andmevoog pakub rakenduste vahel integreeritud kasutuskogemust.

![Andmete seos rakenduste vahel](media/dual-write-overview.jpg)

Topeltkirjutusel on kaks aspekti: *taristu* aspekt ja *rakenduse* aspekt.

### <a name="infrastructure"></a>Taristu

Topeltkirjutuse taristu on laiendatav ja usaldusväärne ning sisaldab järgmisi põhifunktsioone.

+ Sünkroonne ja kahesuunaline andmeedastus rakenduste vahel
+ Sünkroonimine koos esituse, peatamise ja järele jõudmise režiimidega, et toetada süsteemi veebipõhiste ja veebiväliste/asünkroonsete režiimide ajal.
+ Võime sünkroonida algandmeid rakenduste vahel
+ Tegevuse ja vigade logide konsolideeritud vaade andmete administraatoritele
+ Võime konfigureerida kohandatud teatisi ja lävendeid ning tellida teatisi
+ Intuitiivne kasutajaliides (UI) filtreerimiseks ja teisendusteks
+ Võime määrata ja kuvada üksuse sõltuvusi ja seoseid
+ Laiendatavus nii standardsete kui ka kohandatud üksuste ja kaartide jaoks
+ Usaldusväärne rakenduse elutsükli haldus
+ Valmiskujul seadistuse kogemus uutele klientidele

### <a name="application"></a>Avaldus

Topeltkirjutus loob vastenduse Finance and Operationsi rakenduste kontseptsioonide ja Dynamics 365 mudelipõhiste rakenduste kontseptsioonide vahel. See integratsioon toetab järgmisi stsenaariumeid.

+ Integreeritud kliendi koondandmed
+ Juurdepääs kliendi kliendikaartidele ja preemiapunktidele
+ Ühendatud tooteetaloni kasutusfunktsionaalsus
+ Organisatsiooni hierarhia teadlikkus
+ Integreeritud hankija koondandmed
+ Juurdepääs finantsilistele ja maksude viiteandmetele
+ Nõudmisel hinnakujunduse mootori kogemus
+ Integreeritud potentsiaalse kliendi sularaha kogemus
+ Võime teenindada nii majasiseseid varasid kui ka väliagentide kaudu kliendi varasid
+ Integreeritud maksmiseks hankimise kogemus
+ Kliendiandmetele ja dokumentide integreeritud tegevused ja märkused
+ Võimalus otsida vabade varade saadavust ja üksikasju
+ Projektist sularahaks kogemus
+ Võime käsitseda osapoole kontseptsiooni kaudu mitut aadressi ja rolli
+ Kasutajate ühe allika haldamine
+ Jaemüügi ja turunduse integreeritud kanalid
+ Kampaaniate ja allahindluste nähtavus
+ Teenusetaotluse funktsioonid
+ Sujuvad teenusetoimingud

## <a name="top-reasons-to-use-dual-write"></a>Topeltkirjutuse kasutamise peamised põhjused

Topeltkirjutus võimaldab Microsoft Dynamics 365 rakenduste üleselt andmete integreerimist. See jõuline raamistik ühendab keskkondasid ja võimaldab erinevatel ärirakendustel koos töötada. Siin on peamised põhjused, miks peaksite topeltkirjutust kasutama.

+ Topeltkirjutus pakub tihedalt ühendatud, peaaegu reaalajas ja kahesuunalist integratsiooni Finance and Operationsi rakenduste ja Dynamics 365 mudelipõhiste rakenduste vahel. See integratsioon muudab Microsoft Dynamics 365 ühe peatuse poeks kõigi teie ärilahenduste jaoks. Kliendid, kes kasutavad rakendusi Dynamics 365 Finance ja Dynamics 365 Supply Chain Management, kuid kasutavad kliendisuhte halduseks (CRM) mitte-Microsofti lahendusi, liiguvad Dynamics 365 suunas selle topeltkirjutamise toe jaoks.
+ Klientide, toodete, operatsioonide, projektide ja asjade Interneti (IoT) andmed voolavad automaatselt topeltkirjutuse kaudu teenusesse Common Data Service. See ühendus on väga kasulik ettevõtetele, kes on huvitatud Microsoft Power Platformi laiendustest.
+ Topeltkirjutuse infrastruktuur järgib puuduva koodi / vähese koodi põhimõtet. Standardsete tabelist tabelisse kaartide laiendamiseks ja kohandatud kaartide kaasamiseks on vajalik minimaalne projekteerimise panus.
+ Topeltkirjutus toetab nii ühendusega režiimi kui ka võrguühenduseta režiimi. Microsoft on ainus ettevõte, mis pakub ühendusega ja võrguühenduseta režiimide tuge.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Mida tähendab topeltkirjutus CRM-i toodete kasutajate ja arhitektide jaoks?

Topeltkirjutus automatiseerib andmevoo Finance and Operationsi rakenduste ja teenuse Common Data Service vahel. Tulevastes väljaannetes on Dynamics 365 mudelipõhiste rakenduste kontseptsioonid (nt klient, kontakt, pakkumine ja tellimus) muudetud keskmise turu ja ülemise keskmise turu klientidele sobivaks.

Esimeses väljalaskes käsitsevad enamikku automatiseerimisest topeltkirjutuse lahendused. Tulevastes väljaannetes muutuvad need lahendused teenuse Common Data Service osaks. Teenuse Common Data Service tulevaste muudatuste mõistmisega saate pikemas perspektiivis oma jõupingutusi säästa. Siin on mõned uued olulised muudatused.

+ Common Data Service omab uusi kontseptsioone, nt ettevõte ja osapool. Need kontseptsioonid mõjutavad kõiki rakendusi, mis on teenuse Common Data Service peale ehitatud, nagu Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ja Dynamics 365 Field Service.
+ Tegevused ja märkmed on ühtlustatud ning laiendatud, et toetada nii C1-sid (süsteemi kasutajaid) kui ka C2-sid (süsteemi kliendid).
+ Siin on mõned teenuse Common Data Service tulevased muudatused.

    - Kümnendkoha andmetüüp asendab raha andmetüübi.
    - Kuupäeva jõustumine toetab samas kohas mineviku, oleviku ja tuleviku andmeid.
    - Valuuta ja vahetuskursside jaoks on rohkem tuge ning rakenduse programmeerimisliides (API) **Vahetuskurss** vaadatakse üle.
    - Toetatakse ühiku teisendusi.

Lisateavet eelseisvate muudatuste kohta vt teemast [Teenuse Common Data Service andmed – 1. ja 2. faas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).
