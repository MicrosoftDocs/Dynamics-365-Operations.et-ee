---
title: Kasutajat ei leitud Attractis või Onboardis inimeste valijast
description: Selles teemas selgitatakse, mida teha, kui ettevõtte rentnikus olevaid kasutajaid ei kuvata rakendustes Dynamics 365 for Talent Attract või Onboard inimeste valijas.
author: ChrisChua
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: chrichua
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2d4a74ee2cc65153c1f9fdc1b42c2fc440d188d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304112"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Azure Active Directory kasutajaid ei leitud inimeste valijast

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Väljastamine

Microsoft Azure Active Directorys (Azure AD) ei kuvata rentniku puhul teatud kehtivaid kasutajaid, kui rakenduses Dynamics 365 for Talent Attract või Onboard otsitakse inimeste valijas kasutajaid nime järgi.

## <a name="cause"></a>Põhjus

Rakendused Attract ja Onboard ei toeta praegu teatud kasutajatüüpe. Veenduge, et kasutaja ei oleks lahenduse Azure AD Business to Business (B2B) külaliskasutaja. Kasutaja tüübi teabe leiate Azure’i portaalis Azure Active Directory labal.

Lisateavet Azure B2B kohta vt teemast [Mis on külaliskasutaja juurdepääs Azure Active Directory B2B-s](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

Mitte-B2B kasutajate puhul on olemas teatud kasutajad, kellel võib olla objektis **Kasutaja** puudulik atribuut Kasutaja tüüp. Seda saab kontrollida ja parandada Azure AD mooduliga Powershell. Lisateavet vt [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Eraldusvõime

Probleemi lahendamiseks tuleb teha järgmised toimingud ja selleks peavad teil olema Azure Active Directory rentnikus üldadministraatori õigused või õigused **User.ReadWrite.All**.

Mõjutatud kasutaja atribuudi Kasutaja tüüp kontrollimine.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Käsk tagastab järgmise teabe.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Vaadake kasutaja atribuuti **Kasutaja tüüp**. Kui atribuut **Kasutaja tüüp** on tühi, olemata näiteks Liige või Külaline, värskendage atribuuti **Kasutaja tüüp** järgmist käsku kasutades.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```