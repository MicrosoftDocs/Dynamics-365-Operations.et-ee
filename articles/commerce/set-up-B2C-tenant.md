---
title: Jaekaubandusrentniku häälestamine Commerce'is
description: See artikkel kirjeldab, kuidas Azure Active Directory seadistada oma (Azure AD) ettevõtte-tarbe (B2C) rentnikud kasutajasaidi autentimiseks moodulis Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785123"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Jaekaubandusrentniku häälestamine Commerce'is

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas Azure Active Directory seadistada oma (Azure AD) ettevõtte-tarbe (B2C) rentnikud kasutajasaidi autentimiseks moodulis Dynamics 365 Commerce.

Dynamics 365 Commerce kasutab Azure AD B2C'd kasutaja mandaadi ja autentimise voogude toetamiseks. Kasutaja saab nende voogude kaudu registreeruda, sisse logida ja lähtestada parooli. Azure AD B2C talletab kasutaja tundliku autentimisteabe, nt kasutajanime ja parooli. B2C rentniku kasutajakirje salvestab kas kohaliku B2C kontokirje või B2C sotsiaalse identiteedi pakkuja kirje. Need B2C kirjed lingitakse Commerce'i keskkonna kliendikirjetega.

> [!WARNING] 
> Azure AD B2C kustutab vana (pärand) kasutajavood 1. augustiks 2021. Seetõttu peaksite plaanima oma kasutajavood migreerida uude soovitatud versiooni. Uus versioon pakub funktsioonide pariteeti ja uusi funktsioone. Commerce version 10.0.15 või uuema versiooni mooduliteeki tuleb kasutada soovitatud B2C kasutajavoogudega. Lisateabe saamiseks vt [Azure Active Directory B2C kasutajavoog](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce'i hindamiskeskkonnad on eellaaditud Azure AD B2C rentnikuga demo eesmärgil. Oma Azure AD B2C rentniku laadimine alltoodud juhiste alusel ei ole hindamiskeskkondade jaoks vajalik.

> [!TIP]
> Saate oma saidi kasutajaid täiendavalt kaitsta ja suurendada oma Azure AD B2C rentnike turvalisust Azure AD identiteedikaitse ja tingimusliku juurdepääsu abil. Azure AD B2C Premium P1 ja Premium P2 rentnikele pakutavate võimaluste ülevaatamiseks vt [Azure AD B2C identiteedikaitse ja tingimuslik juurdepääs](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Dynamics keskkonna eeltingimused

Enne alustamist veenduge, et teie Dynamics 365 Commerce keskkond ja e-äri kanal konfigureeritakse õigesti, täites järgmised eeltingimused.

- Seadke kassatoimingute **AllowAnonymousAccess** väärtuseks "1" Commerce headquarters`is:
    1. Minge **kassatoimingutesse**.
    1. Tehke paremklõps ruudustikul ja siis klõpsake **Isikupärasta**.
    1. Valige **Lisa väli**.
    1. Valige saadaoleva veeru loendist veerg **AllowAnonymousAccess** et see lisada.
    1. Tehke valik **Värskenda**.
    1. Toimingu **612** "Kliendi lisamine" jaoks muutke **AllowAnonymousAccessiks** "1".
    1. Käitage **1090 (Registrid)** töö.
- Häälestage numbriseeria kliendikonto atribuut **Käsitsi** väärtusele **Ei** Commerce headquarters`is:
    1. Valige suvandid **Jaemüük ja Kaubandus \> Peakontori seadistamine \> Parameetrid \> Nõuete parameetrid**.
    1. Valige **numbriseeria**.
    1. Topeltklõpsake **kliendikonto** real **numbriseeria koodi** väärtust.
    1. Numbriseeria **Üldises** kiirkaardis määrake olekuks **Käsitsi** väärtuseks **Ei**.

Pärast teie keskkonna Dynamics 365 Commerce juurutamist on soovitatav [lähtestada ka algandmed](enable-configure-retail-functionality.md) keskkonnas.

## <a name="next-steps"></a>Järgmised sammud

Äriportaalis B2C [Azure AD rentniku seadistamise jätkamiseks jätkake looge või linkige olemasoleva B2C rentnikuga Azure’i portaalis](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Lisaressursid

[Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.](create-link-aad-b2c-tenant.md)

[B2C rakenduse loomine](create-b2c-app.md)

[Kasutajavoo poliitikate loomine](create-user-flow-policies.md)

[Sotsiaalstete identiteedipakkujate lisamine (valikuline)](add-social-identity-providers.md)

[Commerce headquartersi värskendamine uue Azure AD B2C-teabega](update-hq-aad-b2c-info.md)

[B2C rentniku konfigureerimine kaubanduse saidiehitajas](config-b2c-tenant-site-builder.md)

[Lisateave B2C kohta](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
