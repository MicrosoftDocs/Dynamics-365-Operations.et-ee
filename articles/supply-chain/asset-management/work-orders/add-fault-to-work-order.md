---
title: Töökäsule vea lisamine
description: See teema kirjeldab, kuidas lisada vea registreerimisi töökäskudele Varahalduses.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a79986e3b477865bc1816a1d28c1b7094ae3974
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809802"
---
# <a name="add-fault-to-work-order"></a>Töökäsule vea lisamine

[!include [banner](../../includes/banner.md)]



Saate lisada töökäsule vea kujundajas seadistatud vigu. Vähemalt üks veakirje peab olema seotud varatüüpidega, mida kasutatakse töökäsus valitud vara korral. Häälestuse kohta leiate lisateavet jaotisest [Veahaldus](../setup-for-work-orders/fault-management.md).

1. Valie **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk, mille kohta registreerida viga ja seejärel valige toimingupaani vahekaardil **Töökäsk** rühma **Vara** alt valik **Vara viga**.

3. Valige kiirkaardil **Sümptomid** valik **Lisa rida**. Järjestikune vea number sisestatakse automaatselt väljale **Viga**.

4. Valige väljal **Vea sümptom** asjakohane sümptom.

5. Valige väljadel **Vea ala** ja **Vea tüüp** asjakohased väärtused.

6. Väljale **Vea kuupäev** lisatakse automaatselt praegune kuupäev. Vajadisel saate valida mõne muu kuupäeva.

7. Lisage kiirkaardil **Valitud sümptomi põhjused** probleemi põhjust kirjeldav rida.

8. Lisage kiirkaardil **Valitud sümptomi parandusmeetmed** probleemi võimalikku lahendust kirjeldav rida.

9. Valige käsk **Salvesta**.

Alljärgneval joonisel on esitatud vea registreerimise näide.

![Joonis 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Kuva vara vead

**Vara vead** loendis saate ülevaate kõigist vigadest, mis on registreeritud varadesse.

Loendilehel **Vara vead** saate ülevaate kõigist vigadest, mis on varade kohta registreeritud. Lehe avamiseks valige **Varahaldus** > **Päringud** > **Vara viga** > **Vara vead**.


## <a name="print-asset-fault-report"></a>Prindi vara vea aruanne

Loendilehelt **Kõik varad** saate printida vara vea aruande, kus kuvatakse kõik vea registreerimised ja veastatistika graafiline ülevaade.

1. Valige **Varahaldus** > **Ühised** > **Varad** > **Kõik varad**.

2. Valige vara, mille kohta printida aruanne.

3. Valige toimingupaani vahekaardil **Üldine** grupis **Aruanded** valikut **Vara viga**.

4. Sisestage konkreetne periood või valige vea tüüp.

5. Aruande printimiseks valige **OK**.

>[!NOTE]
>Veaaruande printimiseks mitme vara või varatüübi kohta valige **Varahaldus** > **Aruanded** > **Varad** > **Vara viga**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]