---
title: Andmete integreerimisprojekti loomine
description: See teema kirjeldab, kuidas luua andmete integreerimisprojekti.
author: ShivamPandey-msft
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 50f435f9d461667a1908baa529d73766085c183a
ms.sourcegitcommit: 6526acd0300d9c5800d3d7675d54e23090d031df
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2022
ms.locfileid: "8107283"
---
# <a name="create-a-data-integration-project"></a>Andmete integreerimisprojekti loomine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua andmete integreerimisprojekti.

1. Rakenduse Microsoft Dynamics 365 Finance sisselogimine.
2. Minge jaotisse **Tööruumid \> Andmehaldus** ja valige suvand **Andmeüksused**. Oodake, kuni kõik andmeüksused on värskendatud, enne kui liigute järgmisele etapile.
3. Avage [Power Appsi portaal](https://make.powerapps.com/) ja järgige järgmisi etappe.

    1. Valige sobiv keskkond.
    2. Valige vasakul navigeerimispaanil ühendus **Dataverse\>**.
    3. Looge ühendus järgmiste üksuste vastavate eksemplaridega.

        - Dynamics 365
        - Dynamics 365 Findance and Operationsi jaoks

4. Avage [Power Appsi keskkonnad](https://admin.powerapps.com/environments) ja järgige järgmisi etappe.

    1. Valige **andmete integreerimine**.
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

        - Kliendi makse vihjete tulemus (CDS fini ja Ops 10.0.17+)
        - Rahavoo ajaseeria tulemid (CDS-ist Finance and Operationsisse)
        - Eelarve ajaseeria tulemid (CDS-ist Finance and Operationsisse)

    2. Määrake igale projektile sobiv ajastamine.

> [!NOTE]
> Kui te Dataverse ei näe nõutavaid üksusi, **minge parameetrid Kreedit ja collectionsSetupFinance** > **·** > **InsightsFinance** > **vihjete** parameetrid, lubage funktsioon, **kliendimakse** prognoosid ja seejärel valige suvand **Loo ennustuse mudel.** Kui AI-mudeli juurutamine on lõpetatud, Dataverse juurutatakse integratsiooni loomiseks vajalikud üksused.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
