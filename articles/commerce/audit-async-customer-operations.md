---
title: Klienditoimingute auditi sünkroonimine peakontoris
description: See artikkel selgitab, kuidas auditeerida klienditoimingute sünkroonimist peakontoris Microsoft Dynamics 365 Commerce, et aidata parandada mis tahes saidi kasutaja probleeme.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690956"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Klienditoimingute auditi sünkroonimine peakontoris

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See artikkel selgitab, kuidas auditeerida klienditoimingute sünkroonimist peakontoris Microsoft Dynamics 365 Commerce, et aidata parandada mis tahes saidi kasutaja probleeme.

Kuna organisatsioonid hakkavad vastu võtma klientide asünkroonse loomise ja redigeerimise võimalust, vajavad saidi administraatorid võimalust vaadata ja tõrkeotsingut, mis põhineb saidi kasutaja taotlustel või tootmisprotsessi tõrgetel. Sellistes stsenaariumides peaksid saidi administraatorid saama kliendi loomise ja redigeerimise toiminguid auditeerida ning parandada kõik tõrked iseteenindusmudeli abil.

## <a name="customer-synchronization-status"></a>Kliendi sünkroonimise olek

Kui otsustate kliendihalduse asünkroonse režiimi ja selle vastavate funktsioonidega, peavad Commerce Headquartersi **administraatorid P-töö jaoks looma ja plaanima korduva pakett-töö**, **sünkroonima kliendid ja äripartnerid async** **Mode tööst ja 1010** tööga, nii et kõik async kliendid teisendatakse klientide sünkroonimiseks Commerce Headquartersis. Kliendihalduse toimingute sünkroonimine toimub iga kord, kui neid töid käitatakse. Lisateavet vt asünkroonse [kliendi loomise režiimist](async-customer-mode.md).

Ettevõtte omanikuna saate teha järgmisi toiminguid:

- Saate vaadata kõiki saidi kasutajate loomise/redigeerimise toiminguid. Üksikasjad hõlmavad olekut ja ajatemplit.
- Filtreerige toimingud, kasutades mis tahes klienditabeli välja ja väärtust auditilogi kitsendamiseks.
- Vaadake muutuste lühikirjeldusi koos oleku üksikasjadega, et mõista operatsioone kõrgel tasemel.
- Tõrke korral redigeerige ja parandage problemaatilised väljad ning seejärel salvestage ja sünkroonige konkreetsed klienditoimingud.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Kliendi sünkroonimise olekulehe elemendid

Kõikide sünkroonimistoimingute loendi vaatamiseks minge Commerce Headquartersi commerce’i ja jaemüügi **klientide \> sünkroonimise \> olekusse**. Järgmine näide kliendi sünkroonimise olekulehe **kohta**

![Kliendi sünkroonimise oleku leht Commerce Headquartersis.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Vaikimisi sisaldavad kliendi sünkroonimise toimingute loend vasakul pool kliendi sünkroonimise **oleku lehte** järgmised veerud:

- Kanali nimi
- Kliendi konto
- Asünkroonne kliendikonto
- Operatsioonide ajatempel
- Kliendi sünkroonimise olek

Lehe ülemisel paremal kuvatakse kliendi konto üksikasjad, nt kliendi **konto**, **jaemüügi asynci** toiming, **kliendi sünkroonimise olek** **ja viimased teadaolevad tõrkeväärtused**.

Muudatuse **kirjelduse jaotis** sisaldab käitatud kliendihalduse operatsiooni tüübi kirjeldust (nt kliendi loomine, konto värskendamine või sünkroonimise nurjumine üksikasjadega).

Jaotises **Kliendi atribuudid on** võrgustik, mis näitab kõiki kliendi atribuute koos vanade ja uute väärtustega. Saate seda jaotist redigeerida, kui soovite muuta oma kliendi atribuudi väärtusi vigaste parandamiseks ja seejärel sünkroonige uuesti.
