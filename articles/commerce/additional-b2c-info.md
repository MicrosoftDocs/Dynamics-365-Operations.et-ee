---
title: Lisateave B2C kohta
description: See artikkel annab täiendavat teavet selle kohta, kuidas seadistada oma ettevõtte tarbimist (B2C) rentnikku Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785799"
---
# <a name="additional-b2c-information"></a>Lisateave B2C kohta

[!include [banner](includes/banner.md)]

See artikkel annab täiendavat teavet selle kohta, kuidas seadistada oma ettevõtte tarbimist (B2C) rentnikku Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>Kliendi migreerimine

Kui soovite migreerida kliendikirjeid eelmisest identiteedipakkuja platvormist, siis tehke koostööd Dynamics 365 Commerce meeskonnaga oma klientide migratsiooni vajaduste ülevaatamiseks.

Täiendava Azure AD B2C dokumentatsiooni hankimiseks klientide migratsiooni kohta vaadake teemat [Kasutajate migreerimine Azure Active Directory B2C-sse](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Kohandatud poliitikad

Täiendava teabe saamiseks Azure AD B2C suhtlus- ja poliitikavoogude kohandamise kohta, mis ei kuulu B2C standardpoliitikasse, vaadake teemat [Kohandatud poliitikad Azure Active Directory B2C-s](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Teisene administraator

Teie B2C rentnikku on valikuliselt võimalik lisada teisene administraatorikonto jaotises **Kasutajad**. See võib olla otsene või üldine konto. Kui teil on vaja jagada kontot meeskonnaressursside üleselt, saate luua ka ühise konto. Azure AD B2C-s talletatavate andmete tundlikkuse tõttu tuleb ühist kontot hoolikalt jälgida vastavalt teie ettevõtte turvalisuse tavadele.

### <a name="set-up-a-custom-sign-in-domain"></a>Kohandatud sisselogimisdomeeni loomine

Azure AD B2C võimaldab teil seadistada B2C rentniku jaoks kohandatud Azure AD sisselogimise domeeni. Juhiseid vt B2C [kohandatud domeenide Azure Active Directory lubamine](/azure/active-directory-b2c/custom-domain). 

Kui kasutate kohandatud sisselogimisdomeeni, tuleb domeen sisestada Commerce’i saidiloojasse.

Kohandatud sisselogimise domeeni sisestamiseks saidikonstruktoris järgige neid samme.

1. Saidikonstruktori ülemises parempoolses nurgas valige saidilüliti ja seejärel valige suvand Halda **saite**.
1. Valige vasakul navigeerimispaanil rentniku sätete **saidi autentimise \> häälestus**.
1. Valige jaotises **Saidi autentimise profiilid** suvand **Haldamine**.
1. Paremmenüüs väljaminek valige nupp Redigeeri **(sümbol), mis on seotud saidi autentimisprofiiliga,** mille jaoks soovite sisestada kohandatud domeeni.
1. Sisestage **kohandatud domeeni sisselogimisdomeeni** **väljale** Saidi autentimisprofiili redigeerimine (nt login.fabrikam.com).

> [!WARNING]
> Kui uuendate B2C rentniku Azure AD kohandatud domeeni, mõjutab muudatus loodud loa rentniku väljastaja üksikasju. Väljastaja üksikasjad kaasavad siis B2C-ga antud vaikedomeeni Azure AD asemel kohandatud domeeni. Erinev väljastaja **konfiguratsioon** Commerce headquartersis (**Retail ja Commerce \> Headquartersi \> häälestamise parameetrid Commerce shared parameters \>\> Identity Providers**) muudab süsteemi suhtlust saidi kasutajatega ja võib luua potentsiaalselt uue kliendikirje, kui kasutaja on autentinud uue väljastaja suhtes. Kohandatud domeenimuudatusi tuleb enne kohandatud domeeni lülitumist B2C keskkonnas põhjalikult Azure AD katsetada.

## <a name="additional-resources"></a>Lisaressursid

[Jaekaubandusrentniku häälestamine Commerce'is](set-up-b2c-tenant.md)

[Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.](create-link-aad-b2c-tenant.md)

[B2C rakenduse loomine](create-b2c-app.md)

[Kasutajavoo poliitikate loomine](create-user-flow-policies.md)

[Sotsiaalstete identiteedipakkujate lisamine (valikuline)](add-social-identity-providers.md)

[Commerce headquartersi värskendamine uue Azure AD B2C-teabega](update-hq-aad-b2c-info.md)

[B2C rentniku konfigureerimine kaubanduse saidiehitajas](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
