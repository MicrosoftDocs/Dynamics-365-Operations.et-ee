---
title: B2C rentniku konfigureerimine kaubanduse saidiehitajas
description: See artikkel kirjeldab, kuidas konfigureerida oma ettevõtte tarbimist (B2C) rentnikku saidikonstruktoris Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785804"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>B2C rentniku konfigureerimine kaubanduse saidiehitajas

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas konfigureerida oma ettevõtte tarbimist (B2C) rentnikku saidikonstruktoris Microsoft Dynamics 365 Commerce.

Kui teie Azure AD B2C rentniku häälestus on lõpule viidud, tuleb konfigureerida B2C rentnik kaubanduse saidiehitajas. Konfiguratsioonietapid hõlmavad B2C rakenduse teabe kogumist Azure'i portaalist, selle B2C rakenduse teabe sisestamist saidiehitajasse ja seejärel B2C rakenduse seostamist teie saidi ja kanaliga.

### <a name="collect-the-required-application-information"></a>Nõutava rakenduseteabe kogumine

Nõutava rakenduseteabe kogumiseks toimige järgmiselt.

1. Avage Azure’i portaalis **Home \>Azure AD B2C – rakenduse registreerimised**.
1. Valige oma rakendus ja seejärel valige vasakul navigeerimispaanil **Rakenduse** üksikasjade saamiseks Ülevaade.
1. Koguge **rakenduse (kliendi) ID viitest teie B2C rentnikus loodud B2C-rakenduse rakenduse ID**. See sisestatakse hiljem saidiehitajas väärtuseks **Kliendi GUID**.
1. Valige **ümbersuunamise URL-id** ja koguge oma saidi kohta kuvatud vastuse URL (häälestusel sisestatud vastuse URL).
1. Minge avalehele **\>Azure AD B2C – kasutajavood** ja koguge seejärel iga kasutajavoo poliitika täisnimed.

Järgmine pilt näitab näidet **Azure AD B2C - rakenduse registreerimiste ülevaatelehe** kohta.

![Azure AD B2C – rakenduse registreerimiste ülevaateleht, kus on esile tõstetud rakenduse (kliendi) ID](./media/ClientGUID_Application_AzurePortal.png)

Järgmisel pildil kuvatakse näide kasutajavoo poliitikatest lehel **Azure AD B2C – kasutajavood (poliitikad)**.

![Kõigi B2C poliitikavoo nimede kogumine.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Sisestage oma Azure AD B2C rentniku rakenduse teave rakendusse Commerce

Enne B2C rentniku seostamist oma saitidega, peate sisestama Azure AD B2C rentniku andmed kaubanduse saidiehitajasse.

Oma B2C Azure AD rentniku rakenduse teabe lisamiseks Commerce’ile järgige neid samme.

1. Logige sisse administraatorina oma keskkonna kaubanduse saidiehitajasse.
1. Vasakpoolsel navigeerimispaanil valige suvand **Rentniku sätted** selle laiendamiseks.
1. Valige jaotises **Rentniku** sätted saidi **autentimise häälestus**. 
1. Valige põhiaknas saidi autentimise **profiilide kõrval** suvand **Manage (Halda**). (Kui teie rentnik ilmub saidi autentimise profiilide loendisse, lisas administraator selle juba. Kontrollige, et alltoodud 6. sammus toodud kaubad ühtivad teie kavandatud B2C-seadistusega. Uusi profiile saab luua ka Azure AD sarnaste B2C rentnike või rakenduste abil, et arvestada väiksemate erinevustega, nagu erinevad kasutajapoliitika ID-d.
1. Valige **suvand Lisa saidi autentimise profiil**.
1. Sisestage järgmised nõutavad üksused kuvatud vormile, kasutades oma B2C rentniku ja rakenduse väärtusi. Väljad, mis ei ole kohustuslikud (ilma tärnita), võivad jääda tühjaks.

    - **Rakenduse nimi**: teie B2C rakenduse nimi, näiteks „Fabrikam B2C”.
    - **Rentniku nimi**: teie B2C rentniku nimi (nt „fabrikam“, kui domeen kuvatakse B2C rentnikule kui „fabrikam.onmicrosoft.com“). 
    - **Poliitika ID parooli unustamise korral**: kasutajavoo poliitika ID parooli unustamise korral, näiteks „B2C_1_PasswordReset”.
    - **Registreerumise poliitika ID**: registreerumise ja sisse logimise kasutajavoo poliitika ID, nt "B2C_1_signup_signin".
    - **Kliendi GUID**: B2C rakenduse ID, näiteks „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6”.
    - **Profiilipoliitika ID redigeerimine**: kasutajavoo poliitika ID profiili redigeerimiseks, näiteks „B2C_1A_ProfileEdit”.

1. Valige nupp **OK**. Nüüd peaks olema teie B2C rakenduse nimi loendis kuvatud.
1. Oma muudatuste salvestamiseks valige **Salvesta**.

Valikulist **kohandatud domeenivälja** tuleks kasutada ainult siis, kui seadistate Azure AD kohandatud domeeni B2C rentnikule. Täiendavate üksikasjade ja kaalutluste saamiseks kohandatud sisselogimise **domeeni** välja kasutamise kohta vt [B2C-lisateavet](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C rakenduse seostamine teie saidi ja kanaliga

> [!WARNING]
> - Kui teie sait on juba seostatud B2C rakendusega, siis teise B2C rakendusse üleminekul eemaldatakse praegused juba sellesse keskkonda registreerunud kasutajatele loodud viited. Kui seda muudetakse, ei ole kasutajatele saadaval ükski praegu määratud B2C rakendusega seotud mandaat. 
> - Värskendage B2C-rakendust ainult siis, kui häälestate kanali B2C-rakendust esmakordselt või kui soovite, et kasutajad logiks uuesti sisse uue B2C-rakendusega kanali uute mandaatidega. Olge ettevaatlik kanalite seostamisel B2C rakendustega ja nimetage rakendusi selgelt. Kui kanal ei ole seostatud B2C rakendusega alljärgnevate etappidega, on sisestatakse kasutajad teie saidi kanalisse siselogimisel B2C rakendusse olekuga **vaikimisi** B2C rakenduste loendis **Rentniku sätted \> B2C sätted**.

B2C rakenduse seostamiseks teie saidi ja kanaliga toimige järgnevalt.

1. Liikuge oma saidile kaubanduse saidiehitajas.
1. Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.
1. Jaotises **Saidi sätted** valige **Kanalid**.
1. Valige oma kanal põhiakna jaotises **Kanalid**.
1. Valige paremal kanali atribuutide paanil oma B2C-rakenduse nimi **rippmenüüst Vali B2C-rakendus**.
1. Valige **Sule** ja seejärel valige **Salvesta ja avalda**.

## <a name="next-steps"></a>Järgmised sammud

Äri rentniku B2C-rentniku seadistamise jätkamiseks jätkake [B2C lisateabega](additional-b2c-info.md).

## <a name="additional-resources"></a>Lisaressursid

[Jaekaubandusrentniku häälestamine Commerce'is](set-up-b2c-tenant.md)

[Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.](create-link-aad-b2c-tenant.md)

[B2C rakenduse loomine](create-b2c-app.md)

[Kasutajavoo poliitikate loomine](create-user-flow-policies.md)

[Sotsiaalstete identiteedipakkujate lisamine (valikuline)](add-social-identity-providers.md)

[Commerce headquartersi värskendamine uue Azure AD B2C-teabega](update-hq-aad-b2c-info.md)

[Lisateave B2C kohta](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
