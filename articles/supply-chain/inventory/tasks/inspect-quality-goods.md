---
title: Kaupade kvaliteedi kontrollimine
description: See artikkel kirjeldab, kuidas kvaliteettellimusi töödelda.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eeb14a3b0a61f34819bdd8d524e65ac214a81c35
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857572"
---
# <a name="inspect-the-quality-of-goods"></a>Kaupade kvaliteedi kontrollimine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas kvaliteettellimusi töödelda. Kvaliteedikontrolle teeb üldjuhul kvaliteediametnik.

Kui standardne demoandmed on installitud, saate seda kasutada selle artikli protseduuride lõpule viimiseks. Demoandmete kasutamiseks peate valima ka juriidilise isiku *USMF-i*. Seejärel peate kinnitama ostutellimuse *000016* ja sisestama toote vastuvõtu. Kvaliteeditellimus luuakse automaatselt.

## <a name="step-1-select-a-quality-order"></a>Samm 1. Kvaliteettellimuse valimine

Kvaliteeditellimuse valimiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.
1. Valige kvaliteettellimus, mis loodi enne selle protseduuri käivitamist.

## <a name="step-2-record-test-results"></a>Samm 2. Testitulemuste salvestamine

Testitulemuste salvestamiseks tehke järgmist.

1. Valige **Tulemid**.
1. Valige suvand **Redigeeri**.
1. Sisestage number väljale **Tulemuse kogus**.
1. Valige väljal **Tulemus** soovitud ettevõte. Selles näites põhineb tulemus eelmääratletud tulemusel. Tavaliselt saate salvestada täpsema katse tulemuse, nt suuruse või muu dimensiooni.
1. Valige käsk **Salvesta**.
1. Sulgege leht.

## <a name="step-3-validate-the-quality-order"></a>3. samm. Kvaliteettellimuse õigsuse kontrollimine

Kvaliteeditellimuse valideerimiseks tehke järgmist.

1. Valige **Kinnita**.
1. Valige väljal **Valideerija** kasutaja, kes inspektsiooni läbi viib.
1. Valige käsk **Vali**.
1. Valige nupp **OK**.
1. Sulgege leht.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
