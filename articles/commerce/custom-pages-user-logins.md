---
title: Kohandatud lehtede seadistamine kasutajate sisselogimise jaoks
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce kohandatud lehti, mis käsitsevad Azure Active Directory (Azure AD) ettevõtte ja tarbija (B2C) rentnike kohandatud sisselogimisi.
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5d9f2febc912b35897b063019146d219cadea1fa
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517228"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Kohandatud lehtede seadistamine kasutajate sisselogimise jaoks


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce kohandatud lehti, mis käsitsevad Azure Active Directory (Azure AD) ettevõtte ja tarbija (B2C) rentnike kohandatud sisselogimisi.

## <a name="overview"></a>Ülevaade

Kohandatud lehtede kasutamiseks, mis on rakenduses Dynamics 365 Commerce volitatud käsitsema kasutaja sisselogimise voogusid, peate seadistama Azure AD poliitikad, millele Commerce’i keskkonnas viidatakse. Saate konfigureerida Azure AD B2C poliitikaid „Registreerimine ja sisselogimine”, „Profiili redigeerimine” ja „Parooli lähtestamine”, kasutades Azure AD B2C rakendust. Azure AD B2C rentniku ja poliitika nimedele saab seejärel viidata ettevalmistamise protsessi käigus, mis on tehtud Commerce’i keskkonnas, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).

Kohandatud Commerce’i lehti saab luua, kasutades sisselogimist, registreerumist, konto profiili redigeerimist või parooli lähtestamise moodulit. Nendele kohandatud lehtede jaoks avaldatud lehe URL-idele tuleb seejärel viidata Azure AD B2C poliitika konfiguratsioonides Azure’i portaalis.

## <a name="set-up-b2c-policies"></a>B2C poliitikate seadistamine

Pärast Azure AD B2C rentniku seadistamist ja selle seostamist oma Commerce’i keskkonnaga, avage Azure’i portaalis leht **Azure AD B2C** ja seejärel valige menüüs jaotises **poliitikad** suvand **Kasutaja vood (poliitikad)**.

![Kasutajavoogude (poliitikate) käsk menüüs](./media/B2C_CustomPage_PoliciesMenu.png)

Nüüd saate konfigureerida kasutaja sisselogimise vood „Registreerimine ja sisselogimine”, „Profiili redigeerimine” ja „Parooli lähtestamine”.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Poliitika „Registreerimine ja sisselogimine” konfigureerimine

Poliitika „Registreerimine ja sisselogimine” konfigureerimiseks toimige järgmiselt.

1. Valige suvand **Uus kasutaja voog** ja seejärel valige vahekaardil **Soovitatav** poliitika **Registreerimine ja sisselogimine**.
1. Sisestage poliitika nimi (nt **B2C\_1\_SignInSignUp**).
1. Jaotises **Identiteedipakkujad** valige poliitika jaoks kasutatavad identiteedipakkujad. Minimaalselt peab olema valitud **Registreerimine meili teel**.
1. Veerus **Atribuudi kogumine** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi** ja **Perekonnanimi** juures.
1. Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Identiteedipakkuja**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.

    ![Valitud atribuudid ja nõuded](./media/B2C_SignInSignUp_Attributes.png)

1. Poliitika loomiseks valige **OK**.
1. Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**
1. Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.

    ![Uue poliitika atribuutide leht](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Poliitika nimi on Commerce’i keskkonnas täielikult viidatud. (Viitesse kaasatakse eesliide **B2C\_1\_**.) Poliitikaid ei saa pärast loomist ümber nimetada. Kui asendate oma Commerce’i keskkonna olemasoleva poliitika, saate kustutada algse poliitika ja luua uue poliitika, millel on sama nimi. Teise võimalusena, kui keskkond on juba ette valmistatud, saate teenusetaotluse kaudu esitada uue poliitika nime.

Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks. Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.

### <a name="configure-the-profile-editing-policy"></a>Poliitika „Profiili redigeerimine” konfigureerimine

Poliitika „Profiili redigeerimine” konfigureerimiseks järgige allolevaid etappe.

1. Valige suvand **Uus kasutaja voog** ja seejärel valige vahekaardil **Soovitatav** poliitika **Profiili redigeerimine**.
1. Sisestage poliitika nimi (nt **B2C\_1\_EditProfile**).
1. Jaotises **Identiteedipakkujad** valige poliitika jaoks kasutatavad identiteedipakkujad. Minimaalselt peab olema valitud **Kohaliku konto sisselogimine**.
1. Veerus **Atribuudi kogumine** märkige märkeruudud suvandite **Meiliaadressid** ja **Perekonnanimi** juures.
1. Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Identiteedipakkuja**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.
1. Poliitika loomiseks valige **OK**.
1. Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**
1. Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.

Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks. Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.

### <a name="configure-the-password-reset-policy"></a>Poliitika „Parooli lähtestamine” konfigureerimine

Poliitika „Parooli lähtestamine” konfigureerimiseks järgige allolevaid etappe.

1. Valige suvand **Uus kasutaja voog** ja seejärel valige vahekaardil **Eelvaade** poliitika **Parooli lähtestamine v1.1**.

    ![Eelvaate vahekaardil on valitud poliitika Parooli lähtestamine v1.1.](./media/B2C_ForgetPassword_Menu.png)

1. Sisestage poliitika nimi (nt **B2C\_1\_ForgetPassword**).
1. Jaotises **Identiteedipakkujad** valige suvand **Parooli lähtestamine meiliaadressi kasutades**.
1. Veerus **Tagastamise nõue** märkige märkeruudud suvandite **Meiliaadressid**, **Eesnimi**, **Perekonnanimi** ja **Kasutaja objekti ID** juures.

    ![Valitud nõuded](./media/B2C_ForgetPassword_Attributes.png)

1. Poliitika loomiseks valige **OK**.
1. Topeltklõpsake uuel poliitika nimel ja seejärel valige navigeerimispaanil suvand **Atribuudid.**
1. Seadke suvand **JavaScripti lehe paigutuse (eelvaade) jõustamise lubamine** valikule **Sees**.

Pärast kohandatud lehtede loomist naasete sellesse poliitikasse seadistuse lõpetamiseks. Praegu sulgege poliitika, et naasta Azure’i portaali lehele **Kasutaja vood (poliitikad)**.

## <a name="build-the-custom-pages"></a>Kohandatud lehtede koostamine

Kasutaja sisselogimiste käsitsemiseks kohandatud lehtede koostamiseks toimige järgmiselt.

1. Avage Commerce’i autorluse tööriistades oma sait.
1. Koostage järgmised viis malli ja viis lehte.

    - Mall **Sisselogimine** ja sisselogimise moodulit kasutav leht.
    - Mall **Registreerimine** ja registreerimise moodulit kasutav leht.
    - Mall **Parooli lähtestamine** ja parooli lähtestamise moodulit kasutav leht.
    - Mall **Parooli lähtestamise kinnitus** ja parooli lähtestamise kinnituse moodulit kasutav leht.
    - Mall **Profiili redigeerimine** ja konto profiili redigeerimise moodulit kasutav leht.

Lehtede loomisel järgige järgmisi juhiseid.

- Kasutage iga lehe või mooduli jaoks paigutust ja stiili, mis vastab kõige paremini teie ettevõtte vajadustele.
- Avaldage kõik lehed ja URL-id, mida tuleb Azure AD B2C seadistuses kasutada.
- Pärast lehtede ja URL-ide avaldamist koguge URL-id, mida tuleb kasutada Azure AD B2C poliitika konfiguratsioonideks. Igale URL-ile lisatakse selle kasutamisel järelliide **?preloadscripts=true**.

> [!IMPORTANT]
> Ärge korduvkasutage universaalseid päiseid ja jaluseid, millel on suhtelised lingid. Kuna need lehed majutatakse kasutamisel Azure AD B2C domeenis, tuleks kõikide linkide jaoks kasutada ainult absoluutseid URL-e.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD B2C poliitikate konfigureerimine kohandatud lehe teabega 

Naaske Azure’i portaalis lehele **Azure AD B2C** ja valige menüüs jaotises **Poliitikad** suvand **Kasutajavood (poliitikad)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>Poliitika „Registreerimine ja sisselogimine” kohandatud lehe teabega värskendamine

Poliitika „Registreerimine ja sisselogimine” kohandatud lehe teabega värskendamiseks tehke järgmist.

1. Valige varasemalt konfigureeritud poliitikas **Registreerimine ja sisselogimine** navigeerimispaanil suvand **Lehe paigutused**.
1. Valige paigutus **Ühendatud registreerimine või sisselogimise leht**.
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk sisselogimise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.
1. Valige paigutus **Kohaliku konto registreerimise leht**.
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk registreerimise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.
1. Järgige jaotises **Kasutaja atribuudid** järgmisi samme.

    1. Atribuutide **Meiliaadressid**, **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** väljal **Vajab kinnitamist**.
    1. Atribuutide **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** väljal **Valikuline**.

    ![Kohaliku konto lehe poliitika konfigureerimine](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>Poliitika „Profiili redigeerimine” kohandatud lehe teabega värskendamine

Poliitika „Profiili redigeerimine” kohandatud lehe teabega värskendamiseks tehke järgmist.

1. Valige varasemalt konfigureeritud poliitikas **Profiili redigeerimine** navigeerimispaanil suvand **Lehe paigutused**.
1. Valige paigutus **Profiili redigeerimise leht**.
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk profiili redigeerimise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.
1. Järgige jaotises **Kasutaja atribuudid** järgmisi samme.

    1. Atribuutide **Meiliaadressid** ja **Eesnimi** jaoks valige suvand **Ei** väljal **Vajab kinnitamist**.
    1. Atribuutide **Eesnimi** ja **Perekonnanimi** jaoks valige suvand **Ei** väljal **Valikuline**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>Poliitika „Parooli lähtestamine” kohandatud lehe teabega värskendamine

Poliitika „Parooli lähtestamine” kohandatud lehe teabega värskendamiseks tehke järgmist.

1. Valige varasemalt konfigureeritud poliitikas **Parooli lähtestamine** navigeerimispaanil suvand **Lehe paigutused**.
1. Valige paigutus **Uue parooli leht**.
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk parooli lähtestamise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.
1. Valige paigutus **Konto kinnitamise leht**.
1. Seadistage suvand **Kohandatud lehe sisu kasutamine** valikule **Jah**.
1. Sisestage väljal **Kohandatud lehe URL** täispikk parooli lähtestamise kinnitamise URL. Lisage järelliide **?preloadscripts=true**. Sisestage näiteks ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. Valige väljal **Lehe paigutuse versioon (eelvaade)** suvand **1.2.0**.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Siltide ja kirjelduste vaikimisi tekstistringide kohandamine

Mooduliteegis on sisselogimise moodulid eeltäidetud siltide ja kirjelduste vaiketekstistringidega. Saate neid stringe tarkvara arenduskomplektis (SDK) kohandada, uuendades sisselogimise mooduli väärtusi failis global.json.

Näiteks unustatud parooli lingi vaiketekst on **Unustatud parool?**. Järgnevalt on näidatud see vaiketekst sisselogimise lehel.

![Sisselogimislehe ununenud parooli lingi vaiketekst](./media/B2C_SignUp_ModuleFace.png)

Siiski saate mooduliteegi sisselogimismooduli failis global.json muuta teksti väärtuseks **Kas unustasite parooli?**, nagu järgmises näites on näidatud.

![Värskendatud lingi tekst logisse mooduli Global. JSON failis](./media/B2C_CustomizingStringsForModule.png)

Pärast faili global.json värskendamist ja muudatuste avaldamist ilmub sisselogimise moodulil uus tekst nii Commerce'is kui ka raalajas sisselogimise lehel.

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)
