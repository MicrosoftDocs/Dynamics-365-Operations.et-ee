---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180940"
---
# <a name="create-new-users"></a>Uute kasutajate loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Kasutaja seostamine litsentsiga (ainult uued litsentsi tüübid)
Klientidele, kes on ühes uutest litsentsi tüüpidest, mis lisati oktoobris 2019, peavad kasutajad olema litsentsiga seotud. Kasutajad, kes on seotud litsentsiga, lisatakse automaatselt süsteemi kasutajatele, kellel ei ole esimest korda sisselogimisel rolle. Kasutajad, kes ei ole litsentsiga seotud, saavad hoiatusteate.

Süsteemi administraatorid saavad [litsentse määrata](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)[Microsoft 365-i administreerimiskeskuse](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) kasutajatele.

## <a name="add-a-new-user"></a>Lisa uus kasutaja
1. Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.
2. Valige toimingupaanil nupp **Uus**.
3. Väljale **Kasutaja ID** saate sisestada küsimustiku kordumatu koodi. Kasutaja ID on kohustuslik.  
4. Sisestage väljale **Kasutajanimi** kasutaja nimi.  
5. Sisestage väljale **Domeen** kasutaja domeen.  
6. Sisestage väljale **Pseudonüüm** kasutaja pseudonüüm.  
7. Väljal **Ettevõte** valige soovitud ettevõte. 
8. Vahekaardil **Kasutaja rollid** valige käsk **Määra rollid** [kasutajatele turvalisuse rollide määramiseks.](assign-users-security-roles.md)
9. Valige nupp **OK**.
10. Valige käsk **Salvesta**.

## <a name="import-users"></a>Impordi kasutajad
1. Toimingupaanil valige **Impordi kasutajad**.
2. Märkige loendis valitud rida.
3. Valige **Impordi kasutajad**.
4. Valige suvand **Sule**.

