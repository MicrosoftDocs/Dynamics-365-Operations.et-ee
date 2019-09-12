---
title: Hoolduskatkestus
description: Selles teemas kirjeldatakse hoolduskatkestusi varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918240"
---
# <a name="maintenance-downtime"></a>Hoolduskatkestus


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Võite luua hoolduskatkestuse registreeringuid töökäsus valitud varale. See on kasulik, kui soovite registreerida hoolduskatkestuse ühele või enamale tootmisala masinale. Kõigepealt loote hoolduskatkestuse põhjuse koodid, mida soovite kasutada, näiteks katkiminek ja planeeritud seiskamine. Seda tehakse jaotises **Hoolduskatkestuse põhjuste koodid**. Järgmisena loote hoolduskatkestuse registreeringud jaotises **Hoolduskatkestus** ja lisate asjakohase põhjuse koodid.

## <a name="create-maintenance-downtime-reason-codes"></a>Hoolduskatkestuse põhjuse koodide loomine

1. Klõpsake suvandil **Varahaldus** > **Seadistus** > **töökäsud** > **Hoolduskatkestuse põhjuse koodid**.

2. Klõpsake valikut **Uus**.

3. Sisestage ID väljale **Hoolduskatkestuse põhjuse kood**.

4. Sisestage põhjuse koodi nimi väljale **Nimi**.

5. Valige märkeruut **KPI sisaldus**, kui põhjuse kood peaks sisalduma vara KPI arvutustes. Üldiselt ei peaks planeeritud tootmisseisakuid KPI arvutustesse kaasama, sest need ei mõjuta oodatavat jõudlust.

6. Klõpsake valikut **Salvesta**.

![Joonis 1](media/15-work-orders.png)


Kui olete loonud need hoolduskatkestuse põhjuse koodid, mida kasutada soovite, saate luua töökäskudele ja varadele hoolduskatkestuse registreeringuid.


## <a name="create-maintenance-downtime-registrations"></a>Hoolduskatkestuse registreeringute loomine

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk ja klõpsake **Hoolduskatkestus**.

3. Klõpsake valikut **Uus**.

4. Sisestage hoolduskatkestuse registreeringu kuupäeva ja kellaaja intervall väljadele **Alates** ja **Kuni**.

5. Kui lahkute väljalt **Kuni**, sisestatakse kestvus tundides automaatselt väljale **Kestvus**.

6. Sisestage põhjuse kood väljale **hoolduskatkestuse põhjuse kood**.

7. Kui soovite lisada rohkem registreeringuid, korrake ülaltoodud juhiseid 3–6.

8. Klõpsake valikut **Salvesta**.


![Joonis 2](media/16-work-orders.png)


Hoolduskatkestuse registreeringuteks kasutatav kalender oleneb teie varade ja parameetrite seadistustes tehtud valikust. Kui varale on valitud ressurss jaotise **Kõik varad** > **Põhivara** kiirkaardil > väljal **Ressurss**, kasutatakse seotud ressursirühma kalendri seadistust, nii nagu näidatud järgmisel joonisel.

![Joonis 3](media/17-work-orders.png)


Kui varale ressurssi valitud ei ole, kasutatakse standardset kalendrit, mis on valitud jaotises **Varahalduse parameetrid**, nii nagu näidatud järgmisel joonisel.

![Joonis 4](media/18-work-orders.png)


Klõpsake **Ettevõtte varahaldus** > **Päringud** > **Hoolduskatkestus**, et näha kõigi hoolduskatkestuste registreeringute ülevaadet.

>[!NOTE]
>Kõik moodulis **Varahaldus** kasutatud kalendrid seadistatakse jaotises **Organisatsiooni haldus** > **Seadistus** > **Kalendrid** > **Kalendrid**.

