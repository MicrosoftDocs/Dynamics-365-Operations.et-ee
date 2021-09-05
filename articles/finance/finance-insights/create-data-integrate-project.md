---
title: Andmeintegraatori projekti loomine
description: See teema selgitab, kuidas luua andmeintegraatori projekti.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: b08af906c18f6c0790ca56c69a833733f48cd88c
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386358"
---
# <a name="create-a-data-integrator-project"></a>Andmeintegraatori projekti loomine

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas luua andmeintegraatori projekti.

1. Rakenduse Microsoft Dynamics 365 Finance sisselogimine.
2. Minge jaotisse **Tööruumid \> Andmehaldus** ja valige suvand **Andmeüksused**. Oodake, kuni kõik andmeüksused on värskendatud, enne kui liigute järgmisele etapile.
3. Avage [Power Appsi portaal](https://make.powerapps.com/) ja järgige järgmisi etappe.

    1. Valige sobiv keskkond.
    2. Valige vasakpoolselt navigeerimispaanilt suvand **Andmed \> Ühendused**.
    3. Looge ühendus järgmiste üksuste vastavate eksemplaridega.

        - Dynamics 365
        - Dynamics 365 Findance and Operationsi jaoks

4. Avage [Power Appsi keskkonnad](https://admin.powerapps.com/environments) ja järgige järgmisi etappe.

    1. Valige **Andmeintegraator**.
    2. Valige suvand **Ühenduskomplektid**.
    3. Valige suvand **Uus ühenduskomplekt**.
    4. Sisestage ühenduse nimi.
    5. Valige järgmiste üksuste jaoks sobivad ühendused.

        - Dynamics 365
        - Dynamics 365 Findance and Operationsi jaoks

    6. Valige sobiv organisatsiooni vastendus.
    7. Valige **Loo**.

5. Avage [Power Appsi keskkonnad](https://admin.powerapps.com/environments) ja järgige järgmisi etappe.  

    1. Looge järgmiste mallide jaoks andmeintegratsiooni projektid, kasutades äsja loodud ühenduse komplekti.

        - Kliendimakse ülevaadete tulemused (CDS-ist Finance and Operationsisse)
            - Kui kasutate versiooni 10.0.17 või uuemat versiooni, peate kasutama malli nimega Kliendi makseülevaadete tulemus (CDS kuni Fin ja Ops 10.0.17+).
        - Rahavoo ajaseeria tulemid (CDS-ist Finance and Operationsisse)
        - Eelarve ajaseeria tulemid (CDS-ist Finance and Operationsisse)

    2. Määrake igale projektile sobiv ajastamine.

> [!NOTE]
> Kui te nõutavaid üksusi CDS-is ei näe, avage suvand **Krediidihaldus ja võlanõuded > Seadistus > Finantsülevaated > Finantsülevaadete parameetrid**, lubage kliendimakse prognooside funktsioon ja klõpsake nuppu **Loo prognoosimise mudel**. Kui AI-mudeli juurutamine on lõpetatud (edukas või nurjunud), juurutatakse CDS-is olemid, mis on vajalikud integratsiooni loomiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
