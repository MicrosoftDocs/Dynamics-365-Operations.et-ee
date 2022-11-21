---
title: Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.
description: See artikkel kirjeldab, kuidas luua või linkida Azure Active Directory portaalis olemasoleva (Azure AD) ettevõtte ja tarbija (B2C) rentnikuga Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785802"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas portaalis Azure Active Directory luua (Azure AD) ettevõttelt tarbijale (B2C) rentnikut või sellega linkida Microsoft Azure. Lisateavet vt teemast B2C [rentniku Azure Active Directory loomine](/azure/active-directory-b2c/tutorial-create-tenant).

Olemasoleva B2C rentniku loomiseks Azure AD või linkimiseks Azure’i portaalis järgige neid samme.

1. Logige sisse [Azure’i portaali](https://portal.azure.com/).
1. Valige Azure'i portaali menüüst käsk **Loo ressurss**. Veenduge, et kasutate tellimust ja kataloogi, mis on seotud teie Commerce'i keskkonnaga.

    ![Ressursi loomine Azure'i portaalis.](./media/B2CImage_1.png)

1. Avage **Identiteedi \> Azure Active Directory B2C**.
1. Kui olete lehel **Uue B2C üürniku loomine või olemasoleva rentnikuga linkimine**, kasutage ühte valikutest, mis sobib kõige paremini teie ettevõtte vajadustega.

    - **Loo uus Azure AD B2C rentnik**: kasutage seda suvandit uue Azure AD B2C rentniku loomiseks.
        1. Valige käsk **Loo uus Azure AD B2C rentnik**.
        1. Sisestage organisatsiooni nimi jaotises **Organisatsiooni nimi**.
        1. Sisestage algne domeeninimi jaotises **Algne domeeninimi**.
        1. Valige riik ja piirkond jaotises **Riik või piirkond**.
        1. Rentniku loomiseks valige **Loo**.

     ![Uue Azure AD rentniku loomine.](./media/B2CImage_2.png)

     - **Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega**: kasutage seda suvandit, kui teil on Azure AD B2C rentnik, mida soovite linkida.
        1. Valige **Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega**.
        1. Jaotises **Azure AD B2C rentnik** valige sobiv B2C rentnik. Kui valikukastis kuvatakse teade „Ei leitud ühtegi sobilikku B2C rentnikku”, pole teil kehtivat sobilikku B2C rentnikku ja teil on vaja luua uus.
        1. Tehke jaotises **Ressursigrupp** valik **Loo uus**. Sisestage ressursirühmale **Nimi**, mis sisaldab rentnikku ja valige **Ressursigrupi asukoht** ning seejärel **Loo**.

    ![Olemasoleva Azure AD B2C rentniku linkimine minu Azure'i tellimusega.](./media/B2CImage_3.png)

1. Kui uus Azure AD B2C kaust on loodud (see võib võtta mõne hetke), kuvatakse armatuurlaual link uuele kaustale. See link juhatab teid lehele „Tere tulemast Azure Active Directory B2C-sse”.

    ![Link uude kausta Azure AD](./media/B2CImage_4.png)

> [!NOTE]
> Kui teie Azure'i kontol on mitu tellimust või olete seadistanud B2C rentniku aktiivsele tellimusele linkimata, suunab ribareklaam **Tõrkeotsing** rentnikku tellimusega linkima. Valige tõrkeotsingu teade ja järgige tellimuse probleemi lahendamiseks juhiseid.

Järgmine pilt on Azure AD B2C ribareklaami **Tõrkeotsing** näide.

![Kuvatav hoiatus Kataloogist puudub aktiivne tellimus.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Järgmised sammud

B2C rentniku seadistamise jätkamiseks Äris jätkake [B2C-rakenduse loomisega](create-b2c-app.md).

## <a name="additional-resources"></a>Lisaressursid

[Jaekaubandusrentniku häälestamine Commerce'is](set-up-b2c-tenant.md)

[B2C rakenduse loomine](create-b2c-app.md)

[Kasutajavoo poliitikate loomine](create-user-flow-policies.md)

[Sotsiaalstete identiteedipakkujate lisamine (valikuline)](add-social-identity-providers.md)

[Commerce headquartersi värskendamine uue Azure AD B2C-teabega](update-hq-aad-b2c-info.md)

[B2C rentniku konfigureerimine kaubanduse saidiehitajas](config-b2c-tenant-site-builder.md)

[Lisateave B2C kohta](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
