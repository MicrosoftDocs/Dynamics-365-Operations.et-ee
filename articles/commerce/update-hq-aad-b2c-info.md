---
title: Commerce'i peakontori värskendamine uue Azure AD B2C teabega
description: See artikkel kirjeldab, kuidas värskendada Microsoft Dynamics 365 Commerce peakontorit Azure Active Directory uue (Azure AD) ettevõtte ja tarbija (B2C) teabega.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785805"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce'i peakontori värskendamine uue Azure AD B2C teabega

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas värskendada Microsoft Dynamics 365 Commerce peakontorit Azure Active Directory uue (Azure AD) ettevõtte ja tarbija (B2C) teabega.

Kui eelpool loetletud Azure AD B2C ettevalmistavad etapid on lõpule viidud, peab Azure AD B2C rakendus olema registreeritud teie Dynamics 365 Commerce'i keskkonnas.

Peakontori väsrkendamiseks uue Azure AD B2C teabega toimige järgmiselt.

1. Avage Commerce'i jaotis **Commerce'i jagatud parameetrid** ja valige vasakpoolsest menüüst **Identiteedipakkujad**.
1. Jaotises **Identiteedipakkujad** toimige järgmiselt.
    1. Sisestage **väljale Väljastaja** identiteedipakkuja väljastaja string. Oma väljastajastringi otsimiseks vt allolevat [peakontori häälestamise väljastaja stringi](#obtain-issuer-string-for-headquarters-setup).
    1. Sisestageoma väljaandja kirje nimi väljale **Nimi**.
    1. Väljale **Tüüp** sisestage **Azure AD B2C (id_token)**.
1. Jaotises **Sõltuvad osapooled**, kui eelpool mainitud B2C identiteedipakkuja üksus on valitud, tehke järgmist.
    1. Sisestage **boksi ClientID** oma B2C-rakenduse ID, **mille leiate oma B2C-rakenduse atribuutide lehe väljalt Rakenduse ID**.
    1. Väljale **Tüüp** sisestage **Avalik**.
    1. Väljale **Kasutajatüüp** sisestage **Klient**.
1. Valige toimingupaanil nupp **Salvesta**.
1. Sisestage Commerce'i otsingulahtrisse **Jaotusegraafik**
1. Lehe **Jaotusegraafik** vasakpoolses navigeerimismenüüs valige töö **1110 globaalne konfiguratsioon**.
1. Valige toimingupaanil käsk **Käivita kohe**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Hangi halduse häälestuse jaoks väljastaja string

Oma identiteedipakkuja väljastaja stringi hankimiseks järgige neid samme.

1. Liikuge Azure'i portaali Azure AD B2C lehel oma kasutajavoosse **Sisselogimine ja registreerimine**.
1. Valige **Lehe paigutused** vasakul navigeerimismenüüs, valige **Paigutuse nimi** suvand **Ühtne sisselogimine või registreerimine** lehel ja seejärel valige **Käivita kasutajavoog**.
1. Veenduge, et teie rakendus on seatud Azure AD ülal loodud kavandatud B2C-rakendusele ja valige seejärel kasutajavoo link, **mis kuvatakse pakett-töö Käivita kasutajavoo** päises ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Ära vali **Käivita kasutajavoog**.) Uus vahekaart avaneb kuvab metaandmed poliitika jaoks väljastaja stringi kogumiseks.
1. Brauseri vahekaardil kuvataval metaandmete lehel kopeerige identiteedipakkuja väljastaja string (**väljastaja** väärtus, alustades väärtusega "https://" ja lõpetades väärtusega "/v2.0/"), mis sarnaneb järgmise näitega.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**VÕI**: sama metaandmete URL-i käsitsi loomiseks tehke järgmist.

1. Looge metaandmete aadressi URL järgmises vormingus, kasutades oma B2C rentnikku ja poliitikat: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Näide: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Sisestage metaandmete aadressi URL brauseri aadressiribale.
1. Kopeerige metaandmetest identiteedipakkuja väljaandja URL (väärtus **„väljaandja”**).
    - Näide: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Järgmised sammud

Äri rentniku B2C-rentniku seadistamise jätkamiseks jätkake [oma B2C rentniku konfigureerimist Commerce’i saidi koostajas](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Lisaressursid

[Jaekaubandusrentniku häälestamine Commerce'is](set-up-b2c-tenant.md)

[Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.](create-link-aad-b2c-tenant.md)

[B2C rakenduse loomine](create-b2c-app.md)

[Kasutajavoo poliitikate loomine](create-user-flow-policies.md)

[Sotsiaalstete identiteedipakkujate lisamine (valikuline)](add-social-identity-providers.md)

[B2C rentniku konfigureerimine kaubanduse saidiehitajas](config-b2c-tenant-site-builder.md)

[Lisateave B2C kohta](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
