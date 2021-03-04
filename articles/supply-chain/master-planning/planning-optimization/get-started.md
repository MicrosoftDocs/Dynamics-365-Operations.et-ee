---
title: Planeerimise optimiseerimise kasutamise alustamine
description: Selles teemas selgitatakse, kuidas hakata kasutama planeerimise optimeerimise funktsiooni.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4426704"
---
# <a name="get-started-with-planning-optimization"></a>Planeerimise optimeerimisega alustamine

[!include [banner](../../includes/banner.md)]

Nagu [eelnevalt välja kuulutatud](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), asendab planeerimise optimeerimine varsti olemasoleva sisseehitatud koondplaneerimise mootori.

Kui kasutate praegu sisseehitatud koondplaneerimise mootorit, peaksite hakkama tegema kohe plaane migreerimiseks planeerimise optimeerimisse. On oluline alustada migreerimisprotsessi kohe, sest teie toiminguid võidakse mõjutada, kui iganemine jõustatakse. Et vältida viimasel hetkel tekkivaid probleeme iganemise jõustamisel, soovitame teil tungivalt migreerimise lõpule viia enne 1. detsembrit 2020. 

Planeerimise optimeerimise funktsioon ei toeta hetkel kõiki funktsioone, mis on rakendusse Supply Chain Management ehitatud planeerimismootoris saadaval. Seega on oluline, et hindaksite, kas hetkel planeerimise optimeerimises saadaolev funktsioonide komplekt vastab teie nõuetele. Planeerimise optimeerimise funktsioon ei ole praegu vaikimisi sisse lülitatud lahenduses Dynamics Lifecycle Services (LCS), seega on teil võimalus teha oma hinnang enne funktsiooni sisselülitamist.

> [!NOTE]
> Peate taotlema planeerimise optimeerimise funktsiooni migreerumiseks erandit, kui teie koondplaneerimise protsess ei hõlma tootmist (koondplaneerimise loodud plaanitud tootmistellimused) ja vajate sisseehitatud koondplaneerimise mootori versioonist 10.0.15 uuemat versiooni. Alates versioonist 10.0.16 kuvatakse tõrge keskkondades, kus sisseehitatud koondplaneerimine töötab ilma plaanitud tootmistellimuste loomiseta. Planeerimise optimeerimise funktsiooni tuleks kasutada kõigi uute juurutuste puhul, mis ei loo koondplaneerimise ajal plaanitud tootmistellimusi. Selliste olemasolevate keskkondade omanikud, milles käitatakse sisseehitatud koondplaneerimise mootorit ilma plaanitud tootmistellimuste loomiseta, saavad e-kirja koos üksikasjadega erandiprotsessi kohta. Soovitame töötada koos partneriga, et hinnata ja planeerida migreerumist planeerimise optimeerimise funktsiooni.

Enne planeerimise optimeerimise sisselülitamist soovitame teil hinnata planeerimise optimeerimise sobivuse analüüsi tulemusi. Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).

### <a name="availability"></a>Kättesaadavus
Planeerimise optimeerimine on hetkel kättesaadav järgmistes Azure'i geograafilistes piirkondades: Ameerika Ühendriigid, Kanada, Euroopa, Ühendkuningriik ja Austraalia. Kui proovite lisandmoodulit installida muus geograafilises piirkonnas, siis kuvab LCS teate, et seda geograafilist piirkonda ei toetata.

Pange tähele, et planeerimise optimeerimine ei toeta Dynamics 365 Supply Chain Management-i kohapealseid juurutusi.

### <a name="licensing"></a>Litsentsimine

Kui saate käivitada koondplaneerimise oma praegust litsentsi kasutades, ei pea te täiendavat litsentsi ostma, et hakata planeerimise optimeerimist kasutama.

### <a name="install-the-add-in"></a>Lisandmooduli installimine

Planeerimise optimeerimise kasutamiseks installige Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmoodul. Saate kasutada lisandmoodulit oma LCS projektist ja lülitada planeerimise optimeerimise funktsiooni sisse tarneahela halduse kasutajaliidesest.

> [!NOTE]
> Planeerimise optimeerimise nõue on LCS-i loaga suure kättesaadavusega keskkond, järk 2 või kõrgem, (mitte OneBoxi keskkond) koos Dynamics 365 Supply Chain Management-i versiooniga 10.0.7 või hilisem. Kui proovite paigaldada moodulit OneBoxi keskkonnas, siis ei viida paigaldust lõpule ja te peate paigalduse tühistama.

1. Logige LCS-i sisse ja avage soovitud keskkond.
1. Avage **Kõik üksikasjad**.
1. Kerige alla kiirkaardini **Keskkonna lisandmoodulid**.
1. Valige **Installi uus lisandmoodul**.
1. Valige **Planeerimise optimeerimine**.
1. Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.
1. Valige **Installi**.
1. Kiirkaardil **Keskkonna lisandmoodulid** peaksite nägema, et planeerimise optimeerimine on installitud.
1. Mõne minuti pärast peaks olek **Installimine** muutuma olekuks **Installitud** (võimalik, et peate lehte värskendama). Kui installimine on lõpetatud, olete valmis aktiveerima optimeerimise plaanimise rakenduses Dynamics 365 Supply Chain Management.

Planeerimise optimeerimise lisandmooduli installimise peamine eesmärk on ühendada teenus ja keskkond. Seetõttu peate installima lisandmooduli eraldi igasse keskkonda, kus te kasutate planeerimise optimeerimist, olenemata mis tahes koodist, mis on teisaldatud keskkondade vahel.

### <a name="planning-optimization-integration"></a>Planeerimise optimeerimise integreerimine

Konfigureerimaks, kas planeerimise optimeerimise lisandmoodulit peaks koondplaneerimise jaoks kasutama, avage **Koondplaneerimine** \> **Seadistamine** \> **Optimeerimise parameetrite plaanimine**.

#### <a name="connection-status"></a>Ühenduse olek

Ühenduse olek näitab tarneahela halduse ja planeerimise optimeerimise teenuse vahelise ühenduse hetkeolekut. Järgmine tabel näitab võimalikke väärtuseid.

| Ühenduse olek | Kirjeldus | Kas planeerimise optimeerimist saab kasutada? |
|---|---|---|
| Ühendus on loodud | Planeerimise optimeerimise teenuse ja tarneahela halduse vahel on loodud ühendus. | Jah |
| Ühenduse loomine | Planeerimise optimeerimise teenuse ühendamise sisselülitamise taotlus on praegu tööd. | Ei |
| Ühendus on katkestatud | Planeerimise optimeerimise teenusega puudub ühendus. Ühenduse saab lülitada sisse LCS-ist, nagu selles teemas varasemalt on kirjeldatud. | Ei |
| Ühenduse katkestamine | Planeerimise optimeerimise teenuse ühendamise väljalülitamise taotlus on praegu tööd. | Ei |
| Oleku hankimine | Süsteem ootab planeerimise optimeerimise teenuselt oleku teavet. | Ei |

#### <a name="the-use-planning-optimization-option"></a>Planeerimise optimeerimise kasutamise suvand

Suvandi **Planeerimise optimeerimise kasutamine** säte määrab, millist planeerimismootorit koondplaneerimiseks kasutatakse.

- **Jah** – planeerimise optimeerimist kasutatakse koondplaneerimiseks.
- **Ei** – koondplaneerimise jaoks kasutatakse sisseehitatud tarneahela halduse planeerimise mootorit.

> [!NOTE]
> Kui olemasoleva planeerimise paketi tööd, mis sisseehitatud tarneahela halduse planeerimismootori jaoks loodi, käivitatakse sel ajal, kui suvandi **Planeerimise optimeerimise kasutamine** väärtuseks on seatud **Jah**, siis need tööd nurjuvad.

### <a name="integration-with-the-setup"></a>Integreerimine seadistamisega

Kui planeerimise optimeerimine on sisse lülitatud, tehakse koondplaneerimine planeerimise optimeerimise lisandmoodulit kasutades. Sel juhul on koondplaneerimise tulemused ja funktsioonid mõjutatud.

## <a name="additional-resources"></a>Lisaressursid

[Eelvaate tingimused ja nõuded](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)

[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)

[Plaani ajaloo ja plaanimise logide vaatamine](plan-history-logs.md)

[Plaanile filtrite rakendamine](plan-filters.md)

[Planeerimistöö tühistamine](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]