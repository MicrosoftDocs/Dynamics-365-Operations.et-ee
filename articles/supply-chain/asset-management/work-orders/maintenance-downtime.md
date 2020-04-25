---
title: Hoolduskatkestus
description: Selles teemas kirjeldatakse hoolduskatkestusi varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b4960aea95d63486207699f3bbd7f4b4f3cf0488
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206860"
---
# <a name="maintenance-downtime"></a>Hoolduskatkestus

[!include [banner](../../includes/banner.md)]


Võite luua hoolduskatkestuse registreeringuid töökäsus valitud varale. See funktsioon on kasulik, kui soovite registreerida hoolduskatkestuse ühele või enamale tootmisala masinale. Kõigepealt looge hoolduskatkestuse põhjuse koodid, mida soovite kasutada, näiteks **Katkiminek** ja **Planeeritud seiskamine**. Seda toimingut tehakse lehel **Hoolduskatkestuse põhjuste koodid**. Järgmisena saate luua hoolduskatkestuse registreeringud lehel **Hoolduskatkestus** ja lisada asjakohased hoolduskatkestuse põhjuse koodid.

## <a name="create-maintenance-downtime-reason-codes"></a>Hoolduskatkestuse põhjuse koodide loomine

1. Valige **Varahaldus** > **Seadistus** > **töökäsud** > **Hoolduskatkestuse põhjuse koodid**.

2. Valige suvand **Uus**.

3. Sisestage väljale **Hoolduskatkestuse põhjuse kood** hoolduskatkestuse põhjuse koodi ID.

4. Väljale **Nimi** sisestage nimi.

5. Märkige ruut **KPI sisaldus**, kui põhjuse kood tuleks kaasata vara peamiste tulemusnäitajate (KPI) arvutustesse. Üldiselt ei tulek planeeritud tootmisseisakuid KPI arvutustesse kaasata, sest need ei mõjuta eeldatavat jõudlust.

6. Valige käsk **Salvesta**.

Järgneval joonisel kuvatakse lehe **Hoolduskatkestuse põhjuse koodid** näide.

![Joonis 1](media/15-work-orders.png)

Kui olete loonud need hoolduskatkestuse põhjuse koodid, mida kasutada soovite, saate luua töökäskudele ja varadele hoolduskatkestuse registreeringuid.


## <a name="create-maintenance-downtime-registrations"></a>Hoolduskatkestuse registreeringute loomine

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk ja seejärel tehke vahekaardi **Töökäsk** jaotises **Vara** valik **Hoolduskatkestus**.

3. Valige suvand **Uus**.

4. Määratlege hoolduskatkestuse registreeringu kuupäeva ja kellaaja intervall väljadel **Alates** ja **Kuni**.

>[!NOTE]
>Kui lahkute väljalt **Kuni**, sisestatakse kestvus tundides automaatselt väljale **Kestvus**.

5. Valige põhjuse kood väljal **Hoolduskatkestuse põhjuse kood**.

6. Täiendavate registreeringute lisamiseks korrake samme 3 kuni 5.

7. Valige käsk **Salvesta**.

Alljärgneval joonisel on esitatud hoolduskatkestuse registreerimise näide.

![Joonis 2](media/16-work-orders.png)

Hoolduskatkestuse registreeringuteks kasutatav kalender oleneb teie varade ja parameetrite seadistustes tehtud valikust. Kui varale on valitud ressurss lehe **Kõik varad** kiirkaardi **Põhivara** väljal **Ressurss**, kasutatakse seotud ressursirühma kalendri seadistust, nii nagu näidatud järgmisel joonisel.

![Joonis 3](media/17-work-orders.png)

Kui varale ressurssi valitud ei ole, kasutatakse standardset kalendrit, mis on valitud lehel **Varahalduse parameetrid**, nii nagu näidatud järgmisel joonisel.

![Joonis 4](media/18-work-orders.png)

Kõigi hoolduskatkestuste registreeringute ülevaate vaatamiseks valige **Varahaldus** > **Päringud** > **Hoolduskatkestus**.

>[!NOTE]
>Kõik moodulis **Varahaldus** kasutatud kalendrid seadistatakse jaotises **Organisatsiooni haldus** > **Seadistus** > **Kalendrid** > **Kalendrid**.

