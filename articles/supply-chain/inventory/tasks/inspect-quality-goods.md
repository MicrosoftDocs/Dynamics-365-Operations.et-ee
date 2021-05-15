---
title: Kaupade kvaliteedi kontrollimine
description: Selles teemas selgitatakse, kuidas kvaliteettellimusi töödelda.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956130"
---
# <a name="inspect-the-quality-of-goods"></a>Kaupade kvaliteedi kontrollimine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas kvaliteettellimusi töödelda. Kvaliteedikontrolle teeb üldjuhul kvaliteediametnik.

Kui standardsed demoandmed on installitud, saate seda kasutada selle teema protseduuride lõpule viimiseks. Demoandmete kasutamiseks peate valima ka juriidilise isiku *USMF-i*. Seejärel peate kinnitama ostutellimuse *000016* ja sisestama toote vastuvõtu. Kvaliteeditellimus luuakse automaatselt.

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
