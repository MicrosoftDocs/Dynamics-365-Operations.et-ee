---
title: Andmete integreerimisprojekti loomine
description: See teema kirjeldab, kuidas luua andmete integreerimisprojekti.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: 7841f8b31e0ac1a40dce9acaac747f5f378236e0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752660"
---
# <a name="create-a-data-integration-project"></a>Andmete integreerimisprojekti loomine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See teema kirjeldab, kuidas luua andmete integreerimisprojekti.

1. Rakenduse Microsoft Dynamics 365 Finance sisselogimine.
2. Minge jaotisse **Tööruumid \> Andmehaldus** ja valige suvand **Andmeüksused**. Oodake, kuni kõik andmeüksused on värskendatud, enne kui liigute järgmisele etapile.
3. Avage [Power Apps i portaal](https://make.powerapps.com/) ja järgige järgmisi etappe.

    1. Valige sobiv keskkond.
    2. Valige vasakul navigeerimispaanil **Dataverse\> ühendus**.
    3. Looge ühendus järgmiste üksuste vastavate eksemplaridega.

        - Dynamics 365
        - Dynamics 365 Findance and Operationsi jaoks

4. Avage [Power Apps i keskkonnad](https://admin.powerapps.com/environments) ja järgige järgmisi etappe.

    1. Valige **andmete integreerimine**.
    2. Valige suvand **Ühenduskomplektid**.
    3. Valige suvand **Uus ühenduskomplekt**.
    4. Sisestage ühenduse nimi.
    5. Valige järgmiste üksuste jaoks sobivad ühendused.

        - Dynamics 365
        - Dynamics 365 Findance and Operationsi jaoks

    6. Valige sobiv organisatsiooni vastendus.
    7. Valige **Loo**.

5. Avage [Power Apps i keskkonnad](https://admin.powerapps.com/environments) ja järgige järgmisi etappe.  

    1. Looge järgmiste mallide jaoks andmeintegratsiooni projektid, kasutades äsja loodud ühenduse komplekti.

        - Kliendi makse vihjete tulemus (CDS fini ja Ops 10.0.17+)
        - Rahavoo ajaseeria tulemid (CDS-ist Finance and Operationsisse)
        - Eelarve ajaseeria tulemid (CDS-ist Finance and Operationsisse)

    2. Määrake igale projektile sobiv ajastamine.

> [!NOTE]
> Kui te nõutavaid üksusi CDS-is ei näe, avage suvand **Krediidihaldus ja võlanõuded > Seadistus > Finantsülevaated > Finantsülevaadete parameetrid**, lubage kliendimakse prognooside funktsioon ja klõpsake nuppu **Loo prognoosimise mudel**. Kui AI-mudeli juurutamine on lõpetatud (edukas või nurjunud), juurutatakse CDS-is olemid, mis on vajalikud integratsiooni loomiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
