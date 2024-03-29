---
title: Põhjusekoodide häälestamine
description: Dynamics 365 Human Resources kasutab põhjuse koode, et selgitada, miks töövõtja soodustused muutuvad.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 692bd5acd574492526644849fb555e5856b4463f
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323415"
---
# <a name="set-up-reason-codes"></a>Põhjusekoodide häälestamine

Dynamics 365 Human Resources kasutab põhjuse koode, et selgitada, miks töövõtja soodustused muutuvad.

> [!NOTE]
> Alates 2021. jaanuarist migreeritakse põhjusekoodid tööruumi **Personalihaldus** mitte tööruumi **Soodustuste haldus**. Lisateavet vt teemast [Põhjusekoodide käsitsi migreerimine personalihaldusesse](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Põhjusekoodide loomine

1. Kui teie põhjusekoodid ei ole veel migreeritud valige tööruumis **Personalihaldus** (või tööruumis **Soodustuste haldus**, kui teie põhjusekoodid ei ole veel migreeritud) jaotis **Lingid** ja seejärel valige **Põhjusekoodid**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Põhjuse kood** | Kordumatu nimi, et tuvastada põhjus, miks töövõtja muudaks soodustuse plaani registreerimist. |
   | **Kirjeldus** | Põhjuse koodi kirjeldus. |

4. Seadke jaotises **Rakendatavad stsenaariumid** suvand **Soodustuste haldus** väärtusele **Jah**. (Pole kohaldatav, kui põhjusekoode pole veel tööruumi **Personalihaldus** migreeritud.)

5. Valige käsk **Salvesta**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Põhjusekoodide käsitsi migreerimine Personalihaldusesse

Alates 2021. jaanuarist migreeritakse põhjusekoodid tööruumi **Personalihaldus** mitte tööruumi **Soodustuste haldus**. Enamik põhjusekoodide andmeid migreeritakse automaatselt teie keskkonda. Mõned põhjusekoodide andmed ei pruugi migreeruda. Näiteks on põhjusekoodide suurim lubatud tähemärkide arv 15 märki, seega ei migreerita ühtegi üle 15-tähemärgilist põhjusekoodi automaatselt.

Näete bännerit lehel **Lingid** tööruumis **Soodustuste haldus**, mis teavitab teid migratsioonist ja sellest, kas mõni põhjusekood ei migreerunud.

1. Valige migatsiooni oleku kohta üksikasjade saamiseks **Põhjusekoodid**.

   [![Põhjuse koodid.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Valige põhjusekood, mida ei saanud migreerida.

   [![Põhjusekoodi migreerimise olek.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Valige **Migreeri põhjusekood**.

   [![Migreeri põhjusekood.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. Teil on paanil **Soodustuse põhjusekoodide migreerimine** kaks võimalust Personalihalduse põhjusekoodi vastendamiseks.

   - Olemasoleva põhjusekoodi kasutamiseks Personalihalduses valige üks ripploendist **Kasuta olemasolevat põhjusekoodi**.
     > [!NOTE]
     > Personalihalduses saate kasutada olemasolevat põhjusekoodi ainult siis, kui mõnda muud Soodustuste halduse põhjusekoodi pole juba sinna migreeritud.
   - Personalihalduses uue põhjusekoodi loomiseks sisestage uus põhjusekood väljale **Uus põhjusekood** ja seejärel sisestage kirjeldus väljale **Uus kirjeldus**.

   [![Personalihalduse põhjusekoodile vastendamine.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Kui põhjusekoodid on Personalihaldusse migreeritud, seadistatakse nende kasutamise valiku Soodustuste halduses automaatselt väärtusele **Jah**.

[![Põhjusekoodi kasutamine Soodustuste halduses.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
