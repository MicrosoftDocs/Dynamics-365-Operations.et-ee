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
ms.openlocfilehash: b881f9c6f872061864d4254ce880d981ca71c479
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219030"
---
# <a name="inspect-the-quality-of-goods"></a>Kaupade kvaliteedi kontrollimine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas kvaliteettellimusi töödelda. Kvaliteedikontrolle teeb üldjuhul kvaliteediametnik.

Kui standardne [demoandmed](../../../fin-ops-core/fin-ops/get-started/demo-data.md) on installitud, saate seda kasutada selle artikli protseduuride lõpule viimiseks. Demoandmete kasutamiseks peate valima ka juriidilise isiku *USMF-i*. Seejärel peate kinnitama ostutellimuse *000016* ja sisestama toote vastuvõtu. Kvaliteeditellimus luuakse automaatselt.

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
