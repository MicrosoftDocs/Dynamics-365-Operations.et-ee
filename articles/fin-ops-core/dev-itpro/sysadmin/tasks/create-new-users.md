---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570517"
---
# <a name="create-new-users"></a>Uute kasutajate loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

