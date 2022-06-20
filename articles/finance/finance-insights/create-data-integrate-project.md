---
title: Andmete integreerimisprojekti loomine
description: See artikkel selgitab, kuidas luua andmete integreerimisprojekti.
author: ShivamPandey-msft
ms.date: 05/06/2022
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
ms.openlocfilehash: 4ff4f88c6c5d55d853aebd7d437bfb107292fb2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876236"
---
# <a name="create-a-data-integration-project"></a>Andmete integreerimisprojekti loomine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas luua andmete integreerimisprojekti.

1. Microsoft Dynamics 365 Finantsid: sisselogimine.
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

    1. Looge üks andmete integreerimisprojekt iga järgmise malli jaoks, kasutades äsja loodud ühenduskomplekti:

        - Kliendi makse vihjete tulemus (CDS fini ja Ops 10.0.17+)
        - Rahavoo ajaseeria tulemid (CDS-ist Finance and Operationsisse)
        - Eelarve ajaseeria tulemid (CDS-ist Finance and Operationsisse)

      > [!NOTE]
      > Mitme andmete integreerimisprojekti loomine igale mallile võib põhjustada tõrkeid, mis blokeerivad uuendused.

    2. Määrake igale projektile sobiv ajastamine.

> [!NOTE]
> Kui te ei Dataverse näe nõutavaid üksusi, **minge kreediti ja sissenõuete häälestusprogrammi** > **·** > **·** > **Finance Insights** Finance vihjete parameetrid, lubage funktsioon, **kliendimakse** prognoosid ja seejärel valige suvand Loo **prognoosimudel.** Kui AI-mudeli juurutamine on lõpetatud, Dataverse juurutatakse integratsiooni loomiseks vajalikud üksused.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
