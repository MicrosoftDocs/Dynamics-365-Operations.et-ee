---
title: "Osaliselt reserveeritud üleviimistellimuste hulgiväljastamine"
description: "Selles teemas kirjeldatakse, kuidas seadistada ja rakendada mobiilselt seadmelt osaliselt reserveeritud üleviimistellimuste hulgiväljastamist."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: 4477749c721cf8c8bd244f551d9eca7ec9449fd1
ms.contentlocale: et-ee
ms.lasthandoff: 02/08/2018

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Osaliselt reserveeritud üleviimistellimuste hulgiväljastamine

[!include[banner](../includes/banner.md)]

Osaliselt reserveeritud üleviimistellimuste hulgiväljastamise funktsioon võimaldab pakett-töö abil üleviimistellimusi osaliselt lattu väljastada.
Kuna on olemas osalise koguse väljastamise võimalus, ei pea enne tellimuse väljastamist ootama, et terve tellimuse kogus laos kättesaadav oleks.

Tellimuste väljastamine lattu on täpsem laohalduse protsess. See protsess hõlmab tegevusi, nagu komplekteerimine, pakkimine ja saatmine, mida laotöötaja saab mobiilse seadme abil teha.

## <a name="where-it-applies"></a>Kus see kehtib

Selle funktsiooni puhul väljastatakse üleviimistellimused lattu pakett-töö abil. See funktsioon on abiks, kui teil pole laos piisavalt varusid, kuid soovite siiski kaupu ühest laost teise üle viia.

## <a name="how-it-is-set-up"></a>Kuidas see seadistatakse

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Määrake üleviimistellimuste ja müügitellimuste täitmise kriteeriumid

Enne, kui tellimuse saab osaliselt partiina lattu väljastada, peavad täitmise kriteeriumid olema täidetud. Need täitmise kriteeriumid määratakse täitmispoliitikaga.

Üleviimistellimuste ja müügitellimuste täitmispoliitikad määratakse ettevõtte tasandil. Olenevalt täitmispoliitika seadistusest võetakse tellimuste väljastamine partiina vastu või lükatakse tagasi. Seejärel töödeldakse tellimusi vastavalt.

-   Üleviimis- ja müügitellimuste täitmispoliitikate koostamiseks klõpsake valikuid **Laohaldus** \> **Seadistus** \> **Lattu väljastamine** \> **Täitmispoliitika** ja koostage siis täitmispoliitika, sisestades nime ja kirjelduse.

-   Et määrata täitmise määr, väärtuse tüüp ja sõnum, mis kuvatakse, kui täitmispoliitikat rikutakse, klõpsake välju **Laohaldus** \> **Seadistus** \> **Lattu väljastamine** \> **Täitmispoliitika** ja määrake siis **Täitmismäär**, **Väärtuse tüüp** ja **Täitmise rikkumise teade**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Määrake üleviimistellimuste ja müügitellimuste täitmise poliitikad

-   Üleviimistellimuste täitmise poliitikate määramiseks klõpsake valikuid **Varude haldus** \> **Seadistus** \> **Varude ja laohalduse parameetrid** \> **Üleviimistellimused** \> **Laohaldus** ja valige siis üleviimistellimuse täitmise poliitika.

-   Müügitellimuste täitmise poliitikate määramiseks klõpsake valikuid **Müügireskontro** \> **Seadistus** \> **Müügireskontro parameetrid** \> **Laohaldus** ja valige siis müügitellimuse täitmise poliitika.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Lubage partiina väljastamine ja määrake kogus, mis tuleks partiina väljastada

Laost tellimuste partiina väljastamiseks kasutatakse pakett-tööd. Parameetrid, mis eristavad tellimusi, mis tuleks pakett-tööna käivitada, määratakse pakett-töös eneses.

Parameeter **Kogus** määrab, kas partiina tuleks väljastada terve kogus või füüsiliselt reserveeritud kogus. Parameeter **Luba osaliselt väljastatud tellimuste väljastamine** määrab, kas partii tellimused tuleks vastu võtta või tagasi lükata, kui nad varem osaliselt väljastati.

-   Parameetrite **Kogus** ja **Luba osaliselt väljastatud tellimuste väljastamine** määramiseks üleviimistellimustele klõpsake valikuid **Laohaldus** \> **Lattu väljastamine** \> **Üleviimistellimuste automaatne väljastamine**.

-   Parameetrite **Kogus** ja **Luba osaliselt väljastatud tellimuste väljastamine** määramiseks müügitellimustele klõpsake valikuid **Laohaldus** \> **Lattu väljastamine** \> **Müügitellimuste automaatne väljastamine**.

