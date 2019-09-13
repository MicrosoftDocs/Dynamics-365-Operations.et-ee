---
title: Töökäsule vea lisamine
description: See teema kirjeldab, kuidas lisada vea registreerimisi töökäskudele Varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875614"
---
# <a name="add-fault-to-work-order"></a>Töökäsule vea lisamine

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Vea kujundajas seadistatud vigu saate lisada töökäskudele. Töökäsus valitud vara peab sisaldama varade tüüpe, millega on seotud üks või rohkem veakirjet. Lisateavet häälestuse kohta leiate jaotisest [Veahaldus](../setup-for-work-orders/fault-management.md).

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.

2. Valige loendist töökäsk, milles soovite vea registreerimist teha, ja klõpsake nuppu **Vara viga**.

3. Kiirkaardil **Sümptomid** klõpsake valikut **Lisa rida**. Järjestikune vea number sisestatakse automaatselt **Viga** väljale.

4. Valige sobiv sümptom väljal **Vea sümptom**.

5. Valige **Vea ala** ja **Vea tüüp**.

6. Väljale **Vea kuupäev** lisatakse automaatselt praegune kuupäev. Vajadusel saate valida teise kuupäeva.

7. **Valitud sümptomi põhjused** kiirkaardil lisage probleemi põhjust kirjeldav rida.

8. **Valitud sümptomi parandusmeetmed** kiirkaardil lisage võimalikku probleemi lahendust kirjeldav rida.

9. Klõpsake valikut **Salvesta**.

![Joonis 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Kuva vara vead

**Vara vead** loendis saate ülevaate kõigist vigadest, mis on registreeritud varadesse.

Nimekirja avamiseks klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vead**.


## <a name="print-asset-fault-report"></a>Prindi vara vea aruanne

Loendilehelt **Kõik varad** saate printida vara vea aruande, kus kuvatakse kõik vea registreerimised, samuti vea statistika graafiline ülevaade.

1. Klõpsake **Varahaldus** > **Üldine** > **Varad** > **Kõik varad**.

2. Valige **Varad** loendist vara, mille kohta soovite vea aurannet printida.

3. Vahekaardil **Üldine** > **Aruannete osa** klõpsake **Vara viga**.

4. Sisestage kindel periood või valige vea tüüp.

5. Aruande printimiseks klõpsake **OK**.

>[!NOTE]
>Saate printida ka vea aruande mitme vara või vara tüüpide jaoks, kui klõpsate **Varahaldus** > **Aruanded** > **Varad** > **Vara viga**.

