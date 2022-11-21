---
title: Kasutajavoo poliitikate loomine
description: See artikkel kirjeldab, kuidas portaalis kasutajavoo poliitikaid Microsoft Azure luua.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785803"
---
# <a name="create-user-flow-policies"></a>Kasutajavoo poliitikate loomine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas portaalis kasutajavoo poliitikaid Microsoft Azure luua.

Kasutajavood on poliitikad Azure Active Directory (Azure AD) ettevõttelt tarbijale (B2C) kasutab turvalise sisselogimise, sisselogimise, profiili redigeerimise ja parooli kasutajakogemuste unustamiseks. Dynamics 365 Commerce kasutab neid voogusid et poliitikaga seonduvate toimingute tegemiseks Azure AD B2C rentnikuga suhtlemisel. Kui kasutaja nende poliitikatega suhtleb, suunatakse ta Azure AD ümber B2C rentnikule nende toimingute sooritamiseks.

Azure AD B2C pakub kolme peamist kasutajavoo tüüpi.
- Registreerimine ja sisselogimine
- Profiili redigeerimine
- Parooli lähtestamine

Võite kasutada vaikimisi antud kasutajavoogusid Azure AD, mis kuvavad B2C majutatud Azure AD lehe. Saate ka luua HTML-lehe, et juhtida nende kasutajavoo kogemuste välimust ja olemust. 

Kasutajapoliitika lehtede kohandamiseks Dynamics 365 Commerce'is ehitatud lehtedega vaadake teemat [Kohandatud lehtede häälestamine kasutaja sisselogimisteks](custom-pages-user-logins.md). Lisateavet vt B2C [kasutajakogemuste liidese Azure Active Directory kohandamisest](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Looge registreerumise ja sisselogimise kasutajavoo poliitika.

Registreerumise ja kasutajavoo poliitikasse sisselogimiseks järgige neid samme.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Valige poliitika **Registreerimine ja sisselogimine** ja seejärel **Soovitatud** versioon.
1. Sisestage poliitika nimi väljale **Nimi**. See nimi kuvatakse hiljem koos eesliitega, mille portaal määrab (nt „B2C_1_”).
1. Jaotise **Identiteedi pakkujad** jaotises Kohalikud **kontod** valige e-kirjaga **registreerimine**. Meili autentimist kasutatakse Rakenduse Commerce kõige tavalisemates stsenaariumides. Kui kasutate ka isiku identiteedi pakkuja autentimist, saate need valida ka praegu.
1. Valige sobiv ettevõtte valik jaotises **Mitmikautentimine**. 
1. Jaotises **Kasutaja atribuudid ja nõuded** valige suvandid atribuutide kogumiseks või nõuete tagastamiseks vastavalt vajadusele. Valige **käsk Kuva rohkem ...** atribuutide ja nõuete suvandite täieliku loendi saamiseks. Commerce nõuab järgmisi vaikesätteid.

    | **Atribuudi kogumine** | **Nõude tagastamine** |
    | ---------------------- | ----------------- |
    | Meiliaadress          | Meiliaadressid   |
    | Eesnimi             | Eesnimi        |
    |                        | Identiteedipakkuja |
    | Perekonnanimi                | Perekonnanimi           |
    |                        | Kasutaja objekti ID  |

1. Valige **Loo**.

Järgmine pilt on näide B2C-ga Azure AD registreerumise ja kasutajavoo sisse logimise kohta.

![Registreerimise ja sisselogimise poliitika sätted.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Profiili loomine kasutajavoo poliitika redigeerimisel

Profiili redigeerimise kasutajavoo poliitika loomiseks toimige järgmiselt.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Valige **Profiili redigeerimine** ja seejärel valige **soovitatav** versioon.
1. Jaotises **Nimi** sisestage profiil kasutajavoogu redigeerides. See nimi kuvatakse hiljem koos eesliitega, mille portaal määrab (nt „B2C_1_”).
1. Jaotise **Identiteedi pakkujad** jaotises Kohalikud **kontod** valige Meiliaadress **SignIn**.
1. Jaotises **Kasutaja atribuudid** märkige järgmised ruudud.
    
    | **Atribuudi kogumine** | **Nõude tagastamine** |
    | ---------------------- | ----------------- |
    |                        | Meiliaadressid   |
    | Eesnimi             | Eesnimi        |
    |                        | Identiteedipakkuja |
    | Perekonnanimi                | Perekonnanimi           |
    |                        | Kasutaja objekti ID  |
    
1. Valige **Loo**.

Järgmine pilt on Azure AD B2C profiili redigeerimise kasutajavoo näide.

![Azure AD Näide B2C-profiili redigeerimise kasutajavoost](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Parooli lähtestamise kasutajavoo poliitika loomine

Parooli lähtestamiseks kasutajavoo poliitikas toimige järgmiselt.

1. Tehke Azure'i portaali vasakpoolsel navigeerimispaanil valik **Kasutajavood (poliitikad)**.
1. Lehel **Azure AD B2C – kasutajavood (poliitikad)** valige **Uus kasutajavoog**.
1. Valige **Parooli lähestamine** ja seejärel valige **soovitatav** versioon.
1. Jaotises **Nimi** sisestage parooli lähtestamise kasutajavoo nimi.
1. Jaotises **Identiteedipakkujad** valige suvand **Parooli lähtestamine meiliaadressi kasutades**.
1. Valige **Loo**.
1. Jaotises **Rakenduse nõuded** märkige järgmised ruudud.
    - **Meiliaadressid**
    - **Eesnimi**
    - **Perekonnanimi**
    - **Kasutaja objekti ID**
1. Valige **Loo**.

Järgmisel pildil näidatakse, kuhu seada **Lähtesta parool meiliaadressi abil** Azure AD B2C parooli lähtestamise kasutajavoos.

![„Lähtesta parool meiliaadressi abil” sätestamine parooli lähtestamise poliitikas](./media/B2CImage_13.png)

## <a name="next-steps"></a>Järgmised sammud

B2C rentniku seadistamise jätkamiseks Äris jätkake käsku Lisa isikuidentimise [pakkujad](add-social-identity-providers.md).

## <a name="additional-resources"></a>Lisaressursid

[Jaekaubandusrentniku häälestamine Commerce'is](set-up-b2c-tenant.md)

[Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.](create-link-aad-b2c-tenant.md)

[B2C rakenduse loomine](create-b2c-app.md)

[Sotsiaalstete identiteedipakkujate lisamine (valikuline)](add-social-identity-providers.md)

[Commerce headquartersi värskendamine uue Azure AD B2C-teabega](update-hq-aad-b2c-info.md)

[B2C rentniku konfigureerimine kaubanduse saidiehitajas](config-b2c-tenant-site-builder.md)

[Lisateave B2C kohta](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
