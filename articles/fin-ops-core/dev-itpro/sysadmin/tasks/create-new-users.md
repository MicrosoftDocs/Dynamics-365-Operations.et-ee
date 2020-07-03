---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435580"
---
# <a name="create-new-users"></a>Uute kasutajate loomine

[!include [banner](../../includes/banner.md)]

Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Kasutaja seostamine litsentsiga (ainult uued litsentsi tüübid)
Klientidele, kes on ühes uutest litsentsi tüüpidest, mis lisati oktoobris 2019, peavad kasutajad olema litsentsiga seotud. Kasutajad, kes on seotud litsentsiga, lisatakse automaatselt süsteemi kasutajatele, kellel ei ole esimest korda sisselogimisel rolle.

Süsteemi administraatorid saavad [litsentse määrata](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)[Microsoft 365-i administreerimiskeskuse](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) kasutajatele.

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Välise kasutaja seostamine litsentsiga (ainult uued litsentsi tüübid)
Kasutajad, kes on väljaspool rentnikku, milles keskkond kasutusele on võetud, peavad olema esindatud hosti rentniku kataloogis (Azure Active Directory (Azure AD)), et neile saaks määrata litsentsid. Need välised kasutajad tuleb lisada Azure AD's rentnikku külaliskasutajatena ja seejärel määrata vastavad litsentsid. Lisateavet vt teemast [Azure portaalis Azure Active Directory B2B koostöö kasutajate lisamine](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Lisa uus kasutaja
1. Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.
2. Valige toimingupaanil nupp **Uus**.
3. Väljale **Kasutaja ID** saate sisestada küsimustiku kordumatu koodi. Kasutaja ID on kohustuslik.  
4. Sisestage väljale **Kasutajanimi** kasutaja nimi.  
5. Sisestage väljale **Domeen** kasutaja domeen.  
6. Sisestage väljale **Pseudonüüm** kasutaja pseudonüüm.  
7. Väljal **Ettevõte** valige soovitud ettevõte. 
8. Valige kiirkaardil **Kasutaja rollid** turberollide määramiseks kasutajatele suvand **Määra rollid**. Lisainfo saamiseks vt [Kasutajatele turberollide määramine](assign-users-security-roles.md).
9. Valige nupp **OK**.
10. Valige käsk **Salvesta**.

## <a name="import-users"></a>Impordi kasutajad
1. Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.
2. Toimingupaanil valige **Impordi kasutajad**.
3. Märkige loendis valitud rida.
4. Valige **Impordi kasutajad**.
5. Valige suvand **Sule**.

