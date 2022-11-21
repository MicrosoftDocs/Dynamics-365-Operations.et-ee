---
title: Lisage isiku identiteedi pakkujad.
description: See artikkel kirjeldab, kuidas lisada portaali isiku identiteedi pakkujaid Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785800"
---
# <a name="add-social-identity-providers"></a>Lisage isiku identiteedi pakkujad.

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lisada portaali isiku identiteedi pakkujaid Microsoft Azure.

Sotsiaalsed identiteedipakkujad lubavad kasutajatel autentimiseks sotsiaalmeedia kontosid kasutada. Sotsiaalse identiteedipakkuja autentimise lisamine on Dynamics 365 Commerce'i rakenduses valikuline. 

Kui isiku identiteedi pakkuja autentimist ei lisata, Azure Active Directory on teie kasutajabaasi põhiprofiiliks vaikimisi (Azure AD) B2C-profiilid. Kasutajad valivad oma kasutajanime (eelistatud meiliaadressi) ja määravad parooli. Azure AD B2C autendib kasutajaid otse. 

Kui on sotsiaalse identiteedipakkuja autentimine lisatakse ja kasutaja valib ühe pakutava sotsiaalse identiteedipakkuja, luuakse ikkagi üksus Azure AD B2C rentniku jaoks. Azure AD B2C autendib seejärel kasutaja mandaadi sotsiaalse identiteedipakkuja juures.

> [!NOTE]
> Identiteedipakkujaga sisselogimine loob kirje B2C rentnikku, kuidkohalikest kontodest erinevas vormingus, kuna see nõuab autentimiseks välise sotsiaalse identiteedipakkuja viidet. Kasutaja saab kasutada sama meiliaadressi kõigis sotsiaalsetes identiteedipakkujates, mis tähendab, et autentimiseks kasutatav meili kasutajanimi ei pruugi olla rentniku jaoks kordumatu. Azure AD B2C nõuab kasutajatelt on kordumatu meiliaadress kasutamist kohalikel B2C kontodel.

Enne autentimiseks sotsiaalse identiteedipakkuja lisamist, peate pöörduma identiteedipakkuja portaali poole ja häälestama identiteedipakkuja rakenduse Azure AD B2C dokumentatsioonis kirjeldatud juhiste järgi. Allpool on esitatud linkide loend dokumentidele juurde pääsemiseks.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Üksik rentnik)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsofti konto](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Sotsiaalse identiteedipakkuja lisamine ja seadistamine

> [!NOTE]
> Sotsiaalidentimise pakkujate lisamine on valikuline samm ettevõtte ja tarbija (B2C) rentniku seadistamisel Microsoft Dynamics 365 Commerce.

Sotsiaalse identiteedipakkuja lisamiseks ja seadistamiseks toimige järgmiselt.  

1. Azure'i portaalis liikuge jaotisesse **Identiteedipakkujad**.
1. Valige **Lisa**. Kuvatakse aken **Identiteedipakkuja lisamine**.
1. Sisestage **jaotises** Nimi kasutajatele kuvatav nimi.
1. Valige jaotises **Identiteedipakkuja tüüp** loendist identiteedipakkuja.
1. Valige nupp **OK**.
1. Valige **Selle identiteedipakkuja häälestamine** aknale **Sotsiaalse identiteedipakkuja häälestamine** juurde pääsemiseks.
1. Jaotises **Kliendi ID** sisestage kliendi ID, mille saite identiteedipakkuja rakenduse häälestamisel.
1. Jaotises **Kliendi saladus** sisestage kliendi saladus, mille saite identiteedipakkuja rakenduse häälestamisel.
1. Lisage kasutajavoog sisselogimise/registreerumise poliitikatele.
1. Avage jaotis **Azure AD B2C – kasutajavood (poliitikad) \> {teie sisselogimise registreerumise poliitika} \> Identiteedipakkujad**.
1. Kasutajavoo poliitika seostamiseks sisselogimise/registreerumise poliitikaga valige iga identiteedipakkuja, mille olete oma kontole seadistanud. Voogude testimiseks valige iga **identiteedipakkuja jaoks** suvand Käivita kasutajavoog. Uus vahekaart kuvab uue identiteedipakkuja valikuboksi kuvava sisselogimislehe.

Järgmisel pildil kuvatakse näited akende **Identiteedipakkuja lisamine** ja **Sotsiaalse identiteedipakkuja häälestamine** kohta Azure AD B2C-s.

![Sotsiaalse identiteedipakkuja lisamine rakendusse.](./media/B2CImage_14.png)

Järgmisel pildil kuvatakse näide, kuidas valida identiteedipakkujaid Azure AD B2C lehel **Identiteedipakkujad**.

![Valige kõik enda poliitika jaoks lubatavad sotsiaalse identiteedi pakkujad.](./media/B2CImage_16.png)

Järgmisel pildil kuvatakse näide vaikimisi sisselogimisaken, millel on sotsiaalse identiteedipakkuja sisselogimisnupp.

> [!NOTE]
> Kui kasutate oma kasutajavoogude jaoks teenuses Commerce sisseehitatud kohandatud lehti, tuleb sotsiaalse identiteedi pakkujate nupud lisada Commerce'i mooduli teegi laiendamisfunktsioonide abil. Lisaks, kui seadistate avaldusi kindla isiku identiteedi pakkujaga, võib mõnel juhul URL või konfiguratsioonistring olla tõstutundlik. Lisateabe saamiseks vaadake oma isiku identiteedi pakkuja ühendusjuhiseid.
 
![Näide vaikimisi sisselogimisaknast sotsiaalse identiteedipakkuja sisselogimisnupuga.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Järgmised sammud

Äri rentniku B2C-rentniku seadistamise jätkamiseks jätkake [Commerce headquartersi uuendamist Azure AD uue B2C-teabega](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Lisaressursid

[Jaekaubandusrentniku häälestamine Commerce'is](set-up-b2c-tenant.md)

[Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.](create-link-aad-b2c-tenant.md)

[B2C rakenduse loomine](create-b2c-app.md)

[Kasutajavoo poliitikate loomine](create-user-flow-policies.md)

[Commerce headquartersi värskendamine uue Azure AD B2C-teabega](update-hq-aad-b2c-info.md)

[B2C rentniku konfigureerimine kaubanduse saidiehitajas](config-b2c-tenant-site-builder.md)

[Lisateave B2C kohta](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
